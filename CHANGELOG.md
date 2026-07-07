# Changelog

All notable changes to this tool are documented here.

## [1.3.0]
### Added
- Hex code text input paired with every color swatch, so exact brand colors can be typed in directly.
- Favorite colors palette — save any selected color and reapply it to other fields with one tap.
- Adjustable width control for the checklist items block (and the box around it), independent of title/bottom phrase width.

## [1.2.0]
### Fixed
- Content was visually off-center. Root cause: content position was being driven by the (intentionally asymmetric) safe-zone margins. Content positioning is now decoupled from the safe-zone guide, which is purely a visual reference overlay.
### Added
- Independent color controls for every text role: title, subheading, body text, item subtext, check mark, bottom phrase, and background (previously several of these shared a single color).
### Changed
- Removed the on-screen exit button in Record Mode. Exiting is now done with a swipe-up gesture (or Escape on desktop), so nothing appears on screen during an actual recording.

## [1.1.0]
### Fixed
- The checklist box (brand-colored frame) control was present but easy to miss — it lived inside a collapsed section. Moved to its own clearly labeled "Checklist box" section.
- The box now wraps only the checklist items, not the entire graphic (title/bottom phrase sit outside it).

## [1.0.0]
### Added
- Content anchor position (top/center/bottom/spread) plus fine X/Y nudge.
- Adjustable spacing between sections, between checklist items, and between title/subheading.
- Independent text alignment per section (header, items, bottom phrase).
- Customizable brand-colored box around the checklist, with adjustable color, border thickness, corner rounding, and padding.

## [0.1.0] — Initial release
### Added
- Editable title, subheading, checklist items (with optional subtext), and bottom phrase.
- Three theme presets (Workhorse Dark, Clean Light, High Contrast) plus custom color pickers.
- Typography controls: heading/body font choice, size sliders, Bold/Italic/Uppercase toggles.
- Three check-mark animation styles (Stroke draw, Pop fill, Slide check) with an independent strikethrough toggle and adjustable speed.
- Safe-zone guides for TikTok, YouTube Shorts, and Instagram/FB Reels, including a combined "Universal" guide.
- Tap-to-check and auto-play playback modes.
- Record Mode for clean, full-screen phone recording.
