# Hybrid Windmill - WRO2021 Elementary Open Category Mentoring Elementary (8-12 years)
Hybrid Windmill - WRO2021

## Introduction
The Hybrid Windmill project was developed for the WRO2021 Elementary Open Category competition held in Almaty, 2021. The project aims to address the global problem of resource depletion by introducing a hybrid windmill capable of generating energy from both air and water sources. This repository contains the code and documentation for the Hybrid Windmill project.

## Motivation
With the increasing consumption of fossil fuels, our planet's resources are depleting rapidly. Green energy solutions, such as windmills, have been introduced to tackle this problem. However, traditional windmills are ineffective when there is no wind, leading to wasted resources. The Hybrid Windmill overcomes this limitation by incorporating a mechanism that allows it to operate from both air and water sources.

## Features
Capable of operating from both air and water sources.
Increased efficiency compared to traditional windmills.
Two operational modes: standard mode for generating energy from wind and water mode for generating energy from water flow.
Augmented reality mobile application for demonstration purposes.
Real-time data transmission using Bluetooth modules and Arduino.
## Working Mechanism
The Hybrid Windmill consists of a wind turbine, blades, a conveyor, and a platform. It operates in two modes:

Standard Mode (Wind): When the wind blows, the windmill operates in the standard mode. The blades of the wind turbine are positioned perpendicular to the wind to maximize energy generation.

Water Mode: In the absence of wind, the windmill lowers the wind turbine into the water. The blades of the wind turbine are positioned perpendicular to the water flow, increasing the area of interaction with the water to generate energy from the flow.

Augmented Reality
To demonstrate the Hybrid Windmill, an augmented reality mobile application was developed using the Vuforia engine. The application utilizes image recognition to detect a predefined marker and overlay the windmill model in an augmented reality environment.

Data Transmission
The data from the mobile application is transmitted to the windmill using Bluetooth modules and Arduino. The Arduino receives the data and controls the windmill's operations accordingly. LED lights are used for real-time data visualization.

Code
EV3 Loop Code
```python
while True:
    data = receive_data_from_arduino()  # Receive data from Arduino through LED
    if data == 1:
        rotate_blades_for_wind_mode()  # Rotate blades for wind mode
    elif data == 2:
        rotate_blades_for_water_mode()  # Rotate blades for water mode
    check_turbine_position()  # Check the distance between turbine and Earth
Arduino Loop Code
```
```c++
void loop() {
    int data = receive_data_from_bluetooth();  // Receive data from Bluetooth
    if (data == 1) {
        turn_on_led();  // Turn on LED for wind mode
    } else if (data == 2) {
        turn_off_led();  // Turn off LED for water mode
    }
}
```
## Conclusion
The Hybrid Windmill project represents a significant advancement in energy generation technology. By harnessing both air and water sources, it surpasses the efficiency of traditional windmills and offers a sustainable solution to the global resource depletion problem. Thank you for your attention, and we are proud to present the Hybrid Windmill developed by the Hybrid team!

Hybrid Team
