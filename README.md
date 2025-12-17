# H81MD-GT630Kepler-Hackintosh
EFI configurations for Hackintosh systems using a **Kepler GK208 GPU** and **4th Gen Intel (Haswell)** processors on an **ASUS motherboard**.

**Codename:** ONYX COPPER III

---

# Hackintosh Build – iMacPro1,1 (OpenCore)

## 🖥️ System Overview
This repository contains tested **EFI folders** and documentation for running macOS on legacy Haswell hardware using **OpenCore** with an **iMacPro1,1 SMBIOS**.

The setup focuses on **Kepler GPU compatibility**, offering both **native** and **patched** solutions depending on the macOS version.

---

## ⚙️ Hardware Specifications

| Component | Details |
|---------|--------|
| **SMBIOS** | iMacPro1,1 |
| **Motherboard** | ASUS H81M-D |
| **CPU** | Intel Core i5-4460 @ 3.20 GHz (Haswell) |
| **GPU** | Inno3D GeForce GT 630 (GK208 – Kepler) |
| **Memory** | 8 GB DDR3-1600 |
| **BIOS Version** | 3602 |

---

## 🎮 Graphics Information
- GPU is **Kepler-based (GK208)**
- **Native graphics support up to macOS Big Sur**
- Native support removed starting **macOS Ventura**
- **OpenCore Legacy Patcher (OCLP)** is required for:
  - macOS Ventura (13)
  - macOS Sonoma (14)
  - macOS Sequoia (15)
- HDMI flickering may occur  
  - **DVI is recommended as the primary display**
  - Flicker mitigation is applied via **boot-args**

---

## 🧠 SMBIOS Choice
**iMacPro1,1** was selected for:
- Improved compatibility with newer macOS versions
- Stable power management
- Avoidance of iGPU conflicts (dGPU-only configuration)

---

## 🛠️ Bootloader
- **OpenCore**
- Configured for legacy-compatible ASUS BIOS
- **Post-install root patching via OCLP** is required for newer macOS versions

---

## 📦 EFI Layout & macOS Support

### EFI – Big Sur
- **Purpose:** Installer and daily-use EFI
- **Supported macOS:**  
  - macOS Big Sur (11.x)
- **Notes:**
  - Suitable for daily use, though some modern applications may no longer support Big Sur
  - **No Kepler patching required** — GK208 GPUs have **native support**
  - Recommended for users who prefer maximum stability on legacy Kepler hardware

---

### EFI – Monterey to Sequoia
- **Purpose:** Installer and daily-use EFI
- **Supported macOS:**
  - macOS Monterey (12.x)
  - macOS Ventura (13.x)
  - macOS Sonoma (14.x) *(OCLP patched)*
  - macOS Sequoia (15.x) *(OCLP patched)*
- **Notes:**
  - Requires **OpenCore Legacy Patcher** post-install root patches
  - Hardware acceleration is unavailable until patching is completed
  - macOS updates may require re-patching

---

## ✅ Known Working
- Hardware acceleration *(native on Big Sur, patched on newer macOS)*
- Audio
- Ethernet
- USB mapping
- Sleep / Wake *(BIOS-dependent)*

---

## ⚠️ Known Issues
- HDMI display flickering on Kepler GPUs
- No native graphics support beyond Big Sur
- Limited UEFI functionality due to legacy BIOS
- Secure Boot disabled

---

## 📌 Notes
- Configure **CSM** according to ASUS H81M-D BIOS behavior
- `SecureBootModel` is disabled for patched macOS
- Intended for **educational, experimental, and legacy hardware use**

---

## 📄 Disclaimer
This project is **not affiliated with Apple Inc.**  
macOS is the property of Apple Inc.  
Use at your own risk and ensure compliance with Apple’s EULA.

---

**Maintained by:** Michael Ordenes  
**Build Type:** Legacy Haswell + Kepler Hackintosh  
**Codename:** ONYX COPPER III
