# Smart Air Conditioner Control Dashboard

A web-based IoT Air Conditioner Control System powered by **ESP32**, **Firebase Realtime Database**, and **DHT22**. The system allows users to remotely control air conditioners through a web dashboard while monitoring real-time temperature and humidity.

---

## Features

- Remote Air Conditioner ON/OFF Control
- Real-time Relay Status
- Live Temperature Monitoring (DHT22)
- Live Humidity Monitoring (DHT22)
- Firebase Realtime Database Integration
- Firebase Authentication Login
- Responsive Web Dashboard
- Manual Push Button Override
- ESP32 Wi-Fi Connectivity

---

## Hardware Requirements

- ESP32 Development Board
- 2-Channel Relay Module
- DHT22 Temperature & Humidity Sensor
- Push Buttons (2)
- Air Conditioner
- 5V Power Supply
- Jumper Wires

---

## Software Requirements

- Arduino IDE
- Firebase Realtime Database
- Firebase Authentication
- HTML
- CSS
- JavaScript
- Firebase SDK
- ESP32 Board Package

---

## Arduino Libraries

Install the following libraries before uploading the ESP32 sketch.

- Firebase ESP Client
- AceButton
- DHT Sensor Library
- Adafruit Unified Sensor

---

## GPIO Connections

| Device | ESP32 GPIO |
|---------|------------|
| Relay 1 | GPIO 23 |
| Relay 2 | GPIO 19 |
| DHT22 Data | GPIO 26 |
| Switch 1 | GPIO 13 |
| Switch 2 | GPIO 12 |

### DHT22 Wiring

| DHT22 Pin | ESP32 |
|------------|-------|
| VCC | 3.3V |
| GND | GND |
| DATA | GPIO26 |

> If using a bare DHT22 sensor, connect a 10kΩ pull-up resistor between DATA and 3.3V.

---

## Firebase Database Structure

```json
{
  "relay1": false,
  "relay2": false,
  "temperature": 27.8,
  "humidity": 71.5
}
```

---

## Project Structure

```
Smart-AirConditioner-Control/
│
├── index.html
├── README.md
├── esp32_aircon_controller.ino
├── images/
│   ├── dashboard.png
│   └── wiring.png
└── assets/
```

---

## Dashboard

The web dashboard provides:

- Secure Login
- Relay 1 Control
- Relay 2 Control
- Live Temperature Display
- Live Humidity Display
- All OFF Button
- Logout

---

## How It Works

1. The ESP32 connects to the configured Wi-Fi network.
2. The ESP32 authenticates with Firebase.
3. The dashboard authenticates using Firebase Authentication.
4. Relay states are synchronized through Firebase Realtime Database.
5. The DHT22 sensor continuously measures temperature and humidity.
6. Sensor readings are uploaded to Firebase.
7. The web dashboard updates automatically in real time.

---

## Technologies Used

- ESP32
- Firebase Realtime Database
- Firebase Authentication
- HTML5
- CSS3
- JavaScript
- Arduino
- DHT22 Sensor

---

## Future Improvements

- Air conditioner scheduling
- Mobile application
- Power consumption monitoring
- Historical temperature charts
- Notifications and alerts
- Multiple air conditioner support
- Role-based user accounts

---

## Author

**Alexander S. Laggui**

Bachelor of Science in Information Technology

---

## License

This project is intended for educational and personal use.
