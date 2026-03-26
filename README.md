# RTRP--IOT-ELDERLY-CARE-MONITORNG
README: IoT-Based Elderly Care and Fall Detection System
A professional, non-intrusive monitoring solution designed to ensure the safety of senior citizens living independently. This system tracks real-time body temperature and detects physical falls through 3-axis motion analysis, providing instant data visualization and emergency alerts to caretakers.

Features
3-Axis Fall Detection: Monitors acceleration and orientation changes across the X, Y, and Z planes using an MPU6050 sensor.

Continuous Vital Monitoring: Real-time tracking of body temperature using the LM35 precision integrated-circuit sensor.

Dual-Layer Alert System: * Local: Immediate audio feedback via a 5V active buzzer.

Remote: Instant push notifications and live data streaming via the Blynk IoT Cloud.

Low Latency: Optimized firmware ensures emergency alerts reach the caretaker's device in approximately 2-4 seconds.

Hardware Requirements
Microcontroller: NodeMCU (ESP8266 or ESP32)

Motion Sensor: MPU6050 (Accelerometer + Gyroscope)

Temperature Sensor: LM35

Alert Module: 5V Active Buzzer

Power: 5V Micro-USB Power Supply

Software and Stack
Language: C++ (Arduino Framework)

IDE: Arduino IDE

Cloud Platform: Blynk IoT

Libraries: * BlynkSimpleEsp8266.h (or ESP32 equivalent)

Adafruit_MPU6050.h

Wire.h (for I2C communication)

System Architecture
The system is built on a modular architecture:

Sensing Layer: Continuous raw data acquisition from the X, Y, and Z planes.

Processing Layer: NodeMCU executes threshold-based logic to distinguish between normal activity and accidental falls.

Communication Layer: Secure Wi-Fi transmission of sensor values to the Blynk Cloud.

Application Layer: A user-friendly mobile dashboard for remote monitoring and alert history.

Installation and Setup
Repository Setup:

Bash
git clone https://github.com/VagdeviVellala/Elderly-Care-IoT.git
Blynk Configuration:

Create a new template in the Blynk Console.

Set up Virtual Pin V1 for Temperature and V2 for Fall Status.

Firmware Deployment:

Open the project file in Arduino IDE.

Input your unique BLYNK_AUTH_TOKEN and Wi-Fi credentials (SSID/Password).

Compile and upload the code to your NodeMCU.

Future Scope
GPS Integration: Adding location tracking for patients with wandering tendencies.

Solar Sustainability: Implementing flexible solar panels for long-term power autonomy.

Activity Recognition: Deploying TinyML models to increase the accuracy of fall detection logic.
