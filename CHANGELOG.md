# Changelog

Notable changes to Hplay.

## Click wheel in apps

- Installed apps (Get More → Apps) now receive click-wheel input: turning the
  wheel and pressing the center button are forwarded into the app instead of
  requiring touch. The [hplay-market](https://github.com/iwohost/hplay-market)
  apps (Dice Roller, Library & Stats, Mashup) were updated to use it, and a
  new **Metronome** app was added, built around dialing in a tempo with the
  wheel.

## Get More (marketplace)

- Point Settings → Customize → Get More → Marketplace URL at a site hosting a
  `manifest.json` (see [hplay-market](https://github.com/iwohost/hplay-market))
  to browse and install content without ever reinstalling the app:
  - **Apps** — standalone HTML mini-apps, downloaded and run in a sandboxed
    `<iframe>` (no access to the library, settings, or storage beyond the
    read-only bridge below).
  - **Themes** — downloadable body/wheel color sets, joining the built-in
    themes in the Body/Wheel Color pickers.
  - **Decals** — plain images placed on the aluminum body, always rendered
    behind the screen and wheel so they can never cover a control.
- A read-only `postMessage` bridge lets an installed app request a snapshot of
  the song list and usage stats — no write path, so it can't touch playback,
  the library, or settings.
- Marketplace URL now defaults to the
  [hplay-market](https://github.com/iwohost/hplay-market) site, so Browse
  Apps/Themes/Decals work immediately with no setup.
- Browse Apps/Themes/Decals now look like an actual storefront: letter-
  monogram icons for apps, live color swatches for themes, real image
  thumbnails for decals, and Get/Installed/Applied rendered as colored pill
  badges.

## Lyrics

- Reads ID3v2 `SYLT` (synced) and `USLT` (plain) lyrics tags via `jsmediatags`
  for local files, folder scans, and the native Android bridge.
- Now Playing's center button cycles art → seek bar → lyrics (when available)
  → back to art. Synced lyrics auto-highlight and scroll to the current line.

## Customize

- **Engraving** — a short personal text line, styled in an etched-metal look,
  shown in the gap between the screen and click wheel. Hidden entirely when
  unset.
- **Decals** can be arranged by hand directly on the device body
  (Customize → Decals → Arrange on Screen): drag to move, pinch to resize and
  rotate.
