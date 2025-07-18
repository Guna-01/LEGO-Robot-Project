# LEGO-Based Mobile Robot Navigation and Structure Identification 🚀🤖

Welcome to the **EC6090 Mini Project 2025** repository from the University of Jaffna! This project features a LEGO Mindstorms-based mobile robot designed to autonomously navigate a circular path (radius = 1.3m) and identify the shape of a central structure (square, circle, or triangle) in one rotation. 🎓🔍

## 📖 Project Overview
The robot uses a **sensor-based line-following approach** with a PID controller for navigation and an **edge-counting algorithm** for shape detection. Built with the LEGO Mindstorms core-set kit, it leverages light, ultrasonic, and gyro sensors to achieve precise navigation and accurate shape identification. 🛠️📐

- **Group Members**: 2021/E/010, 2021/E/098, 2021/E/140, 2021/E/185
- **Institution**: University of Jaffna
- **Date**: June 2025

## 🛠️ System Architecture
- **Hardware**: LEGO Mindstorms kit with:
  - Two motors (A and D) for differential drive ⚙️
  - Light sensor (port 1) for line following 🌞
  - Ultrasonic sensor (port 3) for shape detection 📡
  - Gyro sensor (port 2) for rotation tracking 🌀
- **Control**: PID controller (Kp=0.9, Ki=0, Kd=0.7) for smooth navigation 🎮
- **Programming**: Scratch-like block-based environment for LEGO Mindstorms 🖥️
- **Path**: Circular track with 1.3m radius (circumference ≈ 8.17m) 🛤️

## 🚗 Navigation
The robot follows a circular path using a light sensor to detect the line (goal intensity: 45). The PID controller adjusts motor speeds dynamically:
- **Base Speed**: 40% (~0.2 m/s)
- **Time per Rotation**: ~42 seconds (with PID corrections)
- **PID Tuning**: Iterative tuning reduced oscillations to <2 cm 📉

## 🔍 Shape Detection
An ultrasonic sensor measures distances to the central structure, and an edge-counting algorithm identifies shapes:
- **Square**: 4 edges detected ✅
- **Triangle**: 3 edges detected 🔺
- **Circle**: 0 edges detected ⭕
- **Threshold**: 30 cm for edge detection, optimized with a timer to eliminate noise 📏

## 📂 Repository Contents
- `robot_navigation.ev3`: Code for line-following navigation using PID control 📄
- `shape_detection.txt`: Pseudocode for the edge-counting algorithm 🧑‍💻
- `block_diagram.png`: Screenshot of the Scratch-like block-based code 📸
- `docs/MiniProject_EC6090_Group_14.pdf`: Full project report 📚

## 🛑 Challenges Faced
- **Sensor Noise**: Ultrasonic sensor errors mitigated with timer-based optimization 🚧
- **PID Tuning**: Initial oscillations resolved through iterative tuning (Section 3.3) ⚖️
- **Limited Testing**: 1-hour lab slot; used simulations for efficiency ⏱️
- **Shape Detection**: Calibrated 30 cm threshold for reliable edge detection 🎯

## 📊 Results
- **Navigation**: Completed 8.17m path in ~42 seconds with minimal deviations 🚀
- **Shape Detection**: 100% accuracy in identifying square (4 edges), triangle (3 edges), and circle (0 edges) ✅
- **Optimization**: Timer reduced false edge detections to zero 🛠️

## 🖥️ How to Run
1. **Requirements**: LEGO Mindstorms EV3 kit and software 📦
2. **Setup**: Load `robot_navigation.ev3` into the LEGO Mindstorms software.
3. **Path**: Mark a 1.3m radius circular path with a detectable line.
4. **Run**: Deploy the code on the robot and place it on the path. 🚗
5. **Shape Detection**: Ensure the central structure is within ultrasonic sensor range.

## 🙌 Contributing
Contributions are welcome! Feel free to fork this repository, make improvements, and submit pull requests. For collaboration, contact the group members via GitHub. 🤝

## 📜 License
This project is licensed under the MIT License. See [LICENSE](LICENSE) for details. 📄
