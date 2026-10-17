# ⚡ Automatic Transformer Protection and Monitoring System

## 📌 Project Overview

The **Automatic Transformer Protection and Monitoring System** is an Arduino-based prototype designed to monitor the operating conditions of a transformer and protect it against abnormal electrical and thermal conditions.

The system continuously monitors voltage, current, and temperature using dedicated sensors. When an abnormal condition such as overvoltage, undervoltage, overcurrent, or overtemperature is detected, the Arduino processes the sensor readings and activates a relay to disconnect the load. An LCD, LEDs, and a buzzer provide real-time status and fault indications.

The project demonstrates the application of embedded systems, sensor interfacing, and basic electrical protection concepts.

## 🎯 Objectives

- Monitor transformer voltage, current, and temperature in real time.
- Detect overvoltage and undervoltage conditions.
- Detect excessive current and overtemperature conditions.
- Automatically disconnect the load during a detected fault.
- Provide visual and audible fault alerts.
- Improve operational safety through automated monitoring and protection logic.

## 🛠️ Components Used

| Component | Purpose |
|---|---|
| Arduino Uno | Main controller for monitoring and protection logic |
| ZMPT101B Voltage Sensor | AC voltage measurement |
| ACS712 Current Sensor | Current measurement |
| LM35 Temperature Sensor | Temperature monitoring |
| 16×2 I²C LCD | Display of measurements and system status |
| 5V Relay Module | Load disconnection during fault conditions |
| LEDs | Visual indication of normal and fault states |
| Buzzer | Audible fault alert |
| Push Button | Manual reset after a fault |
| Step-down Transformer | Low-voltage transformer under test |
| Connecting Wires and Breadboard | Circuit connections |

## ⚙️ Working Principle

1. **Sensing:** The ZMPT101B, ACS712, and LM35 measure voltage, current, and temperature, respectively.
2. **Processing:** The Arduino Uno reads the sensor outputs and compares the measured values with predefined protection limits.
3. **Fault Detection:** The controller identifies abnormal operating conditions.
4. **Protection:** When a fault is confirmed, the relay disconnects the load to prevent continued operation under the detected abnormal condition.
5. **Alert System:** The LCD displays the fault status, while the LED indicators and buzzer provide visual and audible alerts.
6. **Manual Reset:** A reset button allows the system to resume operation after the fault is cleared and the monitored parameters return to safe limits.

## 🔒 Protection Features

The prototype implements four basic protection functions:

| Protection | Initial Threshold | Action |
|---|---|---|
| Undervoltage | Below 10.5 V | Disconnect load |
| Overvoltage | Above 13.5 V | Disconnect load |
| Overcurrent | Above 1.2 A | Disconnect load |
| Overtemperature | At or above 70°C | Disconnect load |

*Note: These are initial prototype settings for a nominal 12 V, 1 A transformer secondary. Actual thresholds must be verified against the implemented code, sensor calibration, and transformer specifications.*

## 🔌 Hardware and Software

**Hardware**
- Arduino Uno
- Voltage, current, and temperature sensors
- Relay-based load switching circuit
- LCD and fault indication circuit

**Software**
- Arduino IDE
- Embedded C/C++ (Arduino programming)
- Sensor reading and calibration
- Threshold-based fault detection
- Relay control and fault-reset logic

## 🧠 Key Concepts Learned

- Microcontroller-based monitoring and control
- Voltage and current sensor interfacing
- AC voltage measurement and RMS calculation
- Temperature sensing and threshold comparison
- Relay-based protection and load isolation
- Fault detection, alarm generation, and reset logic
- Troubleshooting sensor readings and calibration issues

## 🚀 Future Improvements

- Add data logging for historical analysis of transformer operating conditions.
- Integrate IoT-based remote monitoring and fault notifications.
- Implement improved filtering and sensor calibration for more reliable measurements.
- Add fault-event timestamps and a fault history display.
- Evaluate additional protection functions and communication interfaces.

## ⚠️ Limitations and Safety

This project is an **educational, low-voltage prototype** intended to demonstrate basic transformer monitoring and protection concepts. It is not a substitute for industrial transformer protection relays or certified protection systems.

Sensor accuracy, calibration, relay response, electrical isolation, and fault-handling logic must be validated before practical deployment. Never connect an Arduino or exposed breadboard circuitry directly to mains voltage. Use appropriate isolation, enclosures, and supervised electrical testing.

## 👩‍💻 Author

**Kunga Chuskit**  
B.Tech Electrical Engineering

---

⭐ If you find this project useful, consider starring the repository!

