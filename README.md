# 🌡️ DHT22 Sensor – Temperature & Humidity Monitoring
## 📌 Overview
The DHT22 is a digital sensor used for measuring temperature and humidity with higher accuracy and wider range compared to basic environmental sensors.
It is commonly used in IoT systems, smart agriculture, weather stations, indoor monitoring systems, and climate control applications.
This repository explores the internal working mechanism, sensing methodology, ESP32 interfacing, and real-world engineering applications of the DHT22 sensor.
## 🧠 Working Principle
The DHT22 combines two sensing components:
* Capacitive humidity sensing element
* Thermistor-based temperature sensing element
The internal microcontroller processes the sensor data and sends calibrated digital output to the microcontroller.
## ⚙️ Humidity Sensing Mechanism
The humidity sensor operates using capacitive sensing.
### 🔹 Principle:
When humidity changes, the dielectric constant of the sensing material changes, causing variation in capacitance.
The sensor converts this capacitance variation into digital humidity values.
## 🌡️ Temperature Sensing Mechanism
Temperature is measured using an NTC thermistor.
### 🔹 Working:
* Resistance decreases as temperature increases
* Internal ADC converts analog variation into digital temperature values
## 🔌 Pin Configuration
The DHT22 typically contains:
* VCC → Power supply
* DATA → Digital communication pin
* NC → No connection
* GND → Ground
## 📡 Digital Communication Protocol
DHT22 uses a single-wire serial communication protocol.
### 🔹 Communication Flow:
1. ESP32 sends start signal
2. DHT22 responds with acknowledgment
3. Sensor transmits 40-bit data packet
4. Data includes humidity, temperature, and checksum
## ⚙️ ESP32 Interfacing
ESP32 communicates with DHT22 using GPIO pins.
