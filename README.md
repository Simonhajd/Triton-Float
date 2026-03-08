# Triton Float

Development repository for the 2026 Triton Robotics Float.



## Overview


The Triton Float is being developed for the 2026 MATE ROV Pioneer competition (Newfoundland).
This design iteration is approximately 33% smaller than last year's model, while targeting more than 2× performance improvements in speed and significantly increased precision through layered redundancy and sensor feedback systems. It also includes a dedicated LoRa radio as opposed to last year's 4cm wire antenna, which will increase the reliability and robustness of the system.



## Features

Dimensions: 200mm x 4 in diameter.
Buoyancy system: PWM pump ranging from 220mL/min to -220mL/min.

Accuracy Strategy:

- Internal pressure sensor for ballast state verification  
- Pump movement feedback sensor for closed-loop control  
- Pre-calibrated pump flow rate modeling for predictive adjustment
- Additional onboard MCU sensors for reproducible control accuracy
  


## Hardware / Electrical

- Microcontroller: XIAO nRF52840 Sense  

- Sensors:  
  - XIAO nRF52840 Sense onboard IMU & sensors  
  - Blue Robotics Bar02  
  - Internal pressure sensor  
  - Pump movement sensor  

- Power System:  
  Custom voltage regulation system controlled via relay and magnetic hall-effect sensor on a secondary accessory PCB  

- PCB Revisions:  
  R2 completed, R3 in development



## Mechanical Design

Fusion / CAD link:
🔗 [View Fusion 360 CAD](https://a360.co/4slAPcB)

Notes:
### Structural Considerations:

Cylindrical housing designed to fit within a 4 in diameter constraint

Internal layout arranged to allow operation in the case of flooding (up to ~50-75% of internal volume) while maintaining core electronic functionality.

PCB mounted using tight-tolerance standoffs to prevent movement under vibration and ease serviceability

Layer system used to keep the float intact when the top flange and shell is removed.

### Integration Notes:

Limited internal volume required careful routing of wiring and tubing

Added solderable vias for power, in order to have a secure connection to the battery.

Accessory PCB used to isolate power regulation from main control logic

R3 revision addresses footprint issues and uses a different simpler power system for a working prototype.



## Current Status

- Version / Revision: R2
- In progress: R3, with fixed tracing and the internal pressure sensor.
- Completed: R2.
- Next steps: Testing R3 when it comes in.



## Tools 

- PCB software: KiCad
- CAD software: Fusion 360
- Firmware tools: C++



## Images
<img width="220" alt="Screenshot 2026-02-16 at 4 56 35 PM" src="https://github.com/user-attachments/assets/93eaf852-09b1-407b-b515-f2f914b68fb8" />




