 # Report on L293D Motor Driver IC

## 1. Introduction

The **L293D** is a dual H-bridge motor driver integrated circuit used to control the direction and speed of DC motors. It allows low-power microcontrollers such as Arduino, Raspberry Pi, or other embedded systems to control higher current motors.

The L293D acts as an interface between the control system and the motor, protecting the microcontroller from high voltage and current.

**Applications include:**
- Robotics
- Motorized vehicles
- Conveyor systems
- Embedded systems

The IC can drive **two DC motors independently**.

---

## 2. L293D IC Overview

The L293D is a **16-pin integrated circuit** designed to drive inductive loads such as motors and relays.

![IC](https://raw.githubusercontent.com/Killer7302/Report/refs/heads/main/L293D-Motor-Driver-IC-Pin-780x365.webp)

### Main Features
- Dual H-Bridge driver
- Current up to **600 mA per channel**
- Motor supply voltage up to **36V**
- Built-in **flyback protection diodes**
- TTL compatible logic inputs

It is widely used in robotics and automation systems.

---

## 3. Internal IC Structure

The L293D contains:

- **Four high-current transistor drivers**
- **Two H-bridge circuits**
- **Protection diodes**

These components allow the IC to control both **direction and speed of motors** safely.

---

## 4. Pin Configuration

| Pin | Function |
|----|----|
| 1 | Enable 1 |
| 2 | Input 1 |
| 3 | Output 1 |
| 4 | Ground |
| 5 | Ground |
| 6 | Output 2 |
| 7 | Input 2 |
| 8 | Motor Supply Voltage |
| 9 | Enable 2 |
| 10 | Input 3 |
| 11 | Output 3 |
| 12 | Ground |
| 13 | Ground |
| 14 | Output 4 |
| 15 | Input 4 |
| 16 | Logic Supply Voltage |

---

## 5. H-Bridge Motor Control

An **H-Bridge** is a circuit that allows current to flow in both directions through a motor, enabling forward and reverse motion.

### H-Bridge Operation

| Input1 | Input2 | Motor Direction |
|------|------|------|
| 0 | 0 | Stop |
| 1 | 0 | Forward |
| 0 | 1 | Reverse |
| 1 | 1 | Stop |

The L293D internally contains **two H-bridge circuits**, allowing it to control **two motors independently**.

---

## 6. PWM (Pulse Width Modulation)

PWM is used to control the **speed of the motor**.

Instead of changing voltage, PWM changes the **duty cycle of the signal**.

### PWM Duty Cycle

| Duty Cycle | Motor Speed |
|----|----|
| 0% | Motor OFF |
| 50% | Medium Speed |
| 100% | Full Speed |

PWM is usually applied to the **Enable pin** of the L293D.

Example:
Enable Pin = PWM signal

This varies the power supplied to the motor.

---

## 7. Working Principle

1. The microcontroller sends digital signals to the L293D inputs.
2. The L293D amplifies the current.
3. The H-bridge controls the direction of current through the motor.
4. PWM controls the motor speed.

Thus the motor can rotate:

- Forward
- Reverse
- Stop
- Variable speed

---

## 8. Applications

The L293D motor driver is used in many systems:

- Line following robots
- Robotic arms
- Automated vehicles
- Motor control systems
- Embedded automation

---

## 9. Advantages

- Simple to use
- Controls two motors
- Built-in protection diodes
- Compatible with microcontrollers

---

## 10. Limitations

- Current limited to **600 mA**
- Not suitable for high-power motors
- Generates heat at high loads

---

## 11. Conclusion

The L293D motor driver IC is a widely used device for controlling DC motors in robotics and embedded systems. Its internal H-bridge circuits allow bidirectional motor control, while PWM enables speed control. Due to its simplicity and compatibility with microcontrollers, it remains a popular choice in educational and small robotic applications.
