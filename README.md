# Dark Media Viewer

A portable Windows player for **video, audio, images, GIFs, and animated WebP**.
Download one `DarkMedia.exe`, double-click it, and play. No installer, no Python,
nothing to set up.

Playback uses **libmpv** with FFmpeg inside the exe, so common and awkward
formats (AV1, HEVC, TrueHD, MIDI, tracker modules, and many others) work without
installing codecs.

## What it actually does

- Open a single file or a whole folder. The sidebar lists that folder in
  **Name View** or **Icon View**, with hover previews. Files that are currently
  hidden in Windows stay hidden.
- Play video and audio with seeking, remembered volume, loop, and
  **Auto Replay on Launch**.
- View still images with mouse-wheel zoom, drag-to-pan, and rotate from the
  View menu. GIFs and animated WebP play in place.
- **Clip Video** (green start / red end) or **Clip Video 20mb Cap** from Tools.
  The clip is saved next to the original, same type.
- **Color Scheme** editor with a live preview of the player.
- **Set as Default Player** for video and audio on this PC.
- **Uninstall** from Settings or Windows Apps & Features (removes settings and
  cache too).
- **Check for Updates** from Settings. The app does not talk to the network
  unless you press that button.

The player is one file you can copy anywhere. Settings, logs, and cache go in
the Windows app data folder (`%LOCALAPPDATA%\DarkMedia`), not beside the exe.

## Get it

Download **DarkMedia.exe** from the [latest release](../../releases/latest) and
double-click it.

Windows SmartScreen may warn about an unrecognised app because the exe is not
code-signed. Choose **More info → Run anyway**.

## Updating

Inside the app: **Settings → Check for Updates…**

It downloads the newest release, checks the published SHA-256, replaces itself,
and restarts. The previous exe is kept until the next launch.

## Verifying a download

Every release also publishes `DarkMedia.exe.sha256`. To confirm the file you
downloaded is the one that was published:

```powershell
Get-FileHash .\DarkMedia.exe -Algorithm SHA256
```

The in-app updater does this automatically and refuses anything whose hash does
not match.

## Privacy

No telemetry, no analytics, no background network activity. An update check is
one unauthenticated HTTPS GET to GitHub with `User-Agent: DarkMedia/<version>`
and nothing else — no account name, machine name, or file paths.

## Source

This repository only holds downloads. The source is kept in a separate private
repository.
