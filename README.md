# Fold music player (prop)

A one-screen music player for the Galaxy Z Fold 8 folded (cover) screen, built only from the
"Music App" frame in Figma (file `jO4VrQnb9mAVd7SkmDKv9Y`, node `4:9`, 523×847).

The only thing that works is the red play/pause button. Shuffle, skip, repeat, back, heart and
the bottom nav are artwork.

- Title: "Funiculì, Funiculà" (the Figma frame says "Jamme Jamme"; changed on request).
- Opens paused at 0:00. Play runs the progress bar and clock to 3:15, then returns to 0:00.
- Audio: drop a file named `song.mp3` next to `index.html` and it plays in sync (its length
  replaces 3:15). Without it, a silent timer drives the screen.
- `?t=85` starts at 1:25, `?play=1` starts playing.
- No fake status bar: the strip above the header is left empty for the phone's own time and
  signal icons.
- Keys: Space plays/pauses, R resets to 0:00.
- First tap on a phone goes full screen and keeps the screen awake; Add to Home screen
  launches it full screen.

The layout scales the Figma frame to fit any screen: the top bar sticks to the top, the nav to
the bottom, and the player sits centred between them.
