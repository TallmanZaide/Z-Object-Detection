# Z-Object-Detection

An Arduino-based automated object detector that scans an environment, detects obstacles, measures distances, and triggers alerts on an LCD screen.

---

## Project Overview

This system automates obstacle detection using a scanning ultrasonic sensor assembly. A servo motor constantly sweeps the sensor between 15° and 165°. If an object enters the detection threshold, the system immediately halts the sweep, calculates the exact distance to the target, and outputs a visual alert alongside the distance metrics onto an explicit hardware LCD screen display.

---

## Visuals and Demos

### System Setup
<!-- Upload your image to the repo and reference it here -->
<img width="2160" height="2880" alt="Object detecor IMG 1" src="https://github.com/user-attachments/assets/8b6c6af5-40ec-48b5-83f6-64a64671de8d" />

### System Startup
<img width="2363" height="1466" alt="Object detector IMG 2" src="https://github.com/user-attachments/assets/24e6ce4a-1bac-405f-ab7a-87c3ab9d0986" />


### Working Video Demo
<!-- Drag and drop your mp4 video directly into GitHub's text editor here to render a video player -->


https://github.com/user-attachments/assets/d8ce2b78-300a-41b7-8098-e8868047e46a





---

## Key Features

* Real-Time Detection: Continuous environmental boundary scanning utilizing ultrasonic sound waves.
* Dynamic Braking and Alerting: Instantly halts motor sweep upon detection and prints explicit instructions ("Remove Object") onto the display interface.
* Precision Distance Calculation: Converts sensor pulse timings into real-world centimeter measurements.

---

## Electrical Schematic and Pin Mapping

### Tinkercad Circuit Diagram
<!-- Export your diagram from Tinkercad, upload it to your repo, and reference it below -->

<img width="917" height="572" alt="image" src="https://github.com/user-attachments/assets/d7112d4d-9116-431b-bf4a-accbc07a43d3" />



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
