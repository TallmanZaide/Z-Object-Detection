# Z-Object-Detection

An Arduino-based automated object detector that scans an environment, detects obstacles, measures distances, and triggers alerts on an LCD screen.

---

## Project Overview

This system automates obstacle detection using a scanning ultrasonic sensor assembly. A servo motor constantly sweeps the sensor between 15° and 165°. If an object enters the detection threshold, the system immediately halts the sweep, calculates the exact distance to the target, and outputs a visual alert alongside the distance metrics onto an explicit hardware LCD screen display.

---

## Visuals and Demos

### System Setup
<!-- Upload your image to the repo and reference it here -->
![System Prototype Layout](path-to-your-image.jpg)

### Working Video Demo
<!-- Drag and drop your mp4 video directly into GitHub's text editor here to render a video player -->
[Watch the system operation demo video](path-to-your-video.mp4)

---

## Key Features

* Real-Time Detection: Continuous environmental boundary scanning utilizing ultrasonic sound waves.
* Dynamic Braking and Alerting: Instantly halts motor sweep upon detection and prints explicit instructions ("Remove Object") onto the display interface.
* Precision Distance Calculation: Converts sensor pulse timings into real-world centimeter measurements.

---

## System Architecture and Pin Mapping

To replicate or modify this project, connect the components to your microcontroller board according to the mapping matrix below:

| Component | Component Pin | Arduino Uno Pin | Notes |
| :--- | :--- | :--- | :--- |
| HC-SR04 Sensor | VCC | 5V | Power supply |
| HC-SR04 Sensor | GND | GND | Ground reference |
| HC-SR04 Sensor | Trig | Pin 9 | Output trigger pulse |
| HC-SR04 Sensor | Echo | Pin 10 | Input echo pulse |
| SG90 Servo | PWM / Signal | Pin 11 | Motor position control |
| SG90 Servo | Power | 5V | External 5V source recommended |
| Potentiometer | Wiper (Middle) | LCD VO / Pin 3 | Adjusts display contrast |

---

## Bill of Materials (BOM)

* 1x Elegoo Uno R3 Microcontroller Board
* 1x HC-SR04 Ultrasonic Sonar Sensor Module
* 1x SG90 Micro Servo Motor
* 1x 16x2 LCD Display Screen (with I2C or standard pin-out)
* 1x 10k Ohm Potentiometer
* 1x Solderless Breadboard
* M-M / M-F Jumpers Wires

---

## Getting Started for Collaborators

1. Clone this repository locally.
2. Open the primary `.ino` sketch file inside your Arduino IDE.
3. Install required library dependencies via the Library Manager:
   * `Servo.h`
   * `LiquidCrystal.h` (or `LiquidCrystal_I2C.h` depending on your display type)
4. Wire your hardware matching the system architecture diagram/table.
5. Verify the code compilation and flash the binary payload directly onto the Uno board.
