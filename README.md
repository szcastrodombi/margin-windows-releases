<div align="center">

<img src="assets/banner.svg" alt="Margin: a small, fast, quiet web browser for Windows" width="100%">

<br>

[![Download](https://img.shields.io/badge/Download-latest-1b1b1d?style=for-the-badge&logo=windows&logoColor=white)](https://github.com/szcastrodombi/margin-windows-releases/releases/latest)
[![Version](https://img.shields.io/github/v/release/szcastrodombi/margin-windows-releases?style=for-the-badge&color=1b1b1d&label=version)](https://github.com/szcastrodombi/margin-windows-releases/releases)
[![Downloads](https://img.shields.io/github/downloads/szcastrodombi/margin-windows-releases/total?style=for-the-badge&color=1b1b1d)](https://github.com/szcastrodombi/margin-windows-releases/releases)
![Windows 11](https://img.shields.io/badge/Windows-11-1b1b1d?style=for-the-badge)

**Tabs that glide. Pages that rise in. Nothing in the way.**

[Install](#install) · [Motion](#motion) · [Tabs](#tabs) · [The field](#the-field) · [Privacy](#privacy) · [Reading](#reading-and-pages) · [Bring things over](#bring-things-over) · [Extensions](#extensions) · [Updates](#updates) · [Questions](#questions)

</div>

---

## Install

1. Download `Margin-Setup-<version>.exe` from the [latest release](https://github.com/szcastrodombi/margin-windows-releases/releases/latest).
2. Run it. It installs for **your Windows account only**: no administrator prompt.
3. If the PC doesn't have Microsoft's .NET 9 Desktop Runtime, the installer gets it first.
4. Margin appears in the Start menu and in **Settings › Apps › Default apps**, so you can make it the browser links open in.

| | |
|---|---|
| **Needs** | Windows 11 (it uses the WebView2 engine that ships with Windows) |
| **Installs to** | Your user profile, not Program Files |
| **Uninstall** | Settings › Apps. Removes the app and leaves your tabs, history, bookmarks and settings where they are |
| **Your data** | `%APPDATA%\Margin` (small JSON files) and `%LOCALAPPDATA%\Margin` (cookies, cache, site icons, extensions) |

---

## Motion

Motion is Margin's character, and it is on from the first launch.

- Tabs slide in from the side and glide to their places. Closed ones shrink away.
- Buttons rise to the pointer and spring back.
- Menus and overlays grow in. The tab column slides shut and open. Pages rise in.
- **Settings › Tabs › Reduce animations** makes all of it instant.

## Tabs

Put them where you like: **down the left or right side, or across the top.** The page sits in a card, in light, dark or automatic.

- **Pinned tabs,** drag to reorder, rename, duplicate, mute.
- **Sleeping tabs,** and tabs that close themselves into **Archived Tabs** after a while.
- **Tab groups** that fold, pins shown as rows, and **folders** in pinned rows, including live folders filled from an RSS or Atom feed.
- **Reopen closed tab** and full **session restore**. Or start with a fresh window every time, your choice.
- **Ctrl+K** searches your tabs. **Ctrl+Tab** switches with pictures.
- **Split View** with up to four pages side by side.
- **Peek** at a link without leaving the page: Shift-click it.
- **Private tabs.**
- **Profiles,** each with its own sign-ins, history and bookmarks, in a window of its own (File › Profile).
- Several windows (**Ctrl+N**), all of which come back after **Quit Margin (Ctrl+Q)**.

## The field

There is one floating field, and it takes addresses and words.

- Completion from your history and bookmarks, with typo-tolerant matching.
- **Tab to search** a site directly, site shortcuts, and a second engine on **Shift+Enter**.
- Search suggestions from your engine, and address bar commands.
- Click the tab you're on and type the address in the tab's own row, with suggestions underneath.
- A key that summons the field over any app.

## Privacy

Quiet by default. Every one of these has its own switch in Settings.

- **Shield:** a block list with cosmetic rules and YouTube ad rules.
- **Global Privacy Control,** which tells sites not to sell or share your data.
- **Click-tracker removal,** and **Copy Clean Link** to share a link without the tracking parts.
- **Site card** with permissions for the site you are on.
- **Pop-ups** are blocked, with Open and Always Allow when you want them.
- **Passwords belong to Proton Pass,** which comes with Margin and cannot be removed. Margin doesn't save, offer or fill passwords itself.
- Sync between your PCs runs through **a folder your PCs already share** (such as OneDrive), with no account. It carries bookmarks and settings, never history, passwords or tabs.

## Reading and pages

- **Reading mode,** which also reads a site's own markdown version when it publishes one, with a light, dark and auto switch in the corner.
- **Find on Page.**
- **Hide Elements** and **Hidden on This Site,** to take away what you don't want to see.
- **Your own CSS per site,** and darkening of pages that are light.
- **Floating video** (picture in picture).
- **Zoom per site.**
- **Capture** the visible page or the whole page, or drag out an area or click an element.

## Bring things over

**Bookmarks and history** come across from another browser: File › Bring Things Over.

**Sign-ins from Firefox** can be moved once, too. File › Bring Sign-ins Over reads straight from the Firefox profile on your PC.

- You choose every site. Nothing already in Margin is replaced.
- The last move can be undone for seven days.
- Close Firefox first.
- Some sites keep your login somewhere else and will still ask you.

## Extensions

Chrome extensions install from a Web Store link or an unpacked folder. They live behind the puzzle button, with their pop-ups, and you can pin the ones you use. Turn them on in private tabs too, if you want, under Settings › Extensions.

## Keyboard and mouse

| | |
|---|---|
| Ctrl+K | Search your tabs |
| Ctrl+Tab | Switch tabs, with pictures |
| Ctrl+N | New window |
| Ctrl+Q | Quit Margin; all windows come back next time |
| Shift+Enter | Search with your second engine |
| Shift-click a link | Peek at it |

Shortcuts can be rebound under Settings › Keyboard & Mouse. You can also hold the mouse's own Back or Forward button to pick a page from the list.

---

## Updates

Once a day Margin looks at this page for a newer build, downloads it, **checks its SHA-256 checksum,** and puts it in when you quit. Nothing restarts on its own. Turn it off any time: Settings › About › *Install updates by themselves*.

Settings › About lists every version with what changed in it, so you can go to a newer one or an older one. Choosing an older one pauses updates until you follow the latest again.

To check a download yourself, compare it against the `.sha256` file beside the installer:

```powershell
(Get-FileHash .\Margin-Setup-<version>.exe -Algorithm SHA256).Hash
```

## Questions

<details>
<summary><b>Why does Task Manager list Margin's pages under "WebView2 Manager"?</b></summary>
<br>
Margin runs its pages on the WebView2 engine in Windows, and Task Manager on current Windows 11 groups every WebView2 process under that name instead of the app that started it. Margin can't change how Windows groups them. Settings › About shows what Margin is really using, split between the app itself, each tab, and the engine they share.
</details>

<details>
<summary><b>Does it replace my default browser?</b></summary>
<br>
Only if you want it to. Settings › General › Make default opens Windows' default-apps page. Margin never switches it on its own.
</details>

<details>
<summary><b>Where is my data?</b></summary>
<br>
On your PC, in <code>%APPDATA%\Margin</code> and <code>%LOCALAPPDATA%\Margin</code>. Settings › About has an Open folder button. Margin has no account of its own.
</details>

<details>
<summary><b>Can I try a new build without touching my real data?</b></summary>
<br>
Yes: Margin Preview is the same app with its own name, icon, install folder and data. It is made for testing and isn't published here.
</details>

<details>
<summary><b>I'm on an older Windows, or a PC without WebView2.</b></summary>
<br>
Margin is built for Windows 11, where the WebView2 engine is part of Windows.
</details>

---

<div align="center">

This repository holds installers only. Margin's source lives in a private repository.

Licensed under the MIT License.

</div>
