# 🗑️ Smart Trash Level Monitor

🚀 **An Arduino-based ultrasonic sensor system that monitors trash bin levels and displays the fill percentage on an LCD.**

## 📌 Project Overview
This project uses 3 **HC-SR04 ultrasonic sensors** to measure the height of trash inside a bin. The **Arduino** processes the sensor data, calculates the fill percentage, and displays it on a **LiquidCrystal I2C LCD screen**. Additionally, it logs the readings to the **Serial Monitor** for real-time debugging.

## 🎯 Features
✅ **Real-time trash level detection** using ultrasonic sensors  
✅ **LCD display output** showing trash bin fill percentage  
✅ **Serial Monitor logging** for debugging and calibration  
✅ **Simple and efficient calculation method** for accurate level readings  
✅ **Modular and expandable** (can integrate WiFi/Bluetooth for remote monitoring)  

## 🔧 Hardware Components
- 💥 **Arduino Uno** (or any compatible board)
- 💿 **16x2 I2C LCD Display**
- 🛁 **3 HC-SR04 Ultrasonic Sensors**
- 🔌 **Jumper Wires**
- 🔋 **Power Supply**

## 📜 How It Works
1. The **HC-SR04 ultrasonic sensors** measure the distance from the sensors to the top of the trash. Each sensor outputs travel time in microseconds, which is averaged to determine the space remaining in the trash bin.
2. The average distance is converted into **inches and centimeters**.
3. The fill percentage is calculated using:
   ```cpp
   trash = ((132.0 - inches) / (132.0 - 2.0)) * 100.0;
   ```
   - `132 inches` → Bin is **empty** (0%)
   - `2 inches` → Bin is **full** (100%)
4. The fill percentage is displayed on the **LCD screen** and printed to the **Serial Monitor**.
5. The system updates every **2 seconds** for continuous monitoring.

## 🛠️ Installation & Setup

### == 1️⃣ Wiring Instructions ==

| Component              | Arduino Pin |
|------------------------|--------------|
| (1) HC-SR04 Trigger    | 6            |
| (1) HC-SR04 Echo       | 7            |
| (2) HC-SR04 Trigger    | 8            |
| (2) HC-SR04 Echo       | 9            |
| (3) HC-SR04 Trigger    | 10           |
| (3) HC-SR04 Echo       | 11           |
| LCD SDA                | A4           |
| LCD SCL                | A5           |

### == 2️⃣ Uploading the Code ==

1. Install **Arduino IDE** (if not already installed).
2. Install the required library for **I2C LCD**:
   - Open **Arduino IDE** → Go to **Sketch** → **Include Library** → **Manage Libraries**.
   - Search for **LiquidCrystal_I2C** and install it.
3. Connect the **Arduino via USB**.
4. Upload the code in `smart_trash_monitor.ino`.
5. Open the **Serial Monitor** (`9600 baud`) to see live readings.

## 📸 Project Demo

[Wokwi Simulation](https://wokwi.com/projects/426241176392974337)

![Demo Image](https://github.com/user-attachments/assets/858a351e-c14b-46f9-acb2-a371c10d11b7)

---

## 🚀 Future Improvements

- 📡 **IoT Integration** → Send data to a cloud platform for remote monitoring.
- 🔔 **Alert System** → Add buzzer or LED to notify when the bin is full.

---

## 🏆 Author

**👨‍💻 Steven Reynoso**  
🔗 GitHub: [github.com/StevenReynoso](https://github.com/StevenReynoso)  
📧 Contact: sreynosowork@gmail.com

