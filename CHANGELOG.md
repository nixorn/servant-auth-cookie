# Change Log

## [HEAD]
## [0.6.0.3] - 2018-01-14
### Changed
- Fixed dependencies' bounds.

## [0.6.0.2] - 2018-01-13
### Added
- `CookiedWrapperClass` supports `MonadIO`- and `MonadThrow`-constrained monads.
### Changed
- Fixed dependencies' bounds.
- `AuthCookieExceptionHandler` requires type of underlying monad as parameter.

## [0.6.0.1] - 2017-12-29
### Changed
- Fixed module `tests/Utils` export.

## [0.6.0] - 2017-11-08
### Added
- `getHeaderSession` function to access session data without denying access to a route (issue #30).
- `cookied`function:
  - support for multiple-parametered handlers (issue #34).
  - `CookiedWrapper` type synonym and `CookieWrapperClass` class to ease work with the function (issue #38).

- Support for session cookies (issue #35):
  - `ssExpirationType` of `SessionSetting` record
  - `ExpirationType` datatype

- Support for refreshing cookies (issue #37):
  - `ssAutoRenew` of `SessionSetting` record

- Type synonyms for common boilerplates:
  - `AuthCookieExceptionHandler`
  - `AuthCookieHandler`

### Changed
- `cookied` function's signature, added argument of type `Proxy Session`.
- `addSession*` functions' signatures, added argument of `SessionSettings` type. Use `def` (from `Data.Default`) for fallback mode.
- Fixed bug with wrong time format in `removeSession*` functions (issue #39).
- Refactored internals:
  - Format of encoding cookies is different.
  - `Cookie` record is completely changed.
  - `WithMetadata` replaced with `PayloadWrapper`/`ExtendedPayloadWrapper`. Use the latter one in cookie handlers.
  - `encryptCookie`/`decryptCookie` merged with their session counterparts.

### Removed
- `acsExpirationFormat` field and `CannotParseExpirationTime` exception constructor are no longer needed.

## [0.5.0.7] - 2017-11-08
### Changed
- Fixed dependencies' bounds.

## [0.5.0.6] - 2017-10-23
### Changed
- Fixed dependencies' bounds.

## [0.5.0.5] - 2017-07-13
### Changed
- Fixed dependencies' bounds.

## [0.5.0.4] - 2017-05-27
### Changed
- Fixed dependencies' bounds.

## [0.5.0.3] - 2017-05-24
### Changed
- Fixed dependencies' bounds.

## [0.5.0.2] - 2017-04-26
### Changed
- Fixed dependencies' bounds.

## [0.5.0.1] - 2017-04-16
### Changed
- Fixed incompatibility with older versions of GHC.

## [0.5.0] - 2017-04-15
### Changed
- Server keys management:
  - `ServerKey` becomes `ServerKeySet`.
  - `mkServerKeyFromBytes` becomes `mkPersistentServerKey`.

### Deleted
- `mkServerKey` (instead use custom instance of `ServerKeySet`.

### Added
- class `Cookied` and function `cookied` to faciliate usage of mutable server keys.

## [0.4.4] - 2017-04-15
### Added
- Tests for the example.
- `parseSessionRequest` and `parseSessionResponse` functions.
- `removeSessionFromErr` function.

### Changed
- Fixed constraint for `removeSession`.

## [0.4.3.3]
### Added
- Changelog.

### Changed
- Fixed dependencies' bounds.

## [0.4.3.2] - 2016-02-02
### Changed
- Fixed dependencies' bounds.

## [0.4.3.1] - 2016-01-30
### Changed
- Fixed dependencies' bounds.

## [0.4.3]   - 2016-01-30
### Changed
- Fixed draining of `/dev/random`.
- Refactored the example.

## [0.4.2.1] - 2016-01-17
### Changed
- Fixed dependencies' bounds.

## [0.4.2]   - 2016-12-23
### Added
- `removeSession` function.

## [0.4.0]   - 2016-09-25
### Added
- Support for `servant-0.9`.
- Tags for bytestrings.

### Changed
- Switched to `base-compat`.

## [0.3.2]   - 2016-09-17
### Added
- `mkServerKeyFromBytes` function.

## [0.3.1]   - 2016-08-19
### Added
- `addSessionToErr` function.

## [0.3.0.3] - 2016-08-12
### Changed
- Fixed dependencies' bounds.

## [0.3.0.2] - 2016-08-04
### Changed
- Fixed dependencies' bounds.

## [0.3.0]   - 2016-07-27
### Changed
- Relicensed to `BSD3`
- The great and glorious refactoring of everything ;)

## [0.2.0]   - 2016-07-08
### Added
- Parameters:
  - hash algorithm
  - encryption/decryption algorithms
  - ...and many others.
- Tests
- Documentation

### Changed
- `RandomKey` and `ServerKey` initialization (without `unsafePerformIO`).

## [0.1.0.1] - 2016-06-15
### Changed
- More user-friendly example.

## 0.1.0     - 2016-06-05
### Added
- Initial version of the package.


[HEAD]:    ../../compare/v0.6.0.3...HEAD
[0.6.0.3]: ../../compare/v0.6.0.2...v0.6.0.3
[0.6.0.2]: ../../compare/v0.6.0.1...v0.6.0.2
[0.6.0.1]: ../../compare/v0.6.0...v0.6.0.1
[0.6.0]:   ../../compare/v0.5.0.7...v0.6.0
[0.5.0.7]: ../../compare/v0.5.0.6...v0.5.0.7
[0.5.0.6]: ../../compare/v0.5.0.5...v0.5.0.6
[0.5.0.5]: ../../compare/v0.5.0.4...v0.5.0.5
[0.5.0.4]: ../../compare/v0.5.0.3...v0.5.0.4
[0.5.0.3]: ../../compare/v0.5.0.2...v0.5.0.3
[0.5.0.2]: ../../compare/v0.5.0.1...v0.5.0.2
[0.5.0.1]: ../../compare/v0.5.0...v0.5.0.1
[0.5.0]:   ../../compare/v0.4.4...v0.5.0
[0.4.4]:   ../../compare/v0.4.3.3...v0.4.4
[0.4.3.3]: ../../compare/v0.4.3.2...v0.4.3.3
[0.4.3.2]: ../../compare/v0.4.3.1...v0.4.3.2
[0.4.3.1]: ../../compare/v0.4.3...v0.4.3.1
[0.4.3]:   ../../compare/v0.4.2.1...v0.4.3
[0.4.2.1]: ../../compare/v0.4.2...v0.4.2.1
[0.4.2]:   ../../compare/v0.4.0...v0.4.2
[0.4.0]:   ../../compare/v0.3.2...v0.4.0
[0.3.2]:   ../../compare/v0.3.1...v0.3.2
[0.3.1]:   ../../compare/v0.3.0.3...v0.3.1
[0.3.0.3]: ../../compare/v0.3.0.2...v0.3.0.3
[0.3.0.2]: ../../compare/v0.3.0...v0.3.0.2
[0.3.0]:   ../../compare/v0.2.0...v0.3.0
[0.2.0]:   ../../compare/v0.1.0.1...v0.2.0
[0.1.0.1]: ../../compare/v0.1.0...v0.1.0.1

