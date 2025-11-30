# Smart-Water-Level-Monitoring-System

🚰 Smart Water Level Monitoring System using Arduino

This project is a smart water-level monitoring system built using an Arduino Uno, HC-SR04 Ultrasonic Sensor, LCD Display, Relay Module, Push Buttons, and EEPROM storage.
It automatically detects the water level in a tank and controls the pump in AUTO or MANUAL mode. The LCD continuously displays the current water level percentage and pump status.

🧠 Features

1) Measures water level using ultrasonic sensing
2) Automatic pump control based on water level
3) Manual control via push button
4) Saves maximum water height to EEPROM

LCD display shows:

1) Water level %
2) Pump status (ON/OFF)
3) Current mode (AUTO / MANUAL)

▶️ How to Use

1) Power the system 🟢
2) Press SET button once to store the current tank height to EEPROM
3) System enters AUTO mode pumping based on water percentage
4) Press MODE button to toggle AUTO/MANUAL
5) In MANUAL mode, press SET button to toggle pump ON/OFF

🛠 Components Used

| Component                      | Quantity    |
| ------------------------------ | ----------- |
| Arduino Uno                    | 1           |
| HC-SR04 Ultrasonic Sensor      | 1           |
| 16x2 LCD Display               | 1           |
| Relay Module (5V)              | 1           |
| Push Buttons                   | 2           |
| LED Indicator                  | 1           |
| Resistors                      | As required |
| Potentiometer for LCD contrast | 1           |
| Jumper wires                   | Many        |

📡 Working Principle

The Ultrasonic sensor calculates the water level based on the time it takes for the sound wave to bounce back.
The water percentage is calculated relative to a set height stored in EEPROM:

percentage = (set_val - inches) * 100 / set_val

Pump automatically turns ON if level < 30%
Pump turns OFF when tank is full (>99%)

Manual mode allows direct pump control through a button.

🔧 Pin Connections
| Component               | Arduino Pin |
| ----------------------- | ----------- |
| LCD RS                  | 2           |
| LCD E                   | 3           |
| LCD D4–D7               | 4, 5, 6, 7  |
| Ultrasonic TRIG         | 8           |
| Ultrasonic ECHO         | 9           |
| Manual Set Button       | 10          |
| Mode Auto/Manual Button | 11          |
| Relay Output            | 12          |

