This project is a lightweight ESP32-C3 powered RC plane control system designed for small RC aircraft. It is focused purely on flight control and motor driving. It controls dual motors, processes basic flight logic. It is built to be:

Lightweight enough for small battery-powered planes Modular Beginner-replicable with standard components What it does:

The system provides:

Motor control Basic stabilization logic Battery-powered operation

Future upgrades can include GPS navigation, autopilot logic, or telemetry.

Why I made it:

I've always seen that rc plane are very expensive. I personally wanted to make something easy and cheap.

How to use it:

Hardware setup Connect ESP32-C3 to motor drivers Attach LiPo battery Upload firmware Flash firmware using Arduino IDE or PlatformIO Select ESP32-C3 board Power on Connect battery System initializes motors and begins control loop Components: ESP32-C3 - 3 dollars DRV8833 motor driver - 2 dollars 2x Coreless DC motors - 2.5 dollars Jumper Wires x 20 - 2 dollars A glider frame - 2.5 dollars 500 mAh battery 3.7v - 4 dollars all availible on aliexpress

          +  -
          |  |
          |  |
----------------------
|                    |
|     DRV8833       |
|                    |
| VM ----------- +   |  (Battery +)
| GND ----------- -   |  (Battery -)
|                    |
| IN1 ---- GPIO 0    |  (ESP32-C3)
| IN2 ---- GPIO 1    |
| IN3 ---- GPIO 2    |
| IN4 ---- GPIO 3    |
|                    |
| OUT1 ---- Motor A  |
| OUT2 ---- Motor A  |
| OUT3 ---- Motor B  |
| OUT4 ---- Motor B  |
----------------------
ESP32-C3:

GND → DRV8833 GND 3.3V → (optional logic VCC if needed) 1x LiPo battery (3.7V)

Here is a screenshot of a 3d model:<img width="552" height="524" alt="image" src="https://github.com/user-attachments/assets/49f49ce8-8f12-495f-8ae1-01902eb04c76" />
 
<img width="1602" height="1079" alt="image" src="https://github.com/user-attachments/assets/98885958-4c9f-4dca-94c2-e8d2640f9039" />is a screenshot of the wiring diagram which uses different componenets but serves the same purpose:imageinstead of custom made motor drivers we are going to be using a drv8833.

Here is the poster<img width="2000" height="1414" alt="image" src="https://github.com/user-attachments/assets/3b96c857-13d0-44b0-a18c-f9654a64afdd" />
:5th  Milestone Certificate
