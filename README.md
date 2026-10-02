# Nova Player

**Nova Player plays experiences on [Nova](https://nova-woad-phi.vercel.app).** Press **Play** on any experience on the Nova website: Nova Player opens, downloads the experience, finds you a server, and you're in.

## Download

**[Download Nova Player for Windows](https://github.com/Gh0st2222/nova-player/releases/latest/download/NovaPlayer.exe)** (the latest release, always), or get it from the [Download page](https://nova-woad-phi.vercel.app/download) on the Nova website.

1. Run `NovaPlayer.exe`. It installs itself for your Windows account (in `%LOCALAPPDATA%\Nova Player`), with no administrator rights needed, and makes the website's Play buttons open it.
2. Go to the Nova website and press **Play** on an experience.

> Windows may say "Windows protected your PC", because Nova Player isn't code-signed yet. Choose **More info**, then **Run anyway**.

## Updates

Nova Player keeps itself up to date. Every time it starts, it checks for a newer release here, downloads it, checks that it arrived intact (SHA-256), and switches to it before your game starts. You never need to download it again.

Each release has a `latest.json` that says what the newest version is and where to get it.

## What it does on your computer

- It installs to `%LOCALAPPDATA%\Nova Player` and registers `nova://` links for your Windows account (`HKEY_CURRENT_USER\Software\Classes\nova`).
- It keeps downloaded experiences in `%APPDATA%\Nova Player\packages`, so each one downloads only once per update.
- Experiences run in Nova's sandbox: they can't read your files, start programs, or open their own network connections.

**Uninstall:** delete `%LOCALAPPDATA%\Nova Player`, `%APPDATA%\Nova Player` and the registry key `HKEY_CURRENT_USER\Software\Classes\nova`.

## Requirements

Windows 10 or 11, 64-bit. A graphics card that supports Vulkan or Direct3D 12 for most experiences.

## Licenses

Nova Player is free to download and use. Its source code isn't public.

Nova is built on [Godot Engine](https://godotengine.org), which is open source under the MIT license. The notices for Godot and the libraries it includes are in [GODOT_LICENSE.txt](GODOT_LICENSE.txt) and [THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt).
