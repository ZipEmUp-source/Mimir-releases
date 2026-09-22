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

From v0.17.0 the Mac builds are signed with a Developer ID certificate and notarized by Apple, so Mimir opens like any other app: no warning, nothing to allow.

Versions before v0.17.0 were unsigned. If you still have one of those, Gatekeeper refuses to open it the first time: open **System Settings → Privacy & Security**, scroll to the notice about Mimir, and choose **Open Anyway** (on macOS 15 Sequoia this is the route that works; on older versions right-click → **Open** also does). If macOS calls the app "damaged", clear the quarantine flag once:

```
xattr -cr /Applications/Mimir.app
```

Or simply download the latest release and skip all of that.

## How updates reach you

Mimir checks this repository for a newer published release a few seconds after it starts and every six hours after that. When one is out, a gold **v0.x.y ready** pill appears in the status bar, and the **Tidings** tab in Settings shows the release notes. Nothing installs on its own; you decide.

**One-click install (v0.16.0 and later).** If you installed Mimir with the installer, the Tidings tab offers an **Install** button: Mimir downloads the update, checks it against the signing key built into the app, installs it, and restarts. Your sessions and settings stay where they are. Every update package is signed by the maintainer, and Mimir refuses any download that signature does not verify.

**Coming from v0.15.0 or earlier?** Those versions have no installer built in, so update by hand one last time: download the file for your platform from the latest release, quit Mimir, and run it. From then on, updates are one click. On a Mac, keep Mimir in **Applications**; an app still running from its disk image cannot replace itself.

The files ending in `.sig` and the `latest.json` on each release are what the in-app installer reads. You do not need to download them.

## Reporting a problem

Use **Report a bug** in Mimir's status bar (it attaches the black-box log), or open an issue here.

## License

MIT — see [LICENSE](LICENSE).
