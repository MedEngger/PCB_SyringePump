# 💉 PCB_SyringePump

[![License: Unlicense](https://img.shields.io/badge/license-Unlicense-blue.svg)](http://unlicense.org/)

An open-source **Syringe Pump PCB** designed for precision fluid control. This project is built around the **Teensy 3.2** microcontroller and features robust power management, user inputs, and motor driver connectivity.

📂 **Repository:** [https://github.com/MedEngger/PCB_SyringePump](https://github.com/MedEngger/PCB_SyringePump)

---

## 📖 Overview

This repository contains the KiCad PCB design files for a standalone syringe pump driver. The board integrates a high-performance microcontroller with a dedicated power supply circuit, rotary encoder interface, and tactile buttons for a complete user interface.

## ⚡ Key Features

* **🧠 Microcontroller:**
    * Designed for the **Teensy 3.2** platform (Footprint `U1`).
* **🔋 Power System:**
    * **Input Voltage:** +12V to 24V DC via Barrel Jack (`J1`).
    * **Isolation/Regulation:** Murata **NCS1S2405SC** DC-DC Converter (`T1`) for stable logic power.
    * **Protection:**
        * Reverse Polarity Protection using **FQP47P06** P-Channel MOSFET (`Q1`).
        * **2A Fast Blow Fuse** (`XF1`) and **500mA PTC Fuse** (`F1`) for overcurrent safety.
    * **Zener Regulation:** 10V Zener Diode (`D1`) for voltage clamping.
* **🎛️ User Interface:**
    * **Rotary Encoder:** Bourns **PEC11R** (`ENC1`) for menu navigation and flow adjustment.
    * **Controls:** 3x Tactile Switches (`S1`, `S2`, `S3`) for Start, Stop, and Mode selection.
* **🔌 Connectivity:**
    * **Motor/Sensor Ports:** TE Connectivity style Terminal Blocks (2.54mm pitch).
        * 10-Pin (`XJ1`), 6-Pin (`XJ3`), 4-Pin (`XJ2`), and 2-Pin (`XJ4`) connectors.

## 🧩 Bill of Materials (Highlights)

| Component | Description | Designator |
| :--- | :--- | :--- |
| **MCU** | Teensy 3.2 Development Board | `U1` |
| **Power Jack** | CUI PJ-079AH (+12-24V) | `J1` |
| **DC-DC Conv** | Murata NCS1S2405SC | `T1` |
| **MOSFET** | FQP47P06 (P-Channel) | `Q1` |
| **Fuse** | Littlefuse 2AG (2A Fast Blow) | `XF1` |
| **PTC Fuse** | 500mA Resettable Fuse | `F1` |
| **Encoder** | Bourns PEC11R Series | `ENC1` |
| **Buttons** | Alps SKRGAFD010 Tactile Switches | `S1`, `S2`, `S3` |
| **Capacitors** | 100µF Electrolytic, 10µF Tantalum, 1µF Ceramic | `C1`, `C4`, `C2/C3` |

## 🛠️ Software & Tools

* **PCB Design:** KiCad EDA (Generator Version: 9.0)
* **File:** `SyringePump.kicad_pcb`

## 👥 Credits

* **👨‍💻 Created By:** [ManoMedEngg](https://github.com/ManoMedEngg)
* **🏢 Organization:** [MedEngger](https://github.com/MedEngger)

---

## 📜 License

This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or distribute this software, either in source code form or as a compiled binary, for any purpose, commercial or non-commercial, and by any means.

For more information, please refer to <https://unlicense.org>