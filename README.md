# servo-motor-arduino

# 🤖 Humanoid Robot Servo Control

This project demonstrates how to control **4 servo motors** using an Arduino to simulate humanoid robot motion. The code starts with a sweeping motion for 2 seconds and then makes all servos hold at a fixed angle of 90°.

---

## 🔧 Components Used

- Arduino UNO (or compatible)
- 4x SG90 servo motors
- 4x Polarized Capacitor 100µF and 25v
- External 5V power supply (for multiple servos)
- Breadboard and jumper wires

---
## 

https://github.com/user-attachments/assets/97550c62-37aa-46b7-9ef4-e23a8debc0d7

<img width="1296" height="633" alt="Image" src="https://github.com/user-attachments/assets/c6dcac2b-1299-4ed4-82bb-33fecfc7482a" />

## 📂 Project Structure

📁 humanoid-servo-motion
│
├── servo_motor_code.ino # Arduino code for 2s sweep then 90° hold
├── README.md # Project description and instructions


yaml
Copy
Edit

---

## 🚀 Features

- 🕑 Sweeps all servos from 0° to 180° for 2 seconds
- ⛔ Stops motion and holds all servos at 90°
- 🦿 Lays groundwork for a walking humanoid robot
- 💡 Uses Arduino's built-in `Servo.h` library

---

## 📥 How to Use

1. **Wire up** the servos:
   - Connect signal wires to pins: `3`, `5`, `6`, and `9`
   - Power servos using **external 5V supply**
   - Ensure all grounds (Arduino and external power) are connected

2. **Upload** the code from `ServoSweepAndHold.ino` to your Arduino.

3. **Observe** the motors:
   - They will sweep back and forth for 2 seconds
   - Then all will stop and hold at 90°

---

## 🦿 Step-by-step Walking Algorithm:
text
Copy
Edit
1. Initialize:
   - Set all servos to standing position (e.g., 90°)

2. Lift left leg:
   - Raise left hip servo (e.g., 90° → 60°)
   - Bend left knee servo (90° → 120°)

3. Move left leg forward:
   - Rotate left hip servo forward (60° → 30°)
   - Keep knee bent

4. Place left leg down:
   - Straighten left knee (120° → 90°)

5. Shift balance to left leg:
   - Optional: Tilt body or adjust right leg slightly

6. Repeat steps for right leg:
   - Raise right hip (90° → 120°)
   - Bend right knee (90° → 60°)
   - Swing leg forward (hip: 120° → 150°)
   - Straighten knee (60° → 90°)

7. Repeat entire cycle for continuous walking
