---

#  IoT-Based Web Controlled Rover with Embedded Web Server (ESP32)

## Project Overview

This project demonstrates a simple **IoT-controlled rover** powered by **ESP32**. The rover is controlled via a **web-based interface** hosted directly on the ESP32's internal HTTP server. The setup leverages **WiFiManager** for flexible Wi-Fi network configuration and **mDNS** (`esp32.local`) for convenient, user-friendly access.

Users can control the vehicle’s movement (Forward, Backward, Left, Right, Stop) through any device connected to the same network via a browser.

---

## Technologies & Tools

* **ESP32 Microcontroller**
* **Arduino IDE / ESP-IDF**
* **WiFiManager Library** (for dynamic Wi-Fi provisioning)
* **ESP32 WebServer Library** (HTTP server)
* **mDNS (esp32.local)** for DNS-like access on local network
* **HTML / CSS / JavaScript** (for the browser-based control panel)
* **DC Motor Driver (H-Bridge)** for motor control (L298N / L293D)

---

## Features

✅ Web interface hosted directly on ESP32
✅ Mobile / Desktop browser control
✅ No external apps required
✅ Real-time directional commands: Forward, Backward, Left, Right, Stop
✅ WiFiManager-based dynamic network configuration
✅ mDNS (`esp32.local`) for easy access without IP lookup

---

## User Interface (Screenshot)
https://github.com/harshal061/IoT_Based_Web_Controlled_Rover_with_Embedded_Web_Server_ESP32/blob/8a73a095685791e6fd9e8443607dc8b72d5e9fce/Screenshot%202025-07-13%20225528.png




---

## Project Architecture

```plaintext
Client Device (Phone / PC)
        |
     Browser (HTML/JS)
        |
     HTTP Requests
        |
     ESP32 WebServer (mDNS: esp32.local)
        |
 Motor Control (GPIO Pins -> Motor Driver)
```

---

## 🚀 How to Run

### 1️⃣ Hardware Setup

* ESP32 Development Board
* L298N / L293D Motor Driver Module
* 2 DC Motors (for differential drive)
* Power Supply (Battery)

### 2️⃣ Software Setup

* Install **Arduino IDE**
* Install **ESP32 Board Packages**
* Install Libraries:(essential)

  * `WiFiManager`
  * `ESPmDNS`
  * `WebServer`

### 3️⃣ Upload the Code

* Flash the provided code via Arduino IDE.
* On first boot, connect to **ESP32-Config** Wi-Fi to configure your home Wi-Fi.

### 4️⃣ Access the Control Panel

* Open browser → Visit: **[http://esp32.local](http://esp32.local)** (after successful pairing)
* Use on-screen buttons to control the rover.

---

##  Control Interface

| Action   | HTTP Endpoint |
| -------- | ------------- |
| Forward  | `/forward`    |
| Backward | `/backward`   |
| Left     | `/left`       |
| Right    | `/right`      |
| Stop     | `/stop`       |

---

## Learning Outcomes

* Embedded HTTP server deployment
* IoT device network provisioning (WiFiManager)
* mDNS configuration for `.local` access
* Real-time interaction between hardware and web interface
* Integration of embedded systems with web technologies

---

##  Possible Extensions

* Add obstacle avoidance sensors (Ultrasonic)
* Implement live camera streaming (ESP32-CAM)
* Control via mobile app (Flutter / React Native)
* MQTT-based control for better IoT scalability

---

##  Author

**Harshal Lokhande**

Electronics & Telecommunication | Aspiring Software Engineer | Data Science Enthusiast

---

## ⭐ Why This Project?

> Demonstrates practical knowledge of **IoT systems, networking fundamentals, embedded web servers, and hardware-software integration**, while showcasing complex and analytical thinking.

---


## ⭐ Future Scope

* **Command Logging:** Implement a logging system on the server to record all control commands (Forward, Backward, Left, Right, Stop) with timestamps for future analysis and debugging.
* **Path Mapping:** Develop functionality to visualize or generate a map of the rover's movement path based on the sequence of commands from the commands received.
* **Data Storage:** Store movement logs locally (e.g., SPIFFS on ESP32) or remotely (e.g., cloud database) for historical tracking.
* **Analytics Dashboard:** Create a web-based dashboard to display past movement logs, command history, and possible path heatmaps.

---




