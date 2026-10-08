# Nova Player

**Nova Player plays experiences on [Nova](https://nova-woad-phi.vercel.app).** Press **Play** on any experience on the Nova website: Nova Player opens, downloads the experience, finds you a server, and you're in.

## Download

**[Download Nova Player for Windows](https://github.com/Gh0st2222/nova-player/releases/latest/download/NovaPlayer.exe)** (the latest release, always), or get it from the [Download page](https://nova-woad-phi.vercel.app/download) on the Nova website.

1. Run `NovaPlayer.exe`. It installs itself for your Windows account (in `%LOCALAPPDATA%\Nova Player`), with no administrator rights needed, and makes the website's Play buttons open it.
2. Go to the Nova website and press **Play** on an experience.

> Windows may say "Windows protected your PC", because Nova Player isn't code-signed yet. Choose **More info**, then **Run anyway**.

## Updates

Nova Player keeps itself up to date. Every time it starts, it checks for a newer release here, downloads it, checks that it arrived intact (SHA-256), and switches to it before your game starts. You never need to download it again. The files it needs beside it (NVIDIA's DLSS libraries) come with each release the same way, and are put back if they go missing.

Each release has a `latest.json` that says what the newest version is and where to get it.

## What it does on your computer

- It installs to `%LOCALAPPDATA%\Nova Player` (with NVIDIA's DLSS libraries beside it) and registers `nova://` links for your Windows account (`HKEY_CURRENT_USER\Software\Classes\nova`).
- It keeps your settings (the **Settings** screen in every experience's Esc menu: DLSS, Frame Generation, Reflex, V-Sync, frame limit) in `%APPDATA%\Nova Player\settings.cfg`, for every experience.
- It keeps downloaded experiences in `%APPDATA%\Nova Player\packages`, so each one downloads only once per update.
- Experiences run in Nova's sandbox: they can't read your files, start programs, or open their own network connections.

**Uninstall:** delete `%LOCALAPPDATA%\Nova Player`, `%APPDATA%\Nova Player` and the registry key `HKEY_CURRENT_USER\Software\Classes\nova`.

## Requirements

Windows 10 or 11, 64-bit. A graphics card that supports Vulkan or Direct3D 12 for most experiences. NVIDIA DLSS needs an NVIDIA GeForce RTX card (Frame Generation: RTX 40 series or newer); NVIDIA Reflex, any recent NVIDIA card.

## Licenses

Nova Player is free to download and use. Its source code isn't public.

Nova is built on [Godot Engine](https://godotengine.org), which is open source under the MIT license. The notices for Godot and the libraries it includes are in [GODOT_LICENSE.txt](GODOT_LICENSE.txt) and [THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt).

NVIDIA DLSS: Nova Player includes NVIDIA's DLSS libraries (`nvngx_dlss.dll` and `nvngx_dlssg.dll`, © NVIDIA Corporation), which it keeps beside itself for DLSS, DLAA and DLSS Frame Generation on NVIDIA RTX graphics cards. They're NVIDIA's, under the NVIDIA RTX SDKs license (its text is in [THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt)): you may not reverse engineer, decompile, disassemble or modify them, or distribute them on their own. NVIDIA, DLSS and Reflex are trademarks of NVIDIA Corporation.
