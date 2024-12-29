# Dell G3 3500 Hackintosh EFI - Dual Boot macOS & Windows

This repository contains the EFI configuration files for setting up a dual boot on the Dell G3 3500 with macOS (Hackintosh using OpenCore) and Windows 11. This configuration ensures maximum compatibility with the Dell G3 3500 hardware and provides a stable environment for daily use.

---

## ⚠️ Important Notice

- This repository is provided for educational and reference purposes only.
- Creating a Hackintosh may violate Apple's Terms of Service.
- Proceed at your own risk. I am not responsible for any hardware damage, data loss, or other issues.

---

## 📋 System Specifications

- **Laptop Model:** Dell G3 3500
- **CPU:** Intel Core i7-10750H
- **GPU:** Intel UHD Graphics 630 and NVIDIA GTX 1660 (unsupported on macOS)
- **RAM:** 16GB DDR4
- **Storage:**
  - 512GB NVMe SSD (macOS Sequoia)
  - 1TB NVMe SSD (Windows 11)
- **Wi-Fi and Bluetooth:** Fenvi BCM94360NG (native on macOS with OpenCore Legacy Patcher post-installation)

---

## 🎯 Repository Purpose

- Share a functional EFI configuration for dual boot on the Dell G3 3500.
- Assist users with similar hardware in installing and configuring macOS and Windows on separate SSDs.
- Document the steps required to ensure a stable and functional system.

---

## 📁 Repository Structure

- **/BOOT:** Essential boot files.
- **/Dell:** Dell-specific hardware configurations.
- **/Microsoft:** Windows-related files.
- **/OC:** OpenCore configuration files (version 1.0.2).
- **README.md:** This file.

---

## 🔧 Configurations Applied

### 1. **OpenCore Bootloader**

- Version: **1.0.2**
- Compatible with:
  - macOS Sequoia
  - Windows 11

### 2. **Dual Boot**

- macOS and Windows installed on separate NVMe SSDs.
- Configured to boot both systems via OpenCore.

### 3. **Kexts Used**

The following kexts were included to ensure hardware compatibility on macOS:

- **AMFIPass.kext**
- **AppleALC.kext**
- **AtherosE2200Ethernet.kext**
- **BlueToolFixup.kext**
- **CPUFriend.kext**
- **CPUFriendDataProvider.kext**
- **IO80211FamilyLegacy.kext**
- **IOSkywalkFamily.kext**
- **Lilu.kext**
- **RealtekRTL8111.kext**
- **RestrictEvents.kext**
- **SMCBatteryManager.kext**
- **SMCDellSensors.kext**
- **SMCLightSensor.kext**
- **SMCProcessor.kext**
- **SMCSuperIO.kext**
- **USBPorts.kext**
- **VirtualSMC.kext**
- **VoodooI2C.kext**
- **VoodooI2CHID.kext**
- **VoodooPS2Controller.kext**
- **WhateverGreen.kext**

---

## 🚀 Post-Installation

### Enabling Wi-Fi on macOS

To ensure Wi-Fi functionality, use the [OpenCore Legacy Patcher](https://github.com/dortania/OpenCore-Legacy-Patcher/releases/tag/2.2.0).

1. Download version **2.2.0** of OpenCore Legacy Patcher.
2. Apply the patch to enable compatibility with the BCM94360NG adapter.
3. Restart the system.

---

## 🛠️ Requirements and Setup Steps

### Prerequisites

1. Basic knowledge of Hackintosh and OpenCore.
2. Full backup of all important data.
3. A USB drive with at least 16GB to create the macOS installer.

### Installation

1. Copy the `EFI` folder to the EFI partition of the installation USB drive.
2. Follow the OpenCore installation guide to set up macOS on the 512GB SSD.
3. After installation, copy the `EFI` folder again to the macOS SSD.
4. Configure dual boot in BIOS to boot via OpenCore.

---

## ⚙️ Troubleshooting

1. **Wi-Fi not detected on macOS:** Ensure the OpenCore Legacy Patcher patch is applied.
2. **macOS fails to boot:** Verify that the kexts are up-to-date and the `config.plist` is correctly configured for the hardware.
3. **Dual boot not showing up:** Ensure OpenCore is set as the primary bootloader and the correct entries are listed.

---

## 🤝 Contributions

Contributions are welcome! If you have improvements or suggestions, feel free to open a pull request or report issues in the issues section.

---

## 📜 License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

---

## 📬 Contact

Have questions or suggestions? Reach out by opening an issue in this repository.
