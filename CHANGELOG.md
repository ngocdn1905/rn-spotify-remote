# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.3.11-6] - 2022-06-04

### Fix
- Android null check to fix [#191](https://github.com/cjam/react-native-spotify-remote/issues/191) (Thanks @pretorh)

## [0.3.11-5] - 2022-02-10

### Fix

- Remove unused maven plugin (fix build error on react-native 0.67) (#177)

## [0.3.11-4] - 2022-02-10

### Update

- update legacy double-quoted import for `react-native` (#175)
- update `react-native-events` to `^1.0.21` (#174)

## [0.3.11-3] - 2021-12-19
### Fix
- Update react-native-events (Fix [#173](https://github.com/cjam/react-native-spotify-remote/issues/173))
- Fix PlayerRestrictions key name ([#172](https://github.com/cjam/react-native-spotify-remote/issues/172))

## [0.3.11-2] - 2021-11-11
### Documentation
- Add note for Android 11 setup

### Chore
- Fix build scripts, add back the postpack script
- update `.npmignore`

## [0.3.11-1] - 2021-10-17

### Update

- Update Spotify SDKS (again)
- Update [Readme](./README) with SDK Version Badges
- Update [Contributing Guide](./CONTRIBUTING)
- Add Dependabot configuration

## [0.3.11-0] - 2021-10-13

### Update

- Update Spotify SDKs (thanks Hoang)
  - Update Android SDK to [v7.0.0-appremote_v1.2.3-auth](https://github.com/spotify/android-sdk/releases/tag/v7.0.0-appremote_v1.2.3-auth)
  - Update iOS SDK to [v1.2.2](https://github.com/spotify/ios-sdk/releases/tag/v1.2.2)

### Fixed

- Fix Does not work when targeting Android SDK v30 (React Native 0.65+) #161 (thanks Hoang)
- Fix "missing SpotifyiOS.h" in example #78 #63 (thanks @dylancom)
- Fix example project podfile to build in XCode 12.5

## [0.3.10] - 2021-05-15

### Fixed

- More robust handling of session object on iOS [#146](https://github.com/cjam/react-native-spotify-remote/pull/146) (thanks @gustavoggs)

## [0.3.9] - 2021-05-17

### Fixed

- Fix crash when returned auth code was null [#138](https://github.com/cjam/react-native-spotify-remote/issues/138) (thanks @reinhardholl)

## [0.3.8] - 2021-05-07

### Fixed

- nil context title crash on iOS [#133](https://github.com/cjam/react-native-spotify-remote/pull/133) (thanks @srfaytkn!)
- getPlayerState 'Map already consumed' error [#133](https://github.com/cjam/react-native-spotify-remote/pull/133) (thanks @srfaytkn!)

## [0.3.7] - 2021-04-19

### Fixed

- Reference error for javascript projects [#127](https://github.com/cjam/react-native-spotify-remote/issues/127)

## [0.3.6] - 2021-04-15

### Added

- `playerContextChanged` events to iOS & Android [#118](https://github.com/cjam/react-native-spotify-remote/pull/118)
- CODE flow for Android Authentication [#121](https://github.com/cjam/react-native-spotify-remote/pull/121)

### Fixed

- Fix iOS returning access token instead of session object when re-authing [#112](https://github.com/cjam/react-native-spotify-remote/pull/112)
- Readme error in example code https://github.com/cjam/react-native-spotify-remote/pull/115

## [0.3.5] - 2021-02-27

### Fixed

- Fix for [Issue #100](https://github.com/cjam/react-native-spotify-remote/issues/100)

## [0.3.4] - 2021-02-15

### Fixed

- Renamed `RNSpotifyConvert` -> `RNSpotifyRemoteConvert` to fix [Issue #94](https://github.com/cjam/react-native-spotify-remote/issues/94) ([IbrahimCanKALYA](https://github.com/IbrahimCanKALYA))
- Fix [Issue #97](https://github.com/cjam/react-native-spotify-remote/issues/97)

### Updated

- Allow partial item to be passed into `playItemWithIndex` ([PR #91](https://github.com/cjam/react-native-spotify-remote/pull/91))
- Example to use library from source instead of installing local version
- Autogenerated documentation

## [0.3.3] - 2020-12-13

### Fixed

- Updated Peer Dependency on React Native to `>=0.60` [Issue #80](https://github.com/cjam/react-native-spotify-remote/issues/80)

### Added

- Better error messages on connection failures [Issue #65](https://github.com/cjam/react-native-spotify-remote/issues/65)
  - iOS now checks to see if Spotify is installed
- License file

### Updated

- Example app to RN 63.4

## [0.3.2] - 2020-05-17

### Fixed

- added some defaults for ApiConfig

### Added

- More documentation around setting up android project

## [0.3.1] - 2020-05-17 (pre-release)

### Fixed

- added some additional exports to `index.ts` to support missing typings

## [0.3.0] - 2020-05-16 (pre-release)

### Changed

- `ApiConfig.scope` to `ApiConfig.scopes` which is now of type `ApiScope[]` and also aligns to the web api scopes
- `ApiScope` enum values are now same as web api instead of bit flags
- `PlayerState.paused` -> `PlayerState.isPaused` to align with Spotify's iOS/Android sdk's

### Added

- Android Support! Big thanks to @YozhikM for the initial work on this
- `PlaybackRestrictions.canSeek`
- `SpotifyRemote.getChildrenOfItem` now has optional `options:GetChildrenItemsOptions` for android paging
- `SpotifyAuth.authorize` to replace `SpotifyAuth.initialize` which will now return a session object instead of just a token

### Deprecated

- `SpotifyAuth.initialize` in favor of `SpotifyAuth.authorize`

## [0.2.2] - 2020-03-22

### Changed

- Removed logging on release builds [Issue #31](https://github.com/cjam/react-native-spotify-remote/issues/31)

## [0.2.1] - 2020-03-22

### Fixed

- Playing Playlist Item would throw exception on PlayerState update [Issue #35](https://github.com/cjam/react-native-spotify-remote/issues/35)
- Safer use of the remote apis [Issue #32](https://github.com/cjam/react-native-spotify-remote/issues/32)

## [0.2.0] - 2020-02-19

### Changed

- Spotify SDK from 1.2.0 to 1.2.2
- Example App to use an App Context so that components could be factored to separate files

### Added

- `ApiConfig` (Used to authenticate and initialize session with `SpotifyAuth`)
  - `PlayURI` - URI to play when authorizing ([Issue #29](https://github.com/cjam/react-native-spotify-remote/issues/29))
  - `showDialog` - Whether or not to show the auth dialog
- `SpotifyAuth`
  - `endSession()` - Ends current session
  - `getSession()` - Gets the current session object
- `SpotifySession` - Session Object Definition
- `SpotifyRemote`
  - `disconnect()` - Disconnects the Remote from Spotify
- [Feature Matrix](./README.md#Features) to Readme (Docs)
- Example of queuing many tracks
- Requirement of XCode 11

## [0.1.1] - 2020-01-21

### Fixed

- Missing SpotifyiOS headers / Framework [Issue #25](https://github.com/cjam/react-native-spotify-remote/issues/25)

## [0.1.0] - 2020-01-17

### Changed

- `getRecommendedContentItems` now takes `options` object instead of `ContentType`
- Example app to more fully exercise exposed functionality [Issue #20](https://github.com/cjam/react-native-spotify-remote/issues/20)

### Fixed

- playerStateChanged event not triggered [Issue #14](https://github.com/cjam/react-native-spotify-remote/issues/14)

### Added

- `playItem`
- `playItemWithIndex` for [Issue #15](https://github.com/cjam/react-native-spotify-remote/issues/15)
- `getRootContentItems`
- `getContentItemForUri`
- `getCrossfadeState`
- `Track` Properties
  - `saved`
  - `episode`
  - `podcast`
- `ContentItem` Properties
  - `availableOffline`
  - `children`

## [0.0.8] - 2019-12-14

### Fixed

- #12: 'React/RCTConvert.h' file not found

### Added

- Troubleshooting section to readme

## [0.0.7] - 2019-12-13

### Fixed

- Error in Cocoapod install docs

## [0.0.6] - 2019-12-13

### Added

- Cocoapod support
- RN >= 0.60 support

## [0.0.5] - 2019-03-16

### Fixed

- Usage in README as it did not work

## [0.0.4] - 2019-03-16

### Added

- Example Server
- Example Project

## [0.0.2] - 2019-03-13

### Added

- Surfacing errors on iOS Authentication flow

### Changed

- Updates to API Docs

## [0.0.1] - 2019-03-13

### Added

- iOS Auth Support
- iOS App Remote
- Minor API Documentation