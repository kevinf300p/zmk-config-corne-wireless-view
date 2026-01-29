Keymap for ZMK firmware on Corne keyboard - This is the one WITH the Nice!View display

### Keymap Editing
For simple editing of keymap:

https://nickcoutsos.github.io/keymap-editor/

### Upgrading Firmware
- After updating keymap, save the changes in the main branch
- Look in Actions tab for the new firmware (it will take some time to compile)
- Download the firmware to the local drive
- Plug in the keyboard directly via USB-C
- DOUBLE-TAP on the reset button of the keyboard, this will but it into flash mode
- If popup asks if device can connect, click "allow"
- Copy the correct firmware (left or right)
- Reboot the keyboard

---
# Notes

### Combo Keys

To prevent false combo triggers during fast typing, adjust these settings in your ZMK combo configuration:

require-prior-idle-msIdle
- time needed before combo activates
- 50-100ms (start with 75)

timeout-ms
- How long keys must overlap
- 30-50ms (increase if still triggering)

slow-release
- Keep combo active after releasing one key
- false (uncheck)

Start with 75ms for require-prior-idle and adjust:

Still triggering? Increase to 100-150ms
Combos feel sluggish? Decrease to 50ms

This forces a brief pause before the combo can activate, which won't affect your normal typing but will block the rolling-finger false triggers.
