# Awesome-Camera-Profile-Editing

# Top Camera Profile Editing Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Camera Profiling, ICC/DCP Generation & Self-Hosted Color Management*  
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Camera Profile Editing**. These tools enable photographers and color scientists to create custom camera profiles—mapping raw sensor data to accurate color—and to build ICC profiles, DCP files, and 3D LUTs that ensure consistent color across cameras, displays, and output devices.

**Examples** include Adobe DNG Profile Editor, X-Rite/Calibrite ColorChecker, DxO PhotoLab, Capture One, 3D LUT Creator, Argyll CMS, and DisplayCAL (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, avoiding per-seat or hardware-bundled software fees, and controlling the color pipeline. The open-source landscape is anchored by **Argyll CMS** (the comprehensive ICC-compatible color management system), **DisplayCAL** (the gold-standard GUI for Argyll on Linux/Windows), **dcamprof** (the command-line DCP profile maker for RawTherapee), and **colour-science** (the Python library for color science algorithms), with **rawtoaces** providing ACES-ready raw camera transforms.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

| Product | Description | Pricing | Free Tier Limit |
| :--- | :--- | :--- | :--- |
| **[Adobe DNG Profile Editor](https://helpx.adobe.com/camera-raw/digital-negative.html)** | Free utility from Adobe for creating and editing DNG camera profiles, including dual-illuminant profiles and tone curves. | **Free** (downloadable from Adobe Labs) . | **Fully free**. No account or subscription required. |
| **[X-Rite ColorChecker Camera Calibration](https://calibrite.com/)** | Software bundled with X-Rite/Calibrite ColorChecker targets for generating camera profiles. | Bundled with hardware purchases (e.g., ColorChecker Passport ~$107; ColorChecker Studio ~€599) . | **Software is free with hardware purchase**. No standalone free tier. |
| **[Calibrite ColorChecker Studio](https://calibrite.com/)** | Complete color management kit including ColorChecker target and Calibrite PROFILER software for camera, display, and printer profiling. | **~€599** (incl. VAT) for the Studio kit . UK pricing ~£519 . | No free tier. Hardware bundle only. |
| **[DxO PhotoLab](https://www.dxo.com/)** | RAW processing software with DxO Optical Modules and camera-specific color rendering, plus profile editing capabilities. | **$249.99** one-time purchase (DxO PhotoLab 10); upgrade from v8/v9 for $129.99 . | **30-day free trial** with full features . No permanent free tier. |
| **[Capture One](https://www.captureone.com/)** | Professional RAW editor with ICC profile support and camera-specific color characterization tools. | **Subscription**: ~¥63.08/month. **Perpetual license**: ~¥1,261.00 . | **30-day free trial** available. No permanent free tier. |
| **[3D LUT Creator](https://3dlutcreator.com/)** | Specialized tool for creating and editing 3D LUTs for color grading and camera profiling. | **Grading Edition**: $99. **Standard**: $199. **PRO**: $249 (PC or Mac); $299 for both platforms . | **Free trial** available. No permanent free tier. |
| **[Lumariver Profile Designer](https://www.lumariver.com/)** | Advanced DCP profile editor with full control over look tables, tone curves, and color matrices. | Quote-based; typically **€100–€200** range for individual licenses (not confirmed in search results). | Not specified in available results. |

## Open-Source GitHub Projects

- **[Argyll CMS](https://github.com/ArgyllCMS/ArgyllCMS)** [![GitHub Stars](https://img.shields.io/github/stars/ArgyllCMS/ArgyllCMS?style=social&color=white)](https://github.com/ArgyllCMS/ArgyllCMS/stargazers)  
  **The comprehensive open-source color management system.** **AGPL-3.0 licensed**. A complete ICC-compatible color management system with 40+ command-line tools covering camera profiling (`scanin`, `colprof`), display calibration (`dispcal`, `dispwin`), printer profiling (`printcal`, `printtarg`), and profile inspection (`iccdump`, `profcheck`) . **Strengths**: vendor-independent, supports virtually all colorimeters and spectrophotometers, and produces ICC profiles competitive with commercial tools. **Trade-offs**: command-line interface is intimidating for beginners—DisplayCAL provides a GUI wrapper. Best for color scientists and photographers wanting maximum control over the profiling pipeline without any licensing fees.

- **[DisplayCAL](https://github.com/eoyilmaz/displaycal-py3)** [![GitHub Stars](https://img.shields.io/github/stars/eoyilmaz/displaycal-py3?style=social&color=white)](https://github.com/eoyilmaz/displaycal-py3/stargazers)  
  **The gold-standard GUI for Argyll CMS.** **GPL-3.0 licensed**. A powerful graphical frontend for Argyll CMS that handles display calibration, profiling, and verification . **Features**: supports all major colorimeters, generates ICC/ICM profiles, loads calibration into the video LUT, and provides verification tools. **Installation**: available via most Linux distros, Flatpak (`flatpak install flathub net.displaycal.DisplayCAL`), or Windows/macOS installers . Best for users wanting Argyll's power without command-line complexity.

- **[dcamprof](https://github.com/Beep6581/dcamprof)** [![GitHub Stars](https://img.shields.io/github/stars/Beep6581/dcamprof?style=social&color=white)](https://github.com/Beep6581/dcamprof/stargazers)  
  **The command-line DCP profile maker for RawTherapee.** **GPL-3.0 licensed**. A free and open-source command-line tool for making camera profiles (DCP format) and performing tasks related to camera profiling . **Strengths**: used by the RawTherapee community for creating custom DCP profiles from ColorChecker target shots; supports advanced look tables and tone curves. **Documentation**: tutorial available on RawPedia for creating DCP profiles . Best for RawTherapee users and photographers wanting to generate DCP profiles programmatically.

- **[colour-science](https://github.com/colour-science/colour)** [![GitHub Stars](https://img.shields.io/github/stars/colour-science/colour?style=social&color=white)](https://github.com/colour-science/colour/stargazers)  
  **The Python colour science library.** **BSD-3-Clause licensed**, NumFOCUS-affiliated . Provides comprehensive algorithms and datasets for colour science—chromatic adaptation, colour appearance models, colour difference calculations, spectral up-sampling, and ACES input transforms . **Use case**: not a GUI profiling tool, but a foundational library for developers building custom camera profiling or color management applications in Python. Best for researchers and developers implementing custom color science algorithms.

- **[rawtoaces](https://github.com/AcademySoftwareFoundation/rawtoaces)** [![GitHub Stars](https://img.shields.io/github/stars/AcademySoftwareFoundation/rawtoaces?style=social&color=white)](https://github.com/AcademySoftwareFoundation/rawtoaces/stargazers)  
  **The ACES-ready raw camera transform tool.** Part of the Academy Software Foundation. Converts raw camera files to ACES using spectral sensitivity data or DNG metadata . **Latest**: v2.2.0 (July 2026) adds camera aliases, optional dependencies (Eigen/Ceres no longer required), and a custom matrix solver . Best for VFX and post-production pipelines requiring ACES-compliant camera transforms.

### Additional Strong Open-Source Options

- **Lutgen** — Rust-based CLI for generating and applying interpolated LUTs from color palettes. MIT licensed, actively maintained into 2026 . Best for creating LUTs from color schemes rather than camera profiling.
- **RawTherapee** — Full RAW processing application with built-in DCP profile support and integration with dcamprof. Best as the end-to-end RAW workflow alongside open-source profiling tools.
- **darktable** — Open-source RAW editor with built-in camera profiling and color calibration modules. Best for photographers wanting an integrated open-source RAW workflow with profiling capabilities.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- **Hardware-bundled software is not free-standing**: X-Rite/Calibrite profiling software comes with the purchase of a ColorChecker target (~$107–€599) . The software itself has no separate pricing or free tier.
- **Argyll CMS is the engine; DisplayCAL is the GUI**: neither is a drop-in replacement for Adobe DNG Profile Editor's simplicity, but together they provide comparable or superior profiling capability at zero cost .
- **dcamprof is command-line only**: while powerful for DCP generation, it requires comfort with terminal workflows. RawTherapee users may find its tutorial accessible .
- **Pricing for Lumariver Profile Designer and some commercial tools is not confirmed** in the available search results—verify on official vendor sites before budgeting.

---

**Made for photographers, color scientists, and imaging engineers building accurate color pipelines.**  
Let's make camera profiling more open, accessible, and vendor-independent.
