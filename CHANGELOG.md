# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/) and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [0.3.0](https://github.com/michaelherold/ksuid/compare/v0.2.0...v0.3.0) - 2021-10-07

### Added

- A utility function for converting from a hexidecimal-encoded string to a byte string. This is necessary to handle the default encoding of binary fields within PostgreSQL.

## [0.2.0](https://github.com/michaelherold/ksuid/compare/v0.1.0...v0.2.0) - 2020-11-11

### Added

- The ability to configure the random generator for the gem via `KSUID.configure`. This allows you to set up random generation to the specifications you need, whether that is for speed or for security.
- Support for ActiveRecord. You can now use `KSUID::ActiveRecord[:my_field]` to define a KSUID field using the Rails 5 Attributes API. There is also two new column types for migrations: `ksuid` and `ksuid_binary`. The first stores your KSUID as a string in the database, the latter as binary data.

### Changed

- The `KSUID::Type#inspect` method now makes it much easier to see what you're looking at in the console when you're debugging.

## [0.1.0](https://github.com/michaelherold/ksuid/tree/v0.1.0) - 2017-11-05

### Added

- Basic `KSUID.new` interface.
- Parsing of bytes through `KSUID.from_bytes`.
- Parsing of strings through `KSUID.from_base62`.
