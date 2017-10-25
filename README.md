# .ergodox

#### @rjhilgefort's Ergodox configuration

## Qwerty Layout (Main)

![](Qwerty.png?raw=true)

## Colemak Layout (Layer 4)

![](Colemak.png?raw=true)

## Firmware Flashing (Usage Instructions)

- Goto [configurator site](https://input.club/configurator-ergodox).
- Click "Import Map" of your existing layout (`./MDErgo1-Default.json`).
- Make any updates you want to make!
  - If you're like me, you'll want to take screenshots of your new layout (and commit to your repo).
- Click "download firmware" on the top right and unzip the download.
- Move all files at root of the download into your `.ergodox` directory.
  - If you're unsure which, just replace all the non-image files in this repo with the matching file names of what you just downloaded.
  - You may want to take a second here to verify the changes you are about to flash the firmware with. Assuming your using a VCS, just do a diff on the `.kll` files- or even the `.map` if you think it's more readable. The `.kll` files are what you are about the flash your firmware with though.
- In a terminal, navigate to the root of your `.ergodox` folder (or wherever you have your newly downloaded `.kll` files).
- Plug in just the left hand, use a paperclip to enter "Flash Mode", and run this command `dfu-util -D left_kiibohd.dfu.bin`.
- Plug in just the right hand, use a paperclip to enter "Flash Mode", and run this command `dfu-util -D right_kiibohd.dfu.bin`.
- Plug the keyboard back in normally and take it for a test spin. If it's not what you expect, then start over!
- Commit all your changes.

## Resources

- [Configurator](https://input.club/configurator-ergodox)
- [Flash Firmware](https://github.com/kiibohd/controller/wiki/Loading-DFU-Firmware#mac-osx)

## Ergodox EZ

Replication of the above layout, but for ergodox ez.

- [My Layout Configurator](http://configure.ergodox-ez.com/keyboard_layouts/kbmlob)
- [Flash Firmware App](https://s3.ca-central-1.amazonaws.com/ergodox-ez-configurator/executables/teensy.dmg)
