# Changelog

Notable changes to Hplay.

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
