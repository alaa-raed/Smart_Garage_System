# Automated Garage System

## Overview

Welcome to the **Automated Garage System** project! This system integrates multiple sensors and components to create an intelligent and secure garage management solution. It automates garage door operations, monitors temperature, and ensures access control.

## Components

### Microcontrollers
- **Atmega32** (2 units)

### Sensors
- **Temperature Sensor**: LM35
- **RFID Sensor**
- **IR Sensors**: 2 units

### Actuators
- **Servo Motor**
- **LEDs**: 7 units
- **Buzzers**: 2 units

### Displays
- **LCD Displays**: 2 units

## Features

- **Automatic Garage Door Operation**
  - **Entry**:
    - The first IR sensor detects a car.
    - The RFID scanner reads the car's ID.
    - If authorized, the servo motor opens the garage door.
    - The door closes after the car is inside.
  - **Exit**:
    - The second IR sensor detects a car leaving.
    - The garage door remains open until the car exits.

- **Temperature Monitoring**
  - Alerts with a buzzer and fire LED if the temperature exceeds 40°C.

- **Car Presence Indicators**
  - Four LEDs indicate the presence of a car in the garage: on when a car is detected, off when empty.

- **Unauthorized Access**
  - If an unauthorized car attempts entry, the servo motor does not rotate, and a buzzer sounds.

## Drivers and Libraries

- **DIO**: Digital Input/Output control
- **TIMER1**: Timer management
- **UART**: Serial communication
- **SPI**: Serial Peripheral Interface
- **ADC**: Analog-to-Digital Conversion
- **LCD**: LCD display management
- **INTERRUPT**: Interrupt handling
- **GIE**: Global Interrupt Enable

## Installation and Setup

1. **Hardware Setup**
   - Connect sensors, actuators, and displays to the Atmega32 microcontrollers as outlined in the circuit diagram.

2. **Software Setup**
   - Load the provided code onto the Atmega32 microcontrollers using an appropriate programmer.
   - Configure and calibrate the sensors according to your environment.

3. **Operation**
   - Power the system.
   - Verify each component's functionality individually.

## Contributing

Contributions are welcome! Please fork the repository, make improvements, and submit pull requests. For issues or feature requests, open an issue in this GitHub repository.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

Thanks to the open-source community for their invaluable libraries and tools.
