<div align="center">

<img src="https://avatars.githubusercontent.com/u/78095377?s=200&v=4" alt="LeviLauncher Logo" width="120" style="border-radius: 20%;" />

# LeviLauncher Unlocked

**A lightweight, unlocked Android launcher for Minecraft: Bedrock Edition**  
*Universal package detection • Patched client support • Multi-instance isolation*

[![Platform: Android 9.0+](https://img.shields.io/badge/Platform-Android%209.0%2B-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://www.android.com/)
[![Architecture: ARM64](https://img.shields.io/badge/Arch-ARM64--v8a-FF6F00?style=for-the-badge&logo=arm&logoColor=white)](https://arm.com/)
[![License: Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg?style=for-the-badge)](LICENSE)
[![Status: Testing](https://img.shields.io/badge/Status-Experimental%20%2F%20Testing-orange?style=for-the-badge)](#testing-project-notice)

<br/>

[Overview](#overview) •
[Features](#key-features) •
[Comparison](#upstream-vs-unlocked) •
[Supported Packages](#supported-packages) •
[Requirements](#system-requirements) •
[Installation](#installation) •
[Building](#building-from-source) •
[Credits](#credits--acknowledgements)

</div>

---

## Overview

**LeviLauncher Unlocked** is an enhanced fork of [LeviLaunchroid](https://github.com/LiteLDev/LeviLaunchroid) by LiteLDev. 

While the official upstream launcher is strictly restricted to the official Google Play release (`com.mojang.minecraftpe`), **LeviLauncher Unlocked removes package name restrictions**. It provides full, first-class support for discovering, managing, and launching any installed Minecraft: Bedrock Edition package on Android—including patched, cloned, beta, and preview variants—as well as importing custom patched APK and APKS files.

---

## Upstream vs. Unlocked

| Feature | Upstream (`LiteLDev/LeviLaunchroid`) | LeviLauncher Unlocked |
|:---|:---:|:---:|
| **Official Play Store (`com.mojang.minecraftpe`)** | ✅ Supported | ✅ Supported |
| **Patched Packages (`.patch`, `.prpatch`, `.capespatch`)** | ❌ Hidden / Ignored | ✅ **Auto-detected & Tagged** |
| **Preview & Beta Packages (`minecraftpreview`, etc.)** | ❌ Not detected | ✅ **Fully Supported** |
| **Custom Cloned Packages (e.g., custom MCBE builds)** | ❌ Rejected | ✅ **Detected via `libminecraftpe.so`** |
| **Patched APK / APKS Importing** | ❌ Rejects ("Not a Minecraft APK") | ✅ **Direct Import Supported** |
| **Profile & Storage Isolation** | ⚠️ Collides on single ID | ✅ **Per-package metadata & runtime isolation** |
| **Standalone Launch (No Minecraft on system)** | ❌ Crashes ("Minecraft not found") | ✅ **Independent APK runtime fallback** |
| **Native `.so` Mod Loading & Preloader** | ✅ Supported | ✅ Supported |
| **Xbox Multi-Account Switcher** | ✅ Supported | ✅ Supported |

---

## Key Features

- 🔓 **Universal Package Detection**  
  Scans and identifies all installed Minecraft variants on your device using Android package queries and native binary heuristics (`libminecraftpe.so`), supporting official and modified packages alike.

- 🏷️ **Clear Visual Suffix Badges**  
  Instances are visually tagged in the launcher's version list with their package variant suffix (e.g. `Minecraft [.patch] (1.21.80)`, `Minecraft [.capespatch] (1.21.70)`), making multi-client setups effortless to organize.

- 📦 **Seamless APK & APKS Importing**  
  Import patched APKs and split APKS files directly. The validation logic inspects internal native architecture rather than enforcing a strict Mojang package ID check.

- 🛡️ **Isolated Profiles & Runtime Environments**  
  Each package variant stores its data in dedicated profile directories (`.levi_mc/profiles/<packageName>/`) and extracts native binaries into isolated runtime folders (`.levi_mc/minecraft_libs/<packageName>/`), preventing binary conflicts and save data collisions.

- 🚀 **Installation-Free Execution**  
  Run imported Minecraft APKs directly through the launcher without requiring Minecraft to be installed as a system package.

- 🧩 **Native `.so` Mod Loader**  
  Inject and execute custom native `.so` modules and preloaders to enhance your gameplay, performance, and custom UI.

- 👤 **Account & Content Management**  
  Switch seamlessly between multiple Xbox profiles and manage your worlds, texture packs, and behavior packs from one unified interface.

---

## Supported Packages

LeviLauncher Unlocked is built to recognize any Minecraft: Bedrock Edition package format, including:

- `com.mojang.minecraftpe` (Official Google Play release)
- `com.mojang.minecraftpe.patch` (Common patched client format)
- `com.mojang.minecraftpe.prpatch` (PR-patched client format)
- `com.mojang.minecraftpe.capespatch` (Custom capes patched client format)
- `com.mojang.minecraftpe.beta` (Bedrock Beta releases)
- `com.mojang.minecraftpreview` (Minecraft Preview)
- **Custom cloned & renamed packages** containing `libminecraftpe.so`

---

## System Requirements

| Requirement | Minimum | Recommended |
|:---|:---|:---|
| **Operating System** | Android 9.0 (API 28) | Android 11.0+ (API 30+) |
| **CPU Architecture** | ARM64 (`arm64-v8a`) | ARM64 (`arm64-v8a`) |
| **RAM** | 1 GB free | 3 GB or more |
| **Available Storage** | 2 GB | 5 GB or more |

> [!NOTE]
> On **Android 11 and newer**, package visibility restrictions apply. LeviLauncher Unlocked includes the `QUERY_ALL_PACKAGES` permission and explicit `<queries>` declarations so that your installed patched packages can be discovered automatically.

---

## Installation

### Option 1: Pre-built APK
1. Download the latest release APK from the **[Releases](https://github.com/PixelBoy78/LeviLaunchroidUnlocked/releases)** page or from your GitHub Actions build artifacts.
2. Ensure **"Install from unknown sources"** is enabled in your Android device's security settings.
3. Open and install the APK on your device.
4. Launch **LeviLauncher**, grant the required storage permissions, and your installed Minecraft versions will be detected automatically.

### Option 2: Standalone APK Import
If you do not have Minecraft installed on your Android system:
1. Open LeviLauncher Unlocked.
2. Navigate to the **Versions / Instances** tab and choose **Import APK/APKS**.
3. Select your Minecraft Bedrock APK file. The launcher will extract and configure an isolated instance ready to launch.

---

## Building from Source

To compile LeviLauncher Unlocked locally:

### Prerequisites
- [Git](https://git-scm.com/)
- [Android Studio Ladybug (or newer)](https://developer.android.com/studio)
- JDK 21 or higher
- Android SDK (API 35, Build Tools 35.0.0)

### Build Commands

```bash
# 1. Clone the repository
git clone https://github.com/PixelBoy78/LeviLaunchroidUnlocked.git
cd LeviLaunchroidUnlocked

# 2. Build Debug APK (Linux / macOS)
./gradlew assembleDebug

# 2. Build Debug APK (Windows PowerShell)
.\gradlew.bat assembleDebug
```

The compiled APK will be located at:
`app/build/outputs/apk/debug/app-debug.apk`

---

## Usage Guidelines & Disclaimer

- **Personal Use:** LeviLauncher is intended for personal gameplay, testing, and educational purposes.
- **Fair Play:** Do not use this launcher to violate Mojang, Microsoft, or server terms of service.
- **Liability:** The authors and contributors are not responsible for account bans, data loss, or issues resulting from the use of third-party modified clients.

---

## Credits & Acknowledgements

LeviLauncher Unlocked is built upon the incredible work of the open-source community:

- **[LiteLDev / LeviMC](https://github.com/LiteLDev/LeviLaunchroid)** – Original creators and maintainers of LeviLaunchroid.
- **[Android Open Source Project](https://source.android.com/)** – Tooling, runtime, and ecosystem support.
- **All Community Contributors** – For ongoing testing, bug reports, and passion for the Minecraft Bedrock ecosystem.

LeviLauncher Unlocked is licensed under the **[Apache License 2.0](LICENSE)**.

---

> [!NOTE]
> ### Testing Project Notice
> This repository is a personal testing and experimental project. I do not have any intention or commitment to update or maintain it regularly. Use at your own discretion.
