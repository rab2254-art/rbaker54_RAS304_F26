

# RAS 304 Individual Datasheet

## Rebecca Baker

**Robotics and Autonomous Systems — Arizona State University**

**Fall 2026 | External Design Review**

---

## About Me

My name is Rebecca Baker, and I am studying Robotics and Autonomous Systems at Arizona State University.

This website documents my individual work for RAS 304, including my assigned hardware, component research, block diagram, electrical schematic development, bill of materials, and power budget.

## Project Overview

Our team, Team 102, is designing one functional robotic leg for a six-legged spider robot.

The leg uses multiple actuators and sensors to control joint movement and provide feedback. The overall design uses four PIC18F57Q43 Curiosity Nano development boards, with each board responsible for a different part of the system.

My assigned subsystem is **Driver Nano 2**.

## My Responsibilities

Driver Nano 2 is responsible for controlling one of the leg's linear actuators and monitoring its assigned sensors.

| Component or Function | My Responsibility |
|---|---|
| PIC18F57Q43 Curiosity Nano | Main controller for my subsystem |
| Linear Actuator A | Control extension, retraction, and stopping |
| Motor Driver | Interface between the PIC and actuator |
| Pressure Sensor | Read pressure or contact information |
| Limit Switches | Monitor the actuator's permitted travel |
| UART Communication | Receive commands and return feedback |
| Electrical Schematic | Document subsystem connections |
| Power Budget | Determine electrical requirements |

The main controller, managed by Preston, handles kinematics and overall system coordination. My board receives movement commands from that controller and manages its assigned hardware.

## How My Subsystem Works

The proposed operation is:

1. The main Nano calculates the requested joint movement.
2. My Nano receives the movement command through UART.
3. My software checks the command and relevant limit switches.
4. The PIC sends control signals to the actuator driver.
5. The driver controls the actuator using the required motor power.
6. My Nano reads pressure and limit-switch information.
7. My Nano sends feedback or fault information to the main controller.

This sequence represents the intended operation. It still needs to be implemented and verified with the selected hardware.

## Individual Design Documentation

| Section | Description |
|---|---|
| [Block Diagram](01-Block-Diagram/Block-Diagram.md) | Subsystem organization and connections |
| [Component Selection](02-Component-Selection/Component-Selection.md) | Hardware options and selection reasoning |
| [Bill of Materials](03-BOM/BOM.md) | Components required for Driver Nano 2 |
| [Schematic Design](04-Schematic/schematic.md) | Planned electrical connections and schematic development |
| [Power Budget](05-Power-Budget/Power-Budget.md) | Voltage, current, and power requirements |

## Software and Engineering Tools

- MPLAB X IDE and Microchip development tools
- Visual Studio Code
- Git and GitHub
- Electrical schematic design software
- Microcontroller programming and debugging tools
- Multimeter, oscilloscope, and bench power supply for future testing

## Current Design Status

The subsystem responsibilities and proposed architecture have been identified.

The next steps are to confirm the actuator and driver specifications, complete the individual schematic, determine power requirements, configure the PIC peripherals, and test communication, sensing, and actuator control.

## Related Project Links

- [Team 102 Website](https://ras304-fall26-102.github.io/)
- [Individual GitHub Repository](https://github.com/rab2254-art/rbaker54_RAS304_F26)

---

**Student:** Rebecca Baker

**Course:** RAS 304

**Semester:** Fall 2026

**University:** Arizona State University
