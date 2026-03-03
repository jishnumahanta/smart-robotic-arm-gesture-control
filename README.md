# Smart Robotic Arm — Gesture Controlled Multi-Axis System

A real-time gesture-controlled robotic arm powered by **ESP32 firmware** and **computer vision (OpenCV + MediaPipe)**. This system enables intuitive multi-axis control using hand tracking and machine learning–based gesture recognition.

---

## 🚀 Features

- Multi-axis servo control (Base, Shoulder, Elbow, Wrist, Gripper)
- Real-time hand tracking using MediaPipe
- Gesture classification with ML logic (NumPy / TensorFlow Lite optional)
- Low-latency communication via HTTP / WebSockets
- OTA firmware update support
- Servo jitter reduction & power stability optimization
- Modular firmware architecture
- Real-time motion control loop
- Expandable hardware design

---

## 🏗️ System Architecture

```
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
```

---

## 🧠 How It Works

1. Hand landmarks are detected using MediaPipe.
2. Gestures are classified using rule-based logic or ML models.
3. Gestures are mapped to robotic arm motion commands.
4. Commands are transmitted to ESP32 over WiFi.
5. ESP32 updates servo positions in real-time.

Optimized control pipeline ensures smooth and responsive actuation.

---

## 🔩 Hardware Components

- ESP32
- PCA9685 16-Channel Servo Driver
- 5x Servo Motors
- External regulated power supply
- USB / Webcam
- Custom robotic arm frame
- Optional 3D-printed mounts & housing

---

## 💻 Software Stack

### Embedded Layer
- ESP32
- Embedded C++
- FreeRTOS
- PWM-based servo control
- OTA update module

### Computer Vision Layer
- Python
- OpenCV
- MediaPipe
- NumPy
- TensorFlow Lite (optional)

---

## 📡 Communication

- HTTP / WebSocket-based real-time control
- JSON command packets
- Optimized latency handling

---

## 📂 Folder Structure

```
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
```

---

## 🔌 Setup Guide

### Firmware Setup

1. Install PlatformIO or Arduino IDE.
2. Configure WiFi credentials in `config.h`.
3. Connect PCA9685 and servos properly.
4. Flash firmware to ESP32.

### Computer Vision Setup

```bash
pip install -r requirements.txt
python hand_tracking.py
```

---

## ⚙️ Engineering Challenges Solved

- Servo jitter reduction using optimized PWM timing
- Power stability under multi-servo load
- Gesture classification accuracy tuning
- Latency optimization for real-time response
- Modular firmware state management

---

## 📈 Applications

- Industrial automation
- Educational robotics
- Assistive robotics
- Smart manufacturing
- AI-driven automation systems

---

## 🔮 Future Improvements

- Inverse kinematics integration
- Web-based control dashboard
- Edge AI deployment on-device
- Mobile app integration
- Object detection integration
- ROS compatibility layer

---

## 👤 Author

**Jishnu Mahanta**  
Full-stack & IoT Engineer  
Building intelligent systems & calm UX.

---

## 📜 License

MIT License 
