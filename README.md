Brainstorming

I wanted to create a low cost RC plane using simple electronics and a light foam glider. I wanted to make a functional plane for as little money as possible.

At first, I tried using normal RC airplane parts, but they were too expensive for the budget of the project. Instead, I decided to use:

a cheap foam glider as the airframe
an ESP32-C3 SuperMini clone for wireless control
coreless motors for flying the plane
a phone instead of a rc controller

The main idea of the project was:

Create a Wi Fi controlled airplane using cheap and easily available components.

I also wanted the project to:

- be easy to repair
- use light components
- doesnt cost too much
- be controlled from a phone

2. Research

Before starting the build, I researched different components and methods for controlling the plane.

Airframe Research

I decided to use a small foam glider costing around 1–2 euros because:

- it is lightweight
- it already has an aerodynamic shape
- it is cheap and easy to replace
- foam is easy to modify and cut
- Microcontroller Research

I researched several boards and chose the ESP32-C3 SuperMini clone because:

- it has built in Wi-Fi
- it is very small and light
- it uses low power
- it is inexpensive

To control two motors independently, I chose the TB6612 motor driver because:

- it is more efficient than the L298N
- it supports dual motor control
- it is compact and light
- it works well with small DC motors

Battery Research

I selected a 500 mAh LiPo battery because it was just simply the best option otherwise the plane would be underpowered or the battery couldve not produced enough power.

Instead of using a normal RC transmitter and receiver, I decided to use Wi-Fi control from a phone. I researched different apps and found RemoteXY
, which allows custom phone interfaces for ESP32 projects.

3. Planning:

I worked on the design of the plane and decided to use the foam glider as the frame.

The control system is based on differential thrust. Instead of using moving rudders or control surfaces, the plane will turn by changing the speed of the two motors:

if the left motor slows down, the plane turns left
if the right motor slows down, the plane turns right

I also planned the wiring connections between:

- Esp32 C3
- Tb6612 motor driver
- motors
- battery

4. App Design

I created the phone control app using RemoteXY.

The app contains:

- motor speed control
- steering control
- wireless communication with the ESP32

The phone connects directly to the ESP32 over Wi Fi, so the aircraft can be controlled without an RC transmitter.


Here is a screenshot of a 3d model:<img width="552" height="524" alt="image" src="https://github.com/user-attachments/assets/49f49ce8-8f12-495f-8ae1-01902eb04c76" />
 

<img width="552" height="524" alt="image" src="https://stasis.hackclub-assets.com/images/1778180597173-wdec39.png" img>


