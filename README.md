
# 🤖 Arduino Pot-Controlled Servos

This project demonstrates how to control **four SG90 servo motors** using **four potentiometers** on an **Arduino Uno**. Turn a knob and watch the corresponding servo move—real-time control using analog input and PWM output.

---

## 🎯 Learning Objectives

- Read analog input using `analogRead()`
- Map potentiometer values (0–1023) to servo angles (0–180°)
- Control multiple servos using the `Servo.h` library
- Set up clean power and ground rails on a breadboard
- Document the project with images or videos for GitHub

---

## 🔧 Required Components

| Qty | Component                          |
|-----|------------------------------------|
| 1   | Arduino Uno R3                     |
| 4   | SG90 Positional Micro Servo Motors |
| 4   | 100 µF, 25 V Polarized Capacitors  |
| 1   | Breadboard + Jumper Wires          |
| 1   | 5V / 2A External Power Supply (*)  |

(*) USB power works for testing, but external power is safer when driving all servos.

---

## 🛠️ Tools & Libraries

- Arduino IDE 2.x
- Built-in `Servo.h` library
- Tinkercad Circuits (for simulation and prototyping)

---

## ⚙️ How It Works

1. Potentiometers connect to analog pins `A0` through `A3`.
2. Each servo’s control wire connects to PWM pins (`3`, `5`, `6`, `9`).
3. In the main loop:
```cpp
int potVal = analogRead(A0);             // Read pot value (0–1023)
int angle  = map(potVal, 0, 1023, 0, 180); 
servo1.write(angle);                     // Set servo angle
```
4. Repeat this process for all servos every ~20 ms for smooth motion.
---
## Preview


<img width="2560" height="1180" alt="Brave Albar-Blorr" src="https://github.com/user-attachments/assets/3ef75b28-16b6-4e4a-84d2-2664817b7a0f" />


---
## Have a closer Look

https://shorturl.at/EA4aG

---

## 👤 Author

> Created by **Ahmed Jamjoom**  
> 📅 Date: July 17, 2025
