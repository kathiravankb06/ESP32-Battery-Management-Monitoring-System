# ESP32 Battery Management & Monitoring System

## Overview

This project is an ESP32-based Battery Management and Monitoring System (BMS) simulation developed using Wokwi. The system continuously monitors battery voltage, calculates battery percentage, detects low battery and overcharge conditions, and activates protection and alert mechanisms in real time.

The project demonstrates core embedded systems concepts including ADC reading, I2C communication, OLED interfacing, relay control, real-time monitoring, and embedded decision-making.

---

# Features

* Real-time battery voltage monitoring
* Battery percentage calculation
* OLED status display
* Low battery detection
* Overcharge protection logic
* Relay-based protection control
* LED status indication
* Buzzer alert system
* Serial monitor debugging output
* ESP32-based embedded control system

---

# Components Used

| Component            | Quantity |
| -------------------- | -------- |
| ESP32 Dev Board      | 1        |
| SSD1306 OLED Display | 1        |
| Potentiometer        | 1        |
| Relay Module         | 1        |
| Buzzer               | 1        |
| Green LED            | 1        |
| Red LED              | 1        |
| 220Ω Resistors       | 2        |

---

# Pin Connections

## OLED Display

| OLED Pin | ESP32 Pin |
| -------- | --------- |
| VCC      | 3.3V      |
| GND      | GND       |
| SDA      | GPIO21    |
| SCL      | GPIO22    |

---

## Potentiometer

| Potentiometer Pin | ESP32 Pin |
| ----------------- | --------- |
| VCC               | 3.3V      |
| GND               | GND       |
| SIG               | GPIO34    |

---

## Relay Module

| Relay Pin | ESP32 Pin |
| --------- | --------- |
| VCC       | 5V        |
| GND       | GND       |
| IN        | GPIO18    |

---

## Buzzer

| Buzzer Pin | ESP32 Pin |
| ---------- | --------- |
| +          | GPIO19    |
| -          | GND       |

---

## LEDs

### Green LED

| LED Pin | ESP32 Pin |
| ------- | --------- |
| +       | GPIO25    |
| -       | GND       |

### Red LED

| LED Pin | ESP32 Pin |
| ------- | --------- |
| +       | GPIO26    |
| -       | GND       |

---

# System Working

The potentiometer is used to simulate battery voltage.

The ESP32 continuously reads analog voltage values from GPIO34 using ADC.

Based on the measured voltage, the system performs the following actions:

## Low Battery Condition

When voltage is below 3.3V:

* Red LED turns ON
* Buzzer activates
* OLED displays LOW BATTERY
* Relay remains ON

---

## Normal Condition

When voltage is between 3.3V and 4.1V:

* Green LED turns ON
* Red LED turns OFF
* Buzzer turns OFF
* Relay remains ON
* OLED displays NORMAL

---

## Overcharge Condition

When voltage exceeds 4.1V:

* Relay turns OFF
* Red LED turns ON
* Buzzer activates
* OLED displays OVERCHARGE

---

# Embedded Concepts Demonstrated

* Analog-to-Digital Conversion (ADC)
* GPIO control
* I2C communication
* OLED interfacing
* Real-time monitoring
* Embedded protection logic
* Relay control
* Serial debugging
* Embedded decision making

---

# Project Output

The OLED display shows:

* Battery voltage
* Battery percentage
* Battery condition status

The LEDs, buzzer, and relay respond automatically according to battery conditions.

---

# Simulation Platform

Wokwi Online Simulator

---

# Future Improvements

* WiFi monitoring dashboard
* Mobile app integration
* Battery temperature monitoring
* Data logging system
* Cloud connectivity
* Battery health estimation
* IoT notifications
* Automatic charging control

---

# Demo Video


https://github.com/user-attachments/assets/b97ff892-8690-445d-96c7-e0b4186c9389




---



# Conclusion

This project demonstrates a simplified Battery Management and Monitoring System using ESP32. It simulates real-time battery monitoring, protection logic, and embedded system behavior using multiple peripherals and sensor-based decision making.

The project provides practical experience in embedded firmware development, hardware interfacing, and real-time control systems.
