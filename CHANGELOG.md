Changelog
=========

All notable changes to this project will be documented in this file.

## [Unreleased]
### Added

- Add link ownership verification (#8703)
- Add conversations API (#8832)
- Add limit for the number of people that can be followed from one account (#8807)
- Add admin setting to customize mascot (#8766)
- Add support for more granular ActivityPub audiences from other software, i.e. circles (#8950)
- Add option to block all reports from a domain (#8830)
- Add user preference to always expand toots marked with content warnings (#8762)
- Add user preference to always hide all media (#8569)
- Add `force_login` param to OAuth authorize page (#8655)
- Add `tootctl accounts backup` (#8642, #8811)
- Add `tootctl accounts create` (#8642, #8811)
- Add `tootctl accounts cull` (#8642, #8811)
- Add `tootctl accounts delete` (#8642, #8811)
- Add `tootctl accounts modify` (#8642, #8811)
- Add `tootctl accounts refresh` (#8642, #8811)
- Add `tootctl feeds build` (#8642, #8811)
- Add `tootctl feeds clear` (#8642, #8811)
- Add `tootctl settings registrations open` (#8642, #8811)
- Add `tootctl settings registrations close` (#8642, #8811)
- Add `min_id` param to REST API to support backwards pagination (#8736)
- Add a confirmation dialog when hitting reply and the compose box isn't empty (#8893)
- Add PostgreSQL disk space growth tracking in PGHero (#8906)
- Add button for disabling local account to report quick actions bar (#9024)
- Add Czech language (#8594)
- Add `Clear-Site-Data` header when logging out (#8627)
- Add `same-site` (`lax`) attribute to cookies (#8626)
- Add support for styled scrollbars in Firefox Nightly (#8653)
- Add highlight to the active tab in web UI profiles (#8673)
- Add auto-focus for comment textarea in report modal (#8689)
- Add auto-focus for emoji picker's search field (#8688)
- Add nginx and systemd templates to `dist/` directory (#8770)
- Add support for `/.well-known/change-password` (#8828)
- Add option to override FFMPEG binary path (#8855)
- Add `dns-prefetch` tag when using different host for assets or uploads (#8942)
- Add `description` meta tag (#8941)
- Add `Content-Security-Policy` header (#8957)
- Add cache for the instance info API (#8765)

### Changed

- Change forms design (#8703)
- Change reports overview to group by target account (#8674)
- Change web UI to show "read more" link on overly long in-stream statuses (#8205)
- Change design of direct messages column (#8832, #9022)
- Change home timelines to exclude DMs (#8940)
- Change list timelines to exclude all replies (#8683)
- Change admin accounts UI default sort to most recent (#8813)
- Change documentation URL in the UI (#8898)
- Change style of success and failure messages (#8973)
- Change DM filtering to always allow DMs from staff (#8993)
- Change recommended Ruby version to 2.5.3 (#9003)

### Deprecated

- `GET /api/v1/timelines/direct` → `GET /api/v1/conversations` (#8832)
- `POST /api/v1/notifications/dismiss` → `POST /api/v1/notifications/:id/dismiss` (#8905)

### Removed

- Remove "on this device" label in column push settings (#8704)
- Remove rake tasks in favour of tootctl commands (#8675)

### Fixed

- Fix remote statuses using instance's default locale if no language given (#8861)
- Fix streaming API not exiting when port or socket is unavailable (#9023)
- Fix network calls being performed in database transaction in ActivityPub handler (#8951)
- Fix dropdown arrow position (#8637)
- Fix first element of dropdowns being focused even if not using keyboard (#8679)
- Fix tootctl requiring `bundle exec` invocation (#8619)
- Fix public pages not using animation preference for avatars (#8614)
- Fix OEmbed/OpenGraph cards not understanding relative URLs (#8669)
- Fix some dark emojis not having a white outline (#8597)
- Fix media description not being displayed in various media modals (#8678)
- Fix generated URLs of desktop notifications missing base URL (#8758)
- Fix RTL styles (#8764, #8767, #8823, #8897, #9005, #9007, #9018, #9021)
- Fix crash in streaming API when tag param missing (#8955)
- Fix hotkeys not working when no element is focused (#8998)
- Fix some hotkeys not working on detailed status view (#9006)

## [2.5.2] - 2018-10-12
### Security

- Fix XSS vulnerability (#8959)

## [2.5.1] - 2018-10-07
### Fixed

- Fix database migrations for PostgreSQL below 9.5 (#8903)
- Fix class autoloading issue in ActivityPub Create handler (#8820)
- Fix cache statistics not being sent via statsd when statsd enabled (#8831)
- Bump puma from 3.11.4 to 3.12.0 (#8883)

### Security

- Fix some local images not having their EXIF metadata stripped on upload (#8714)
- Fix being able to enable a disabled relay via ActivityPub Accept handler (#8864)
- Bump nokogiri from 1.8.4 to 1.8.5 (#8881)
- Fix being able to report statuses not belonging to the reported account (#8916)
