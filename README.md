# 🚀 Raspberry Pi RS485 & Power HAT for OpenPLC
This repository contains the design files and documentation for a custom Raspberry Pi HAT specifically engineered for industrial automation. 
By combining a **high-quality RS485 transceiver** with a **ruggedized power supply**, this board transforms a standard Raspberry Pi into a Modbus-capable PLC (Programmable Logic Controller) ready for **OpenPLC** runtime.
![20260221_133352](https://github.com/user-attachments/assets/7865b642-ac1f-4ac6-a047-c1b632ad7eb4)

## 🛠 Key Features
* **Integrated RS485 Transceiver**: Enables seamless Modbus RTU communication for interfacing with industrial sensors, VFDs, and meters.
* **Onboard Power Supply**: A wide-input voltage regulator allowing you to power both the Pi and the HAT directly from industrial 12V or 24V DC rails.
* OpenPLC Optimized: Pinout and timing tuned for low-latency execution of Ladder Logic and Structured Text.Standard HAT Form Factor: Snaps directly onto the 40-pin GPIO header.

## 📂 Project Contents
* Schematics: Detailed circuit diagrams including the transceiver isolation and buck converter stages.
  <img width="884" height="885" alt="image" src="https://github.com/user-attachments/assets/90bff432-cefd-410c-8198-6fb4b9c6ffca" />

* Bill of Materials (BOM): Links to the specific modules used in this build.
* Prototype: Photos of the Rev 1.0 hardware in action.
  ![20260221_133056](https://github.com/user-attachments/assets/ffbc4e4b-a593-4a57-bf8d-71df62d40c7d)

## 🔧 Hardware Breakdown
| Component | Function |Link |
| ------------- | ------------- | ------------- |
| RS485 Module | Signal conversion for Modbus RTU | [[Link to Module]](https://s.click.aliexpress.com/e/_c3xQa1XV) |
| DC-DC Converter | 24V to 5V Step-down | [[Link to Module]](https://s.click.aliexpress.com/e/_c3xQa1XV) |
| Modbus IO module | RS485 Slave | [[Link to Module]](https://s.click.aliexpress.com/e/_c3Pnotx9) |

## 🚦 Quick Start with OpenPLCHardware Setup: 
1. Mount the HAT and connect your 24V DC supply.
2. Software: Install the OpenPLC Runtime on your Raspberry Pi.
3. Configuration: In the OpenPLC web interface, set the RS485 serial port (usually /dev/ttyS0 or /dev/ttyAMA0) to match your Modbus slave devices.
4. Deploy: Upload your logic and start the hardware cycle!
  **Note:** Ensure your RS485 A/B lines are correctly polarized. If communication fails, the first step is usually swapping the A and B wires!

## 🔗 Links
* [OppenPLC project](https://autonomylogic.com/)
* [RaspberryPI DIN rail mount](https://www.thingiverse.com/thing:2659908)
