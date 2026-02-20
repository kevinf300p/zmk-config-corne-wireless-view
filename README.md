Keymap for ZMK firmware on Corne keyboard - This is the one WITH the Nice!View display

For simple editing of keymap:

https://nickcoutsos.github.io/keymap-editor/

## ZMK version pinning

ZMK is currently pinned to commit `ac7f75b859` (Jan 29 2026) in both `config/west.yml` and `.github/workflows/build.yml`. This is because ZMK `main` has a build-breaking bug where the `pillbug` board is defined multiple times, causing all builds to fail.

When unpinning, note that the board name changed: the pinned version uses `nice_nano` (with revision overlays for v2), while newer ZMK `main` uses `nice_nano_v2` as a separate board. Update `build.yaml` accordingly when switching back to `main` / `@main`.
