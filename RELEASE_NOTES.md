# Duo Status Bar 2.0.2

## Fixes

- **ColorOS 16/17 shade icons**: ColorOS mirrors the main status bar into the pulled-down shade
  (`qs_fake_statusicon_container` / `SystemIconFakeFrame`), so the battery, Wi-Fi and signal Duo hides
  in the main bar also vanished from the shade. While the shade or QS is open and Duo is not drawn
  there, the stock icons are now put back, and hidden again on collapse. Only ROMs that have the
  mirror resource take this path. Reported on OnePlus 13 (PJZ110), ColorOS 17.0.0.103.

# Duo Status Bar 2.0.1

A maintenance release on top of 2.0.0.

## Fixes

- **QS/shade hand-off**: the panel guards now retry the incoming/outgoing drawable check for a bounded
  window instead of giving up after one frame, so the main copy no longer stays visible over an expanded
  panel (or the outgoing copy is no longer kept after collapse).
- **Charge shake**: the 20 % shake no longer throws when it tags the view, so the animation runs and a
  second trigger cancels the previous one cleanly.
- **Shade fallback**: the shade copy keeps the right seat when there is no battery anchor.

The relay reporting fix is pending configuration and is not part of this build.
