# GM-CTRL Releases

This repository hosts the Windows installer releases for **GM-CTRL** — the
Escape Room Game Master Control Panel desktop app from
[gmctrl.com](https://www.gmctrl.com).

It exists separately from the (private) source repository so that the auto-
update channel works without authentication.

## Download the latest installer

Grab the latest `GM-CTRL-Setup-X.Y.Z.exe` from the
[**Releases page**](https://github.com/X04N/gm-ctrl-releases/releases/latest).

After install, GM-CTRL keeps itself up-to-date automatically — every release
published here triggers an in-app notification with a one-click "Restart Now"
button (or "Skip this update" if you'd rather wait).

## Each release contains

| File | What it is |
|---|---|
| `GM-CTRL-Setup-X.Y.Z.exe` | NSIS installer for Windows x64 |
| `GM-CTRL-Setup-X.Y.Z.exe.blockmap` | Delta-update map (lets the auto-updater download only the changed bytes between versions) |
| `latest.yml` | Manifest used by `electron-updater` — contains the SHA-512 of the .exe for integrity verification |

## Verifying the installer

Each release's `latest.yml` includes a SHA-512 hash of the installer. The
auto-updater verifies this automatically. To verify manually:

```powershell
Get-FileHash GM-CTRL-Setup-X.Y.Z.exe -Algorithm SHA512
# Compare against the `sha512` field in latest.yml (base64-encoded)
```

## Reporting issues

This repo doesn't accept issues — file bug reports through the in-app
**Report a bug** button (sidebar or footer chip), or email
[bugs@gmctrl.com](mailto:bugs@gmctrl.com).
