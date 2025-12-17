# H81MD-GT630Kepler-Hackintosh
EFI for Hackintosh that supports GK208 Kepler with 4th Gen Intel processor with an ASUS motherboard.

# Hackintosh Build – iMacPro1,1 (OpenCore)

## 🖥️ System Overview
This repository contains the configuration and notes for a **Hackintosh system** running macOS using **OpenCore** with an **iMacPro1,1 SMBIOS**.

## ⚙️ Hardware Specifications

| Component | Details |
|---------|--------|
| **SMBIOS** | iMacPro1,1 |
| **CPU** | Intel Core i5-4460 @ 3.20 GHz (Haswell) |
| **GPU** | Inno3D GeForce GT 630 (GK208 – Kepler) |
| **Memory** | 8 GB DDR3-1600 |
| **BIOS Version** | 3602 |

## 🎮 Graphics Information
- GPU is **Kepler-based (GK208)**  
- Native support removed in macOS Ventura and newer  
- Requires **OpenCore Legacy Patcher (OCLP)** for Sonoma and later  
- HDMI may cause flickering; DVI is recommended as the primary display (patched using bootargs)

## 🧠 SMBIOS Choice
**iMacPro1,1** was selected for:
- Better compatibility with newer macOS versions
- Stable power management
- Avoiding iGPU-related issues (system runs dGPU-only)

## 🛠️ Bootloader
- **OpenCore** (with Legacy/CSM-aware configuration if required)
- Patched using **OpenCore Legacy Patcher** for Kepler GPU support

## 📦 Known Working
- macOS Sonoma (14.x) *(patched via OCLP)*
- Hardware acceleration (after post-install patch)
- Sleep/Wake *(may vary by BIOS settings)*

## ⚠️ Known Issues
- HDMI display flicker (use DVI where possible)
- No native Kepler support without OCLP patches
- BIOS limitations on older boards

## 📌 Notes
- Ensure **CSM is properly configured** depending on motherboard support
- SecureBootModel is typically disabled for patched systems
- This setup is intended for **educational and experimental purposes**

## 📄 Disclaimer
This project is **not affiliated with Apple**.  
macOS is the property of Apple Inc.  
Use at your own risk and comply with Apple’s EULA.

---

**Maintained by:** Michael Ordenes  
**Build Type:** Legacy Haswell + Kepler Hackintosh
