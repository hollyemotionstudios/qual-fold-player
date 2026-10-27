# Fold music player (prop)

A one-screen music player for the Galaxy Z Fold 8 folded (cover) screen, built only from the
"Music App" frame in Figma (file `jO4VrQnb9mAVd7SkmDKv9Y`, node `4:9`, 523×847).

The only things that work are the red play/pause button, the progress bar (tap or drag it
to jump to any point in the song) and the album cover (tap it to reset to 0:00, paused). Shuffle, skip, repeat, back, heart and
the bottom nav are artwork.

- Title (big title and header): "Jamme, Jamme"; subtitle: "Let’s Go to the Top" (the Figma
  frame says "Jamme Jamme" / "Let’s Go"; changed on request). The album cover is a
  "Jamme, Jamme / Napoli · Italia" poster (assets/cover-jamme.jpg).
- Opens paused at 0:00. Play runs the progress bar and clock to 3:15, then returns to 0:00.
- Audio: drop a file named `song.mp3` next to `index.html` and it plays in sync (its length
  replaces 3:15). Without it, a silent timer drives the screen.
- `?t=85` starts at 1:25, `?play=1` starts playing.
- No fake status bar: the strip above the header is left empty, as in the Figma frame.
- Keys: Space plays/pauses, R resets to 0:00.
- Full screen, no status bar: installed from the home screen it opens full screen (manifest
  display: fullscreen, falling back to standalone), and in a browser tab the first tap goes
  full screen. The first tap also keeps the screen awake.
- sw.js is a pass-through service worker; it's there so Chrome on Android installs the player
  as a real app (in the app drawer) instead of a home-screen shortcut.

The layout scales the Figma frame to fit any screen: the top bar sticks to the top, the nav to
the bottom, and the player sits centred between them.
