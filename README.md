Smart Robotic Arm — Gesture Controlled Multi-Axis System

A real-time gesture-controlled robotic arm built using ESP32 firmware and computer vision (OpenCV + MediaPipe). The system allows intuitive multi-axis control of a robotic arm using hand tracking and ML-based gesture recognition.

🚀 Features

Multi-axis servo control (Base, Shoulder, Elbow, Wrist, Gripper)

Real-time hand tracking using OpenCV + MediaPipe

Gesture classification using ML (NumPy / TensorFlow Lite)

Low-latency communication via HTTP/WebSockets

OTA firmware update support

Power stability & servo jitter optimization

Modular firmware architecture

Real-time motion control loop

Expandable hardware design

🏗️ System Architecture
[Camera Input]
        ↓
OpenCV + MediaPipe
        ↓
Gesture Classification
        ↓
Command Mapping Layer
        ↓
WiFi Communication (HTTP/WebSocket)
        ↓
ESP32 Firmware
        ↓
PCA9685 Servo Driver
        ↓
Robotic Arm Actuation
🧠 How It Works

Hand landmarks detected using MediaPipe.

Gesture classified using custom logic / ML model.

Gesture mapped to robotic arm movement.

Commands sent to ESP32 over WiFi.

ESP32 updates servo positions in real-time.

Low-latency pipeline ensures smooth and responsive control.

🔩 Hardware Components

ESP32

PCA9685 Servo Driver

5x Servo Motors

External power supply

Camera (USB/Webcam)

Custom mechanical arm structure

3D-printed mounts (optional)

💻 Software Stack
Embedded

ESP32

Embedded C++

FreeRTOS

PWM control

OTA update system

Computer Vision

Python

OpenCV

MediaPipe

NumPy

TensorFlow Lite (optional)

📡 Communication

HTTP / WebSocket-based real-time control

JSON command packets

Optimized control loop for reduced latency

📈 Challenges Solved

Servo jitter reduction

Power stability under load

Gesture classification accuracy

Latency optimization

Real-time smooth actuation

Modular firmware structure

📷 Demo

(Add demo video or GIF here)

📦 Folder Structure
smart-robotic-arm/
│
├── firmware/
│   ├── main.cpp
│   ├── servo_controller.cpp
│   ├── wifi_server.cpp
│   ├── ota_update.cpp
│   └── config.h
│
├── computer_vision/
│   ├── hand_tracking.py
│   ├── gesture_classifier.py
│   ├── command_mapper.py
│   └── requirements.txt
│
├── hardware/
│   ├── circuit_diagram.png
│   └── component_list.md
│
├── docs/
│   ├── architecture.png
│   └── setup_guide.md
│
└── README.md
🔌 Setup Guide
Firmware

Install PlatformIO or Arduino IDE.

Flash firmware to ESP32.

Configure WiFi credentials.

Connect PCA9685 and servos.

Computer Vision

Install dependencies:

pip install -r requirements.txt

Run:

python hand_tracking.py
🛠️ Future Improvements

Add inverse kinematics

Web dashboard control

Edge AI deployment

Mobile app interface

Object detection integration

ROS compatibility

🎯 Applications

Industrial automation

Educational robotics

Assistive robotics

Smart manufacturing

AI-driven automation systems

👤 Author

Jishnu Mahanta
Full-stack & IoT Engineer
Building intelligent systems & calm UX.
