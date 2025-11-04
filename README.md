# SMART-DOOR-LOCK
a small coa project which can unlock door wired and wireless 


🔐 ESP8266 CyberLock – Smart Wi-Fi Door Lock System
📖 Overview
CyberLock is a smart lock system built using an ESP8266 microcontroller.
It creates its own Wi-Fi hotspot and serves a web interface that allows users to unlock access by entering a 6-digit secret PIN. The system uses LEDs and a buzzer to indicate authentication success or failure.
This project demonstrates secure web-based authentication, GPIO control, and embedded web server handling using the ESP8266.
⚙️ Features
🚪 Web-based access control via browser
🔑 6-digit PIN authentication system
💡 Visual and audio feedback using LEDs and buzzer
🌐 Self-hosted Wi-Fi network (Access Point mode)
💾 Responsive HTML/CSS interface stored in flash memory (PROGMEM)
📱 Works on both mobile and desktop browsers
🧰 Hardware Requirements
Component	Description
ESP8266 (e.g., NodeMCU, Wemos D1 Mini)	Wi-Fi microcontroller
Green LED	Indicates successful access
Red LED	Indicates denied access
Buzzer	Provides audio feedback
Resistors	220Ω–330Ω for LEDs
USB Cable	For programming and power
🔌 Pin Configuration
Component	ESP8266 Pin
Green LED	D1
Red LED	D2
Buzzer	D3
🧾 Setup Instructions
Install Arduino IDE and add the ESP8266 Board Manager URL:
https://arduino.esp8266.com/stable/package_esp8266com_index.json
Install Libraries:
ESP8266WiFi.h
ESP8266WebServer.h
Open the Code:
Load the file Smart_Lock.cpp in Arduino IDE.
Edit Credentials:
const char* ssid = "DoorLock_AP";
const char* password = "password123";
const char* SECRET_PIN = "123456";  // Change this to your own PIN
Upload the Code:
Select your board: Tools → Board → NodeMCU 1.0 (ESP-12E Module)
Select the correct COM port and upload.
Connect to the Network:
On your phone or laptop, connect to Wi-Fi:
SSID: DoorLock_AP
Password: password123
Access the Lock Interface:
Open your browser and go to
http://192.168.4.1
Enter the Secret PIN and test the system:
✅ Correct PIN → Green LED blinks, success tone plays.
❌ Wrong PIN → Red LED blinks, alarm tone plays.
🎨 Web Interface Preview
The webpage features a cyberpunk-style design using:
Orbitron font (from Google Fonts)
Glowing animations and neon color palette
Responsive layout for mobile and desktop
🔉 Feedback Behavior
Condition	LED	Sound	Message
Correct PIN	Green LED blinks	Success tone	“ACCESS GRANTED”
Incorrect PIN	Red LED blinks	Alarm tone	“ACCESS DENIED”
🧠 Future Improvements
Add relay or servo to physically unlock a door.
Integrate with Firebase for PIN logging.
Include multi-user support or PIN reset system.
Add HTTPS and PIN timeout for better security.
📜 License
This project is open-source under the MIT License.
You may modify and use it freely for educational and personal use.
