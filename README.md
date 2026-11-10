# VoltBench releases

**VoltBench** is an electronics workbench: place an Arduino, ESP32, ESP8266 or Raspberry Pi Pico and parts, wire them, write the
firmware, run it on an emulated chip, then flash the real board.

This repository only holds the downloadable desktop apps. The app itself runs in the browser too, with nothing to install:
**https://voltbench.click**

## Download

Step-by-step install guides for Windows, macOS and Linux, with a button for your system:

**https://voltbench.click/#download**

Or take the files straight from the [latest release](https://github.com/voltbench/voltbench-releases/releases/latest):

| System | File | Notes |
| --- | --- | --- |
| Windows | `VoltBench_<version>_x64-setup.exe` | Recommended. An `.msi` is there for managed PCs. |
| macOS | `VoltBench_<version>_universal.dmg` | Apple silicon and Intel. |
| Linux | `VoltBench_<version>_amd64.AppImage` | Any distribution; updates itself. |
| Linux | `.deb` / `.rpm` | Debian, Ubuntu, Mint / Fedora, openSUSE. |

The `.sig` files and `latest.json` are used by the app's automatic updater; you do not need them.

## First start

- **Windows:** if “Windows protected your PC” appears, choose *More info*, then *Run anyway*.
- **macOS:** if the app “cannot be opened”, right-click it in Applications, choose *Open*, then *Open* again. Still blocked:
  `xattr -dr com.apple.quarantine /Applications/VoltBench.app`
- **Linux AppImage:** `chmod +x VoltBench_*_amd64.AppImage && ./VoltBench_*_amd64.AppImage` (needs `libfuse2`).
  To use USB serial ports add yourself to the group once: `sudo usermod -aG dialout $USER`, then log out and in.

Building and uploading firmware use free tools on your computer (arduino-cli, avrdude, esptool); the app shows how to install a
missing one. Signed-in users can also build on the server.

## Updates

The app checks this repository when it starts and offers new versions in a window. `.deb` and `.rpm` installs cannot update
themselves: download the new package from the latest release.

## Links

- Website and web app: https://voltbench.click
- Download guide: https://voltbench.click/#download
