# Duo Status Bar 2.0.4

## Fixes

- **ColorOS 17 (China) shade icons**: on these builds Duo's shade/QS copy hid the header's battery and
  signal but never drew the ring, so the pulled-down shade showed neither. The shade/QS copy is now
  turned off on ColorOS 17 CN builds and the stock header is left as is, whatever the "Show Duo in
  Quick Settings / notification panel" switches say. The 2.0.2/2.0.3 main-bar "mirror" workaround is
  removed: the device log showed the shade draws its own header, not a mirror. Reported on OnePlus 13
  (PJZ110), ColorOS 17.0.0.103.

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
