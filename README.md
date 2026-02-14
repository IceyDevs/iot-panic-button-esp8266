# IoT Panic Button using NodeMCU (ESP8266)

## Overview

The IoT Panic Button is a low-cost, Wi-Fi-enabled emergency alert system developed using the NodeMCU ESP8266 microcontroller. When a physical push button is pressed, the system activates a local buzzer and sends a real-time alert notification through the Blynk IoT platform.

This project demonstrates the practical integration of embedded systems with cloud-based IoT services for real-time communication and emergency response applications.

---

## Objectives

- Design an IoT-based emergency alert system using ESP8266.
- Establish real-time communication between hardware and a smartphone.
- Develop a portable and cost-effective safety device.
- Implement event-based notification using the Blynk IoT platform.

---

## System Architecture

Push Button → NodeMCU (ESP8266) → Wi-Fi → Blynk Cloud → Smartphone Notification  
                                    │  
                                    └── Local Buzzer Alert  

---

## Hardware Components

- NodeMCU ESP8266
- Push Button (Momentary Switch)
- Active Buzzer
- 10kΩ Resistor
- Breadboard
- Jumper Wires
- USB Cable (Power and Programming)

---

## Software Requirements

- Arduino IDE
- ESP8266 Board Package
- Blynk Library for Arduino
- Blynk IoT Mobile App
- Active Wi-Fi Connection

---

## Pin Configuration

| Component    | NodeMCU Pin | GPIO  |
|--------------|------------|--------|
| Push Button  | D2         | GPIO4  |
| Buzzer       | D5         | GPIO14 |

- The push button is configured using `INPUT_PULLUP`.
- The buzzer is configured as a digital output.
- All components share a common ground.

---

## Working Principle

1. The NodeMCU connects to the configured Wi-Fi network.
2. The system initializes and waits for user input.
3. When the push button is pressed:
   - The buzzer activates briefly to provide audible feedback.
   - A message is printed on the serial monitor.
   - An event is triggered in the Blynk cloud for notification delivery.

---

## Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/iot-panic-button-esp8266.git
```

### 2. Arduino IDE Configuration

- Install the ESP8266 board package.
- Install the Blynk library.
- Select "NodeMCU 1.0 (ESP-12E Module)" as the board.
- Set the baud rate to 9600.

### 3. Update Credentials

Before uploading the code, update the following fields:

```cpp
#define BLYNK_AUTH_TOKEN "YOUR_AUTH_TOKEN"
char ssid[] = "YOUR_WIFI_NAME";
char pass[] = "YOUR_WIFI_PASSWORD";
```

### 4. Upload the Code

- Connect the NodeMCU via USB.
- Select the correct COM port.
- Upload the sketch.
- Open Serial Monitor to verify connection.

---

## Applications

- Personal safety emergency device
- Assistance system for elderly individuals
- School or office emergency alert system
- Industrial safety signaling
- Home security alert system

---

## Advantages

- Low-cost implementation
- Simple hardware design
- Real-time cloud connectivity
- Portable and scalable
- Easy to customize for various applications

---

## Limitations

- Requires a stable Wi-Fi connection
- Dependent on internet availability
- Basic system without location tracking

---

## Future Enhancements

- Integration of GPS module for location-based alerts
- Addition of GSM module (SIM800L) for SMS-based backup alerts
- Support for multiple panic buttons with unique identifiers
- Battery-powered portable enclosure
- Offline fallback alert mechanism

---

## License

This project is open-source and available under the MIT License.

---

## Author

Your Name  
GitHub: https://github.com/yourusername
