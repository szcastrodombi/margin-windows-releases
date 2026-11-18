<div align="center">

# Margin

**A small, fast, quiet web browser for Windows.**
Tabs that glide. Pages that rise in. Nothing in the way.

[**Download the latest**](https://github.com/szcastrodombi/margin-windows-releases/releases/latest) · [All versions](https://github.com/szcastrodombi/margin-windows-releases/releases)

Windows 11 · installs for your account only · no administrator prompt

</div>

---

## Why Margin

- **Motion is the character.** Tabs slide in and settle, closed ones shrink away, menus grow in, the side column slides shut. One switch makes it all instant.
- **One floating field** for addresses and words, with completion from your history and bookmarks.
- **Tabs where you want them:** down the left or right, or across the top. Pins, groups, sleeping tabs, Ctrl+K tab search.
- **Quiet by default.** A built-in block list, click-tracker removal, Global Privacy Control, Reading mode, Hide Elements.
- **Light on your PC.** It uses the WebView2 engine already in Windows, so there is no second browser engine to download.
- **Proton Pass comes with it** for passwords. Bring your sign-ins over from Firefox in a few clicks.

## Install

1. Download `Margin-Setup-<version>.exe` from the [latest release](https://github.com/szcastrodombi/margin-windows-releases/releases/latest).
2. Run it. If your PC lacks Microsoft's .NET 9 Desktop Runtime, the installer gets it first.
3. Margin appears in the Start menu and in Settings › Apps › Default apps.

Uninstalling removes the app and leaves your tabs, history and bookmarks in place.

## Stays up to date

Once a day Margin checks this page, downloads a newer build, verifies its SHA-256 checksum, and puts it in when you quit.
Nothing restarts by itself. Settings › About lists every version if you want to go to an older one.

Each release lists its checksum file (`.sha256`) beside the installer, so you can check a download yourself:

```powershell
(Get-FileHash .\Margin-Setup-<version>.exe -Algorithm SHA256).Hash
```

## About this repository

This repository holds installers only. Margin's source lives in a private repository.

Licensed under the MIT License.
