# Workhorse Checklist Builder

A single-file, mobile-first tool for building on-screen checklist graphics for short-form video — TikTok, YouTube Shorts, and Instagram/Facebook Reels. Built for the **Workhorse AI & SEO** YouTube channel.

No install, no build step, no dependencies. Open `index.html` on your phone and go.

**Live demo:** `https://<your-github-username>.github.io/<your-repo-name>/` (see [Hosting on GitHub Pages](#hosting-on-github-pages) below)

---

## What it does

You fill in a title, subheading, checklist items (each with optional subtext), and a bottom phrase. The tool renders it as a vertical (9:16) on-screen graphic you can style, position, and then screen-record directly off your phone.

### Features

- **Content** — editable title, subheading, unlimited checklist items with optional subtext, optional bottom phrase. Items can be reordered or removed.
- **Themes & colors** — three built-in presets (Workhorse Dark, Clean Light, High Contrast), plus independent color pickers for every text role (title, subheading, body text, item subtext, check mark, bottom phrase, background). Enter exact hex codes directly, and save colors to a favorites palette for quick reuse.
- **Typography** — separate heading/body font choices, adjustable title and body size, Bold/Italic/Uppercase toggles. Fonts are offline-safe system fonts by default; Anton and Inter load from Google Fonts only if you select them.
- **Position & spacing** — content anchor (top/center/bottom/spread), fine X/Y nudge, spacing between sections and items, per-section text alignment (title, items, bottom phrase — each independently left/center/right), and an adjustable width for the checklist block itself.
- **Checklist box** — an optional brand-colored border around just the checklist items, with adjustable color, thickness, corner rounding, and inner padding.
- **Check animations** — three styles (Stroke draw, Pop fill, Slide check), an independent strikethrough toggle, and an adjustable animation speed.
- **Safe-zone guides** — a visual reference overlay for TikTok, YouTube Shorts, Instagram/FB Reels, or a "Universal" guide covering all three. This is advisory only — it never moves your content, and it never appears in Record Mode or in your actual recording.
- **Playback** — tap any item to check it off live while you record (so it matches your narration pace), or use auto-play with an adjustable delay for a hands-free version.
- **Record Mode** — hides all editor UI and goes full-bleed on your phone screen for clean recording. Swipe up anywhere on the stage (or press Escape on desktop) to exit back to the editor.

---

## Using it

1. Open `index.html` in a mobile browser (Chrome or Safari — see [Browser support](#browser-support)).
2. Fill in your content and style it using the sections below the preview.
3. Pick a safe-zone guide and eyeball your layout against it.
4. Tap **Record Mode**, start your phone's native screen recorder, and tap items to check them off as you talk.
5. Swipe up to exit Record Mode when you're done.

No data is saved between sessions — favorites and all your field values reset on page reload. This is intentional (see [Notes](#notes) below).

---

## Hosting on GitHub Pages

1. Push this repo to GitHub (if you haven't already).
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to "Deploy from a branch."
4. Set **Branch** to `main` (or whichever branch has `index.html`) and folder to `/ (root)`.
5. Save. GitHub will give you a URL like `https://<username>.github.io/<repo-name>/` — it usually takes a minute or two to go live.

No build step, no Actions workflow required — it's a static file.

---

## Browser support

The tool uses **CSS container query units** (`cqw`) so text and spacing scale cleanly with the graphic's size. This needs a reasonably modern browser:

- Chrome / Edge 105+
- Safari 16+ (iOS 16+)
- Firefox 110+

On older browsers, sizing falls back to viewport-width units (`vw`), which is close but not pixel-identical.

---

## Notes

- **No localStorage / persistence.** Everything (content, styling, favorite colors) lives in memory for the session only and resets on reload. This was a deliberate choice during development to keep the tool safe to preview inside Claude's artifact environment. If you want saved presets or persistence across sessions now that it's living on its own on GitHub Pages, that's a straightforward addition — see the [persistent storage](#) notes if you revisit this with Claude.
- **Optional online fonts.** Anton and Inter (used to more closely match the Workhorse brand look) load from Google Fonts only if you select them in the Typography section. Every other font option works fully offline.
- Safe-zone margins are approximate, industry-standard figures. Platform UI shifts occasionally — give your layout a quick visual check before publishing.

---

## License

MIT — see [LICENSE](LICENSE).
