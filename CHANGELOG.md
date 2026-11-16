# Changelog

**English** · [Русский](CHANGELOG.ru.md)

All notable changes to JoinSheets are documented here. Dates are release dates (UTC).

## Planned next

Formula handling cleanup: fix known bugs in formula parsing/evaluation and in
value-type coercion (numbers/dates/booleans). See
[#1](https://github.com/JoinSheets/JoinSheets/issues/1).

## [0.3.0b1] - 2026-11-15

### Added

- Multi-language UI support (English/Russian): every screen, button, tooltip,
  and error message -- including formula-parse errors -- is now translated.
  Settings → Language switches it live across every open tab, the same way
  the theme switcher already worked. Closes the placeholder noted in
  0.2.0b1.
- An "About" section in Settings: the running version (read from index.html's
  own version tag, so it can't drift out of sync) and a link to
  joinsheets.github.io.

### Changed

- The top nav row is now two flex blocks -- logo + "JoinSheets" brand, then
  the action buttons -- that wrap as whole units on a narrow screen, instead
  of wrapping wherever it happened to run out of width. The current preset's
  description moved to its own row below the buttons (omitted, not blank,
  when there is no description).

## [0.2.0b1] - 2026-11-01

### Added

- A settings screen (gear icon, top right, on every screen): currently holds a
  theme switcher; the language section is a placeholder for the next release.
  The chosen theme is saved and applied live across every open tab.
- Modular theming: the app's palette (~15 CSS custom properties) now lives in
  swappable `themes/*.css` files instead of being baked into `styles.css`. Four
  themes ship: Compose (matches joinsheets.github.io's own look -- the
  default), Auto (follows the OS/browser setting), Light, and Dark.
- A logo button in the nav header, linking to joinsheets.github.io.

### Changed

- The Export/Filter/Fields/Data nav buttons dropped their icons -- Filter's
  funnel icon was also the per-column quick-filter's own icon, so the same
  pictogram read as two different things. "Advanced filter" is now labeled
  "Filter".

## [0.1.0b1] - 2026-10-27

First release under the JoinSheets organization: ported from `ds-webui`
(DS-Pipeline org, last alpha `0.33.0a1`) -- code, comments, and the UI
translated to English, screens renamed (Data/Fields/Table), license switched to
Apache-2.0.
