🚗 IoT-Based Web Controlled Rover with Embedded Web Server (ESP32)
📑 Project Overview
This project demonstrates a simple IoT-controlled rover powered by ESP32. The rover is controlled via a web-based interface hosted directly on the ESP32's internal HTTP server. The setup leverages WiFiManager for flexible Wi-Fi network configuration and mDNS (esp32.local) for convenient, user-friendly access.

Users can control the vehicle’s movement (Forward, Backward, Left, Right, Stop) through any device connected to the same network via a browser.

🔧 Technologies & Tools
ESP32 Microcontroller

Arduino IDE / ESP-IDF

WiFiManager Library (for dynamic Wi-Fi provisioning)

ESP32 WebServer Library (HTTP server)

mDNS (esp32.local) for DNS-like access on local network

HTML / CSS / JavaScript (for the browser-based control panel)

DC Motor Driver (H-Bridge) for motor control (L298N / L293D)

🌐 Features
✅ Web interface hosted directly on ESP32
✅ Mobile / Desktop browser control
✅ No external apps required
✅ Real-time directional commands: Forward, Backward, Left, Right, Stop
✅ WiFiManager-based dynamic network configuration
✅ mDNS (esp32.local) for easy access without IP lookup

📸 User Interface (Screenshot)

(Optional - Add screenshot if available)

🚦 Project Architecture
plaintext
Copy
Edit
Client Device (Phone / PC)
        |
     Browser (HTML/JS)
        |
     HTTP Requests
        |
     ESP32 WebServer (mDNS: esp32.local)
        |
 Motor Control (GPIO Pins -> Motor Driver)
📂 Project Structure
bash
Copy
Edit
/src
  |-- main.ino               # Main Arduino sketch
  |-- libraries               # WiFiManager, WebServer
/assets
  |-- web-ui.png              # Screenshot (optional)
/README.md                    # This file
🚀 How to Run
1️⃣ Hardware Setup
ESP32 Development Board

L298N / L293D Motor Driver Module

2 DC Motors (for differential drive)

Power Supply (Battery)

2️⃣ Software Setup
Install Arduino IDE

Install ESP32 Board Packages

Install Libraries:

WiFiManager

ESPmDNS

WebServer

3️⃣ Upload the Code
Flash the provided code via Arduino IDE.

On first boot, connect to ESP32-Config Wi-Fi to configure your home Wi-Fi.

4️⃣ Access the Control Panel
Open browser → Visit: http://esp32.local (after successful pairing)

Use on-screen buttons to control the rover.

🎮 Control Interface
Action	HTTP Endpoint
Forward	/forward
Backward	/backward
Left	/left
Right	/right
Stop	/stop

💡 Learning Outcomes
Embedded HTTP server deployment

IoT device network provisioning (WiFiManager)

mDNS configuration for .local access

Real-time interaction between hardware and web interface

Integration of embedded systems with web technologies

📌 Possible Extensions
Add obstacle avoidance sensors (Ultrasonic)

Implement live camera streaming (ESP32-CAM)

Control via mobile app (Flutter / React Native)

MQTT-based control for better IoT scalability

👨‍💻 Author
Harshal Lokhande
Electronics & Telecommunication | Aspiring Software Engineer | IoT & Embedded Systems Enthusiast

⭐ Why This Project?
Demonstrates practical knowledge of IoT systems, networking fundamentals, embedded web servers, and hardware-software integration, which are essential for CS/IT placements in roles involving IoT, Embedded Systems, and Networking.
