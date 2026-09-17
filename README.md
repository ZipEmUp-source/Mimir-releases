# Mimir — downloads

Mimir is a Norse-themed, multi-provider AI agent for the desktop: it chats, calls tools inside a sandboxed workspace, convenes a round table of other agents, and keeps its own counsel. This repository holds the **release builds** for Windows and macOS. The source lives in a private repository for now.

## Download

**[Latest release →](https://github.com/ZipEmUp-source/Mimir-releases/releases/latest)**

| Platform | File | Notes |
| --- | --- | --- |
| Windows 10 / 11, x64 | `Mimir_<version>_x64-setup.exe` | Installer. An `.msi` is provided as well. |
| macOS, Apple silicon | `Mimir_<version>_aarch64.dmg` | M1 and later |
| macOS, Intel | `Mimir_<version>_x64.dmg` | |

### Windows

SmartScreen may say "Windows protected your PC" because the installer is not yet code-signed. Click **More info → Run anyway**.

### macOS

The builds are not yet notarized with Apple, so Gatekeeper refuses to open Mimir the first time. Open **System Settings → Privacy & Security**, scroll to the notice about Mimir, and choose **Open Anyway** (on macOS 15 Sequoia this is the route that works; on older versions right-click → **Open** also does). If macOS calls the app "damaged", clear the quarantine flag once:

```
xattr -cr /Applications/Mimir.app
```

## How updates reach you

Mimir checks this repository for a newer published release a few seconds after it starts and every six hours after that. When one is out, a gold **v0.x.y ready** pill appears in the status bar, and the **Tidings** tab in Settings shows the release notes with a download link for your platform. Nothing installs on its own: download, quit Mimir, run the installer.

## Reporting a problem

Use **Report a bug** in Mimir's status bar (it attaches the black-box log), or open an issue here.

## License

MIT — see [LICENSE](LICENSE).
