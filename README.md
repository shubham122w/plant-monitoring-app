# plant-monitoring-app
# 🌿 Plant Monitoring System (IoT-Based)

## 📖 Overview
The **Plant Monitoring System** is an IoT-based project designed to monitor the health and environment of plants in real-time. It uses sensors to collect data such as **soil moisture**, **temperature**, **humidity**, and **light intensity**, and sends it to a cloud platform for analysis and visualization. The system helps users ensure optimal conditions for plant growth and automates irrigation when needed.

---

## 🚀 Features
- 🌱 Real-time monitoring of plant conditions.
- 💧 Automatic irrigation based on soil moisture levels.
- ☀️ Light intensity monitoring for better growth conditions.
- 📊 Data visualization on cloud dashboard or web app.
- 🔔 Alerts/notifications when parameters go beyond threshold.
- 🔌 Low power consumption with ESP32/NodeMCU microcontroller.

---

## 🧠 Components Used
| Component | Description |
|------------|-------------|
| **Microcontroller** | ESP32 / NodeMCU (ESP8266) |
| **Soil Moisture Sensor** | Measures soil water content |
| **DHT11 / DHT22 Sensor** | Measures temperature and humidity |
| **LDR Sensor** | Measures light intensity |
| **Relay Module** | Controls the water pump |
| **Water Pump** | Used for irrigation |
| **Power Supply** | 5V DC |
| **Wi-Fi Module** | Built-in (ESP32/ESP8266) |

---

## 🔧 Working Principle
1. The sensors continuously measure environmental parameters.
2. Data is sent to the microcontroller.
3. The microcontroller processes the data and:
   - Sends it to a **cloud platform** (like ThingSpeak, Blynk, or Firebase) for monitoring.
   - Turns on the **water pump** if soil moisture falls below a certain level.
4. The user can view the live data and history on the dashboard.

---

## ☁️ Cloud Integration (Example: ThingSpeak / Blynk)
- The ESP32/NodeMCU sends sensor data to a cloud service using **HTTP/MQTT protocols**.
- The user can visualize graphs, monitor conditions, and control the system remotely.

---

## 🖥️ Software Requirements
- **Arduino IDE** (for programming the microcontroller)
- **Blynk / ThingSpeak / Firebase** (for IoT dashboard)
- **Drivers for ESP32 or NodeMCU**
- **Wi-Fi Connection**

---

## ⚙️ Installation & Setup
1. **Connect hardware components** as per the circuit diagram.
2. **Open Arduino IDE** and install the following libraries:
   - `DHT.h`
   - `ESP8266WiFi.h` or `WiFi.h` (for ESP32)
   - `ThingSpeak.h` or `BlynkSimpleEsp8266.h`
3. **Enter Wi-Fi credentials** and API keys in the code.
4. **Upload code** to ESP32/NodeMCU.
5. **Open dashboard** (ThingSpeak/Blynk) to view live updates.

---

## 🧩 Circuit Connections
| Sensor | ESP32/NodeMCU Pin |
|---------|------------------|
| Soil Moisture | A0 |
| DHT11 / DHT22 | D4 |
| LDR | A0 (through voltage divider) |
| Relay IN | D5 |
| Pump | Connected to relay output |

---

## 📈 Output
- Displays **real-time readings** on the IoT dashboard.
- Automatically activates pump when soil is dry.
- Sends **alerts** for abnormal environmental conditions.

---

