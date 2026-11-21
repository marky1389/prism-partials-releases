# Prism Partials Studio releases

Signed release builds and the update feed for **Prism Partials Studio**, a stereo VST3 effect that tracks the partials of incoming audio and resynthesizes your edits.

## Install

Download the 3.2.0 ZIP for your system and extract it. Copy the entire **Prism Partials Studio.vst3** folder into a VST3 plug-in folder, then rescan plug-ins in your DAW.

- [Download for macOS 11 or later, Apple silicon or Intel](https://github.com/marky1389/prism-partials-releases/raw/main/downloads/Prism_Partials_Studio_3.2.0_macOS_VST3.zip).
- [Download for Windows x64](https://github.com/marky1389/prism-partials-releases/raw/main/downloads/Prism_Partials_Studio_3.2.0_Windows_VST3.zip).

| System | Per-user folder |
| --- | --- |
| Windows x64 | `%LOCALAPPDATA%\Programs\Common\VST3\` |
| macOS | `~/Library/Audio/Plug-Ins/VST3/` |

In Ableton Live, turn on VST3 in Settings → Plug-Ins. If your VST3 folder is not on the host's search path, add it as a custom folder.

Copies of 3.0.2 to 3.0.4 can use **Updates → Check for Updates → Install update** to get 3.2.0 from their existing update channel. Follow the restart instructions in your installed version.

## New in 3.2.0

Split the rack into up to seven frequency bands. Drag modules within a band or onto another band, close them on the row, or use Randomize to generate a chain for the selected band. Preset selection now refreshes the rack when patch notes are open, and the selected FFT size caps the Partials control.

## Updates

Prism checks this repository for a newer version when its editor opens. Choose **Install update**. Prism checks the download against the release signature and installs it while your DAW stays open. Close and reopen Prism, or reload your project, to use the new version. When the VST3 folder is writable, Prism also replaces it after the DAW quits.

To always run the version inside the VST3 folder, set the environment variable `PRISM_SAFE_MODE=1` before starting the DAW.

## What is here

- `channel/` is the update feed that the plug-in reads. `latest.txt` names the newest version, and each version folder holds its signed manifest, release notes and packages. Prism accepts a package only when its signature verifies against the key built into the plug-in.
- `downloads/` holds the installer ZIPs. The SHA-256 checksums for 3.2.0 are listed below.

| Installer | SHA-256 |
| --- | --- |
| Windows x64 | `0db422a6c5a3fd580c4eb32a5b3a78a1b61554e68e620afbb6843cdeee3d2f02` |
| macOS universal | `5439ed74197db833ec451ff3f8b4fd285e5d8a6ed561fb4a30cd6582b4b32c2f` |

The plug-in source is kept elsewhere. This repository never holds the signing key.
