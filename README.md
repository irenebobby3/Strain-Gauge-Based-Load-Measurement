# Strain-Gauge-Based-Load-Measurement
# Strain Gauge Based Load Measurement System

## Project Overview
This project implements a strain gauge-based load measurement system using an HX711 load cell amplifier and a microcontroller.

The strain gauge senses the applied load and produces a small change in electrical resistance. The HX711 module amplifies and converts this signal into digital data, which is processed by the microcontroller to measure the load.

The system also uses two digital output pins to indicate whether the measured load is above or below a predefined threshold.

## Components Used
- Strain Gauge Load Cell
- HX711 Load Cell Amplifier Module
- Microcontroller (Arduino-compatible board)
- Connecting wires
- LEDs or other output indicators (if connected)

## Pin Configuration

| Component | Microcontroller Pin |
|---|---|
| HX711 DOUT | Digital Pin 4 |
| HX711 SCK | Digital Pin 5 |
| Output 1 | Digital Pin 2 |
| Output 2 | Digital Pin 3 |

## Working Principle
1. The load cell senses the applied force or weight.
2. The HX711 module amplifies the small electrical signal from the load cell.
3. The microcontroller reads the digital output using the HX711_ADC library.
4. A calibration factor of 696.0 is used to convert the readings into calibrated load values.
5. The measured value is compared with a threshold of 30.
6. If the measured value is greater than 30, digital pin 2 is set HIGH and pin 3 is set LOW.
7. Otherwise, digital pin 2 is set LOW and pin 3 is set HIGH.

## Software Requirements
- Arduino IDE
- HX711_ADC library
- EEPROM library (included conditionally in the code)

## Features
- Load measurement using a strain gauge load cell.
- Signal amplification using the HX711 module.
- Calibrated load readings through serial communication.
- Automatic comparison with a predefined threshold.
- Two digital outputs for load status indication.
- Tare functionality through the serial monitor by sending the character `t`.

## Calibration
The calibration factor used in the current program is:

`696.0`

This value may need to be adjusted depending on the load cell and calibration procedure.

## Applications
- Electronic weighing systems
- Load monitoring systems
- Industrial weight measurement
- Force measurement applications
- Basic overload indication systems

## Future Improvements
- Display measured load on an LCD or OLED.
- Add wireless monitoring using Wi-Fi or Bluetooth.
- Implement adjustable load thresholds.
- Improve calibration accuracy.
- Store measurement data for analysis.

## Author
Irene Susan Bobby

## License
This project is available for educational and learning purposes.
## Project Hardware

The following images show the hardware setup and implementation of the strain gauge-based load measurement system.

### Hardware Setup 1
![Strain Gauge 1](images/Strain%20Gauge%201.jpeg)

### Hardware Setup 2
![Strain Gauge 2](images/Strain%20Gauge%202.jpeg)

### Hardware Setup 3
![Strain Gauge 3](images/Strain%20Gauge%203.jpeg)
