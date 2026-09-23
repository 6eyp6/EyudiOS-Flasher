<p align="right">
  <a href="README.tr.md">🇹🇷 Türkçe</a> • <b>🇬🇧 English</b>
</p>

<p align="center">
  <h1 align="center">⚡ Eyudio Flasher</h1>
  <p align="center">
    <b>A Modern, Unified GUI Firmware Flasher for AVR and Espressif Microcontrollers</b>
  </p>
  <p align="center">
    <a href="https://github.com/6eyp6/EyudiOS-Flasher/releases"><img src="https://img.shields.io/github/v/release/6eyp6/EyudiOS-Flasher?style=for-the-badge&color=blue" alt="Latest Release"></a>
    <img src="https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
    <img src="https://img.shields.io/badge/UI-CustomTkinter-blueviolet?style=for-the-badge" alt="CustomTkinter">
    <img src="https://img.shields.io/badge/License-GPL--3.0-green?style=for-the-badge" alt="License">
  </p>
</p>

---

## 📌 Overview

**Eyudio Flasher** is an open-source, desktop flashing utility designed to eliminate CLI friction when burning firmware to embedded hardware. It bridges legacy AVR programmers and modern Espressif flashing toolchains into a sleek, dark-themed GUI.

No more manual terminal arguments or hunting down COM ports—plug in, select your target binary, and flash with a single click.

### Supported Toolchains & Chips
- 🔹 **AVR Core (`avrdude`):** Arduino Uno, Nano (ATmega328P), Arduino Leonardo (ATmega32U4), and Mega.
- 🔹 **Espressif Core (`esptool`):** ESP32, ESP32-S2, ESP32-S3 (including native USB JTAG/CDC targets).

---

## 📸 Interface Preview

<p align="center">
  <img src="image.png" alt="Eyudio Flasher Dashboard" width="700">
</p>

---

## ✨ Key Capabilities

- 🎨 **Modern Dark Interface:** Built with CustomTkinter for high-DPI crisp rendering.
- 🔌 **Dynamic Port Discovery:** Real-time enumeration of serial/COM ports.
- 📦 **Multi-Format Parsing:** Seamless validation for `.hex` (AVR) and `.bin` (ESP) binaries.
- ⚡ **Live Logging Console:** Streamed terminal outputs directly inside the UI for debugging.
- 🚀 **Zero-Dependency Portable Binary:** Standalone Windows `.exe` available for non-technical users.

---

## 📁 Supported Targets

| Architecture | Platform / Board | Binary Type | Default Flashing Engine |
| :--- | :--- | :--- | :--- |
| **8-bit AVR** | Uno, Nano, Leonardo, Mega | `.hex` | `avrdude` |
| **Xtensa / RISC-V** | ESP32, ESP32-S3 | `.bin` | `esptool.py` |

---

## 🚀 Quick Start

### Option A: Windows Portable (Recommended)
Download the standalone zero-install executable directly from the Releases tab:
1. Grab `EyudioFlasher.exe` from **[Releases](https://github.com/6eyp6/EyudiOS-Flasher/releases)**.
2. Connect your microcontroller via USB.
3. Launch and select your firmware file.

### Option B: Run from Source

#### Prerequisites
- Python 3.10 or higher
- System drivers for CH340 / CP210x / Native USB CDC (if required)

```bash
# Clone the repository
git clone [https://github.com/6eyp6/EyudiOS-Flasher.git](https://github.com/6eyp6/EyudiOS-Flasher.git)
cd EyudioFlasher

# Install dependencies
pip install -r requirements.txt

# Launch Application
python flasher.py
