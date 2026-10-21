<div align="center">

![LeviLauncher Logo](https://avatars.githubusercontent.com/u/78095377?s=200&v=4)

# LeviLauncher Unlocked

![Banner](https://camo.githubusercontent.com/bd7bd77cb422a267057d9863095b239b096d4f46dc831a37b45867a9acfad697/68747470733a2f2f63617073756c652d72656e6465722e76657263656c2e6170702f6170693f747970653d576176696e6726636f6c6f723d74696d654772616469656e74266865696768743d33303026616e696d6174696f6e3d66616465496e2673656374696f6e3d68656164657226746578743d4c6576694d4326666f6e7453697a653d313230)

**A lightweight Android launcher for Minecraft: Bedrock Edition**

[![GitHub Release](https://img.shields.io/github/v/release/LiteLDev/LeviLaunchroid?style=flat-square&color=blue)](https://github.com/LiteLDev/LeviLaunchroid/releases)
[![License: Apache 2.0](https://img.shields.io/github/license/LiteLDev/LeviLaunchroid)](https://github.com/LiteLDev/LeviLaunchroid/blob/main/LICENSE)
[![Issues](https://img.shields.io/github/issues/LiteLDev/LeviLaunchroid?style=flat-square&color=red)](https://github.com/LiteLDev/LeviLaunchroid/issues)
[![Stars](https://img.shields.io/github/stars/LiteLDev/LeviLaunchroid?style=flat-square&color=yellow)](https://github.com/LiteLDev/LeviLaunchroid)
[![Downloads](https://img.shields.io/github/downloads/LiteLDev/LeviLaunchroid/total.svg)](https://github.com/LiteLDev/LeviLaunchroid/releases)
[![Android](https://img.shields.io/badge/Android-9.0%2B-green?style=flat-square&logo=android)](https://www.android.com/)

</div>

---

## Introduction

**LeviLauncher Unlocked** is a modified fork of [LeviLaunchroid](https://github.com/LiteLDev/LeviLaunchroid), a lightweight, open-source Android launcher specifically designed for players of Minecraft: Bedrock Edition (MCBE). 

While the official upstream launcher is strictly locked to the official `com.mojang.minecraftpe` Google Play installation, this **Unlocked fork adds universal package support**. It allows you to discover, manage, and launch **any installed Minecraft package**, including patched and cloned clients (such as `.patch`, `.prpatch`, `.capespatch`, `.beta`, Preview, etc.) as well as importing custom patched APKs and APKS bundles.

### Fork Highlights & Features

- **Universal Package Support** – Detects and runs any Minecraft Bedrock package on your device, not just the official Play Store edition (`com.mojang.minecraftpe`, `com.mojang.minecraftpe.patch`, `com.mojang.minecraftpe.prpatch`, `com.mojang.minecraftpe.capespatch`, and custom cloned packages).
- **Patched Version Display** – Installed patched packages are clearly identified and tagged in the version selector and instance manager (e.g. `Minecraft [.patch]`, `Minecraft [.prpatch]`, `Minecraft [.capespatch]`) with independent profile data.
- **Support for Patched APK/APKS Imports** – Import patched APK or APKS bundles directly without encountering "Not a Minecraft APK" validation rejections.
- **Installation-Free & Unlocked Launching** – Bypassed Play Store verification restrictions, allowing you to run imported Minecraft APKs directly.
- **Native SO Module Loading** – Load external native SO mods and preloader modules to enhance gameplay and performance.
- **Multi-Version Management & Version Isolation** – Manage multiple Minecraft versions independently with isolated directories, configurations, and worlds.
- **Xbox Account & Content Management** – Switch seamlessly between multiple Xbox accounts and manage worlds, resource packs, and behavior packs.

---

## System Requirements

Before installing LeviLauncher Unlocked, ensure your device meets the following minimum specifications:

- **Operating System:** Android 9.0 (API 28) or higher
- **Device Architecture:** ARM64 (v8a)
- **RAM:** Minimum 1 GB available RAM (2 GB or more recommended)
- **Storage:** At least 2 GB of available storage for Minecraft and game data

> **Note:** For optimal performance and stability, we recommend Android 9.0 or higher with at least 3 GB of available RAM and 5 GB of free storage.

---

## Installation

### Prerequisites

You can use LeviLauncher Unlocked with:
- The official Minecraft Bedrock Edition from Google Play, **OR**
- Any installed patched/cloned version (e.g., `.patch`, `.prpatch`, `.capespatch`), **OR**
- A standalone Minecraft APK or APKS bundle imported directly into the launcher.

System installation of the official package is not mandatory if you import an APK directly.

### Installation Steps

1. Download the latest APK build from GitHub Releases or compile from source using GitHub Actions.
2. Open your device Settings and navigate to Security or Applications.
3. Enable "Allow installation from unknown sources" for your browser or file manager.
4. Locate the downloaded APK file and tap to install.
5. Grant the required permissions (including storage access and package query permissions).
6. Open LeviLauncher from your app drawer.


---

## Development Setup

If you want to build LeviLauncher from source or contribute to development, follow these steps to set up your development environment:

### Prerequisites

- Git installed on your system
- Android Studio (latest version recommended)
- Java Development Kit (JDK) 21 or higher
- Android SDK with API level 28 or higher

### Setup Instructions

1. Clone the LeviLauncher repository:

   ```bash
   git clone https://github.com/0Sombra666/LeviLaunchroidUnlocked.git
   ```

2. Open the project directory in Android Studio

3. Allow Android Studio to download and install required dependencies and build tools

4. Wait for Gradle to complete the initial sync process

5. Connect your Android device or start an emulator (API 28+)

6. Click the "Run" button in Android Studio to build and deploy to your device

7. The app will launch automatically on successful build completion

> **Build Tip:** For faster builds during development, use `Build > Make Project` to compile incrementally instead of full rebuilds.

---

## Contribution Guidelines

We welcome contributions from the community to improve LeviLauncher. To ensure a high-quality codebase and smooth collaboration, please adhere to the following guidelines:

### Code Quality

Write clean, modular code with descriptive variable names and consistent formatting. Follow Kotlin and Java style guidelines established in the project. Ensure your code is readable and well-structured for future maintainers.

### Commit Structure

Use small, focused commits with clear and descriptive messages. Each commit should address a single feature or bug fix. Example: "Fixed memory leak in version manager" or "Added support for ARM32 architecture".

### Documentation

Add comments for complex logic and update relevant documentation in the repository. If you add new features, update the README and any related documentation files.

### Performance

Optimize all additions to maintain low latency and smooth performance. Test your changes thoroughly to ensure they don't introduce lag or performance regressions.

### Testing

Test all changes on multiple devices and Android versions to ensure compatibility and stability.

### Pull Requests

Submit PRs with a detailed description of changes, including the problem solved or feature added. Reference any related issues and provide screenshots or videos if your changes affect the UI.

### Community Standards

Follow our Code of Conduct to maintain a respectful and inclusive environment. Be constructive in feedback, respect others' work, and communicate professionally with all contributors.

**Before Submitting:** Run a full build cycle and test on at least one device to minimize errors. We review all contributions promptly and appreciate your efforts to enhance LeviLauncher.

---

## Usage Guidelines

LeviLauncher is designed for players of Minecraft Bedrock Edition. Please respect the following guidelines and terms of use:

### Permitted Uses

- Modify LeviLauncher for personal gameplay and to test new features
- Create educational content (videos, tutorials, blog posts) showcasing LeviLauncher's capabilities
- Fork the repository for learning purposes or to create derivative projects, provided you comply with the Apache License 2.0
- Share your modified versions with others as long as you comply with the Apache License 2.0 terms

### Prohibited Uses

- Do not claim LeviLauncher as your own without crediting the LeviMC team and its contributors
- Do not use LeviLauncher to violate Mojang or Microsoft's user agreements

> **Disclaimer:** The authors and contributors of LeviLauncher are not responsible for bans, damages, or issues arising from the use of this software. Use it at your own risk and in accordance with Minecraft's terms of service.

For full legal details, see the LICENSE and NOTICE files in the repository.

---

## Credits & Acknowledgements

LeviLauncher would not be possible without the contributions and support of many talented individuals and organizations:

### Special Thanks To

- **LeviMC Organization** – For maintaining the LeviLauncher project and providing infrastructure support
- **Android Community** – For excellent documentation, libraries, and tools that made this launcher possible
- **Open Source Community** – For all the libraries, frameworks, and tools that power this project
- **Contributors** – A heartfelt thank you to all [contributors](https://github.com/LiteLDev/LeviLaunchroid/graphs/contributors) who have continuously improved and maintained LeviLauncher through their time and expertise

---

## Contact & Support

**Author / Team:** LeviMC Team

**Project Repository:** [https://github.com/LiteLDev/LeviLaunchroid](https://github.com/LiteLDev/LeviLaunchroid)

**Report Issues:** [GitHub Issues Page](https://github.com/LiteLDev/LeviLaunchroid/issues)

**For support and questions:** Please create an issue on the GitHub repository or contact the LeviMC team directly

---

<div align="center">

[![GitHub Release](https://img.shields.io/github/v/release/LiteLDev/LeviLaunchroid?style=flat-square&color=blue)](https://github.com/0Sombra666/LeviLaunchroidUnlocked/releases)
[![License: Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg?style=flat-square)](https://www.apache.org/licenses/LICENSE-2.0)
[![Issues](https://img.shields.io/github/issues/LiteLDev/LeviLaunchroid?style=flat-square&color=red)](https://github.com/LiteLDev/LeviLaunchroid/issues)
[![Stars](https://img.shields.io/github/stars/LiteLDev/LeviLaunchroid?style=flat-square&color=yellow)](https://github.com/LiteLDev/LeviLaunchroid)
[![Downloads](https://img.shields.io/github/downloads/LiteLDev/LeviLaunchroid/total.svg)](https://github.com/0Sombra666/LeviLaunchroidUnlocked/releases)
[![Android](https://img.shields.io/badge/Android-9.0%2B-green?style=flat-square&logo=android)](https://www.android.com/)

**Made with ❤️ by the LeviMC Community**

</div>

---

> [!NOTE]
> **Notice:** This repository is just a personal testing project. I do not have any intention or plans to update or maintain it regularly.

