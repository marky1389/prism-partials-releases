# Prism Partials Studio releases

Signed release builds and the update feed for **Prism Partials Studio**, a stereo VST3 effect that tracks the partials of incoming audio and resynthesizes your edits.

## Install

Download the ZIP for your system from [`downloads/`](downloads) (Windows: [Prism_Partials_Studio_3.1.0_Windows_VST3.zip](https://github.com/marky1389/prism-partials-releases/raw/main/downloads/Prism_Partials_Studio_3.1.0_Windows_VST3.zip)) and extract it. Copy the whole **Prism Partials Studio.vst3** folder into a VST3 plug-in folder, then rescan plug-ins in your DAW.

| System | Per-user folder |
| --- | --- |
| Windows x64 | `%LOCALAPPDATA%\Programs\Common\VST3\` |
| macOS | `~/Library/Audio/Plug-Ins/VST3/` |

In Ableton Live, turn on VST3 in Settings → Plug-Ins. If your VST3 folder is not on the host's search path, add it as a custom folder.

Version 3.1.0 is available for Windows. Copies of 3.0.2 to 3.0.4 need 3.1.0 installed once from the ZIP to switch to this update feed.

## Updates

Prism checks this repository for a newer version when its editor opens. Choose **Install update**: the download is checked against the release signature and installed while your DAW stays open. Close and reopen Prism, or reload your project, to use the new version. When the VST3 folder is writable, Prism also replaces it after the DAW quits.

To always run the version inside the VST3 folder, set the environment variable `PRISM_SAFE_MODE=1` before starting the DAW.

## What is here

- `channel/` is the update feed that the plug-in reads: `latest.txt` names the newest version and each version folder holds its signed manifest, release notes and packages. Prism accepts a package only when its signature verifies against the key built into the plug-in.
- `downloads/` holds the installer ZIPs. SHA-256 of the 3.1.0 Windows ZIP: `3769ba01bb532a014f47472a567c420b9cd8c339b73fa185604222c1e26a9d34`.

The plug-in source is kept elsewhere. This repository never holds the signing key.
