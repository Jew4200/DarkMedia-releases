# Dark Media Viewer — Downloads

Portable Windows video, audio and image player. One file, no installer, nothing
to set up.

## Get it

Grab **DarkMedia.exe** from the [latest release](../../releases/latest) and
double-click it. Settings are written next to the exe, so it runs fine from a
USB stick or any folder you can write to.

Windows SmartScreen may warn about an unrecognised app because the exe is not
code-signed. Choose **More info → Run anyway**.

## Verifying your download

Every release also publishes `DarkMedia.exe.sha256`. To confirm the file you
downloaded is the one that was published:

```powershell
Get-FileHash .\DarkMedia.exe -Algorithm SHA256
```

The app does this automatically whenever it updates itself, and refuses to
install anything whose hash does not match.

## Updating

Open **Settings → Check for Updates…** inside the app. It downloads the newest
release, verifies the checksum, replaces itself and restarts. Your previous exe
is kept until the next launch in case you want to go back.

The app never contacts the network unless you press that button. The update
check sends no account name, machine name, file paths, or telemetry.

## Source

This repository only holds downloads. The source is kept in a separate private
repository.
