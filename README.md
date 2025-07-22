# 🗑️ Smart Trash Management System using STM32

This project implements a **Smart Dustbin** using the STM32F407G microcontroller to promote **contactless, hygienic waste disposal**. It uses an IR sensor to detect user presence, a servo motor to open the lid, and an ultrasonic sensor to monitor trash levels. The system automates waste collection and prevents overflow, contributing to smart city infrastructure.

> Developed under Project-Based Learning – RV College of Engineering (2024)

---

## 🎯 Objectives

- Automate the opening and closing of a dustbin lid using sensors and STM32.
- Prevent the dustbin from operating if it is full.
- Use STM32CubeMX + HAL drivers for modular embedded programming.
- Promote cleaner and smarter waste disposal in public areas.

---

## 🧠 Working Principle

The system operates based on **real-time sensor feedback** processed by STM32:

- **IR Sensor (LM393)** detects human presence.
- **Ultrasonic Sensor (HC-SR04)** checks the trash level.
- **STM32F407G** processes sensor data and controls:
  - **Servo Motor (SG90)** via PWM to open/close the lid accordingly.

---

## 🔄 Algorithm Summary

1. Initialize STM32 peripherals (GPIOs, Timer4 for PWM).
2. Read IR sensor to detect presence.
3. Measure bin fill level with ultrasonic sensor.
4. Control servo angle:
   - **90°** – Open lid if user detected
   - **0°** – Keep lid closed if bin is full
   - **45°** – Idle state
5. Loop every 200 ms for smooth, stable operation.

---

## ⚙️ Components Used

| Component         | Description                            |
|------------------|----------------------------------------|
| STM32F407G-DISC1 | Microcontroller board                  |
| IR Sensor (LM393)| Detects human proximity                |
| Ultrasonic Sensor| Measures bin fill distance             |
| Servo Motor (SG90)| Controls lid rotation (PWM)           |
| Breadboard & Wires| For connections and prototyping        |
| External Power    | 5V source to power servo independently |

---

## 🔌 Circuit Connections

### IR Sensor:
- **VCC** → 5V  
- **GND** → GND  
- **OUT** → `PA0` (GPIO Input)

### Ultrasonic Sensor:
- **VCC** → 5V  
- **GND** → GND  
- **Trigger** → `PC0` (GPIO Output)  
- **Echo** → `PC1` (GPIO Input)

### Servo Motor:
- **VCC** → 5V (external)
- **GND** → GND
- **Signal** → `PB6` (TIM4 Channel 1 – PWM)

---

## 📐 Architecture Diagram




[Smart Dustbin](pic.jpg)


---

## 📄 Documentation



[PPT](PPT.pdf)


---

## ✅ Key Features

- 💡 Automatic lid control via IR and ultrasonic sensing
- 🤖 Real-time embedded control with STM32 HAL
- 🔋 External power for uninterrupted servo operation
- 🌐 Promotes smart, hygienic public waste handling

---

## 🚀 Future Improvements

- Add BLE or Wi-Fi module for remote trash level updates
- Solar power integration for off-grid operation
- Integration with central waste management dashboard
- Use of OLED/LCD to show real-time fill level

---

## 👨‍💻 Contributors

  
- Preetham V  
- Shiven Singh  
- Sneha Pandey

---

## 📬 Contact

- Email: preethamv.et23@rvce.edu.in  
- GitHub: [github.com/preethamv6](https://github.com/preethamv6)

---

> “Automating hygiene, one lid at a time.” ♻️
