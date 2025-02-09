# 🏡 IoT-Powered Smart Home Automation System

This repository presents the design and implementation of an IoT-powered Smart Home Automation System using various sensors and IoT platforms. It leverages real-time monitoring, automation and remote control to enhance home safety, energy efficiency and convenience.

## Contents

## Introduction

In today's world, managing home safety, energy efficiency and convenience can be challenging. Many homes lack an integrated system to automate daily tasks like adjusting lighting, monitoring air quality, detecting gas leaks and responding to environmental changes. This project introduces an IoT-powered smart home system that makes your living space safer, smarter and more efficient.

Traditional home management relies heavily on manual operation of lighting, ventilation and security systems. Homeowners must physically switch appliances on and off, monitor air quality through observation and rely on standalone smoke or gas detectors without centralized control. This fragmented approach often results in energy wastage, delayed hazard detection and overall inconvenience, making home management inefficient and at times, unsafe.

In contrast, the IoT-Powered Smart Home Automation System offers a modern, integrated solution to these challenges. It enables real-time monitoring, automation and remote control through IoT connectivity. By streamlining home management, the system improves safety, reduces energy consumption and simplifies daily tasks. This makes home operation more efficient, secure and convenient for homeowners.

## Overview

The IoT-Powered Smart Home Automation System is a sensor-driven, cloud-integrated solution designed to optimize energy efficiency, enhance safety and provide real-time remote monitoring for modern households. The system consists of a network of IoT-enabled sensors and actuators that continuously monitor environmental conditions and automate home functions based on real-time data analytics.

The system is structured around a central microcontroller (ARIES v3.0), which serves as the primary processing unit, collecting data from multiple sensors and executing automation commands. 

Key hardware components include:

✅ **Motion and Light Sensors** – Enable automated lighting and fan control based on occupancy and ambient lighting conditions. <br>
✅ **Temperature and Humidity Sensors** – Optimize ventilation and climate control. <br>
✅ **Fire and Smoke Detectors** – Detect leaks and fire hazards, triggering immediate safety alerts. <br>
✅ **Air Quality Sensors** – Monitor pollutants and adjust ventilation accordingly. <br>

To enable real-time data transfer and remote control, the system utilizes Blynk, a cloud-based IoT platform that facilitates intelligent automation of various smart home functions. A user-friendly web and mobile application, built using Blynk’s IoT framework, allows homeowners to monitor sensor data, control devices and receive instant alerts from anywhere.

In the event of a gas leak, fire or deteriorating air quality, the system immediately notifies homeowners via Blynk app alerts, email logs, and SMS notifications. Additionally, automated safety measures, such as ventilation control, are activated to mitigate risks and ensure timely hazard prevention.

This seamless integration of hardware, cloud connectivity and automation enhances home security, energy efficiency and overall convenience.

## Components Required

### Components List with Bill

| Item                          | Quantity | Description                                     | Links to Products |
|-------------------------------|----------|-------------------------------------------------|-------------------|
| **ARIES v3.0**          | 1        | Microcontroller board                          | [ARIES v3.0](https://robu.in/product/aries-v30-devlopment-board/) |
| **ESP8266 Wi-Fi Module**      | 1        | Wi-Fi module for communication                 | [ESP8266 Module](https://robu.in/product/nodemcu-cp2102-board/) |
| **MQ-135 Gas Sensor** | 1        | Air quality detection sensor                    | [MQ-135 Sensor](https://robu.in/product/waveshare-mq-135-gas-sensor/) |
| **DHT11 Temperature & Humidity Sensor** | 1 | Measures temperature & humidity                 | [DHT11 Sensor](https://robu.in/product/dht11-temperature-and-humidity-sensor-module-with-led/) |
| **HC-SR501 PIR Sensor**         | 1        | Detects motion                                  | [PIR Motion Sensor](https://robu.in/product/pir-motion-sensor-detector-module-hc-sr501/) |
| **ADIY Flame Sensor Module**       | 1        | Detects flame or fire                          | [Fire Sensor](https://robu.in/product/flame-sensor-infrared-receiver-module-ignition-source-detection-module/) |
| **Light Dependent Resistor (LDR) Module**                | 1        | Detects light intensity                         | [LDR Sensor](https://robu.in/product/5mm-ldr-sensor-photoresistor-photo-cell-100-200k-gl5549/) |
| **5V Piezoelectric Buzzer**                    | 1        | Alarm/Alert system                             | [Buzzer](https://robu.in/product/5v-passive-buzzer/) |
| **I2C 16x2 LCD Display**               | 1        | Displays information                            | [LCD Display](https://robu.in/product/lcd1602-parallel-lcd-display-with-iic-i2c-interface/) |
| **Jumper Wires**              | 1 set    | Male-to-male and female-to-male jumper wires   | [Jumper Wires](https://robu.in/product/20-cm-40-pin-dupont-male-male-male-female-female-female-cable-combo/) |
| **Micro USB Cable**           | 1        | For programming and power supply               | [Micro USB Cable](https://robu.in/product/10-inch-micro-usb-cable-a-to-micro-b/) |

## Pin Connections

### MQ-135 Air Quality Sensor
| Sensor Pin | ARIES v3.0 Pin | Function |
|-----------|---------------|----------|
| VCC | 3.3V | Power |
| GND | GND | Ground |
| AOUT (Analog Output) | ADC_CH1 (J10_4) | Air Quality Detection |


### DHT11 Temperature & Humidity Sensor
| Sensor Pin | ARIES v3.0 Pin | Function |
|-----------|---------------|----------|
| VCC | 3.3V | Power |
| GND | GND | Ground |
| DATA | GPIO3 (J2_16) | Temperature & Humidity |

### HC-SR501 PIR Sensor
| Sensor Pin | ARIES v3.0 Pin | Function |
|-----------|---------------|----------|
| VCC | 3.3V | Power |
| GND | GND | Ground |
| OUT | GPIO2 (J2_7) | Motion Detection |

### ADIY Flame Sensor Module
| Sensor Pin | ARIES v3.0 Pin | Function |
|-----------|---------------|----------|
| VCC | 3.3V | Power |
| GND | GND | Ground |
| OUT | GPIO4 (J2_14) | Fire Detection |

### Light Dependent Resistor (LDR) Module
| Sensor Pin | ARIES v3.0 Pin | Function |
|-----------|---------------|----------|
| One end of LDR | 3.3V | Power |
| Other end of LDR | ADC_CH0 (J10_2) | Light Intensity (Analog Input) |

### 5V Piezoelectric Buzzer
| Sensor Pin | ARIES v3.0 Pin | Function |
|-----------|---------------|----------|
| VCC | 3.3V | Power |
| GND | GND | Ground |
| Signal | GPIO5 (J2_18) | Alarm/Alert |

### I2C 16x2 LCD Display
| Sensor Pin | ARIES v3.0 Pin | Function |
|-----------|---------------|----------|
| VCC | 3.3V | Power |
| GND | GND | Ground |
| SDA | GPIO6 | Data Line |
| SCL | GPIO7 | Clock Line |

### ESP8266 Wi-Fi Module
| Sensor Pin | ARIES v3.0 Pin | Function |
|-----------|---------------|----------|
| VCC | 3.3V | Power |
| GND | GND | Ground |
| TX | RX (J3_2) | Transmit Data |
| RX | TX (J3_3) | Receive Data |

## Contributors
- Sree Vishnu Varthini S, Pre-Final Year Student, Sri Eshwar College of Engineering.
- Shanmuga Sanjeevi P S, Pre-Final Year Student, Sri Eshwar College of Engineering.
- Sri Krishna M, Pre-Final Year Student, Sri Eshwar College of Engineering.

## Acknowledgements
- Mr. Kunal Ghosh, Director, VSD Corp. Pvt. Ltd.
- Mr. Vignesh, Technical Trainer, Sri Eshwar College of Engineering

## Contact Information
- Sree Vishnu Varthini S, Pre-Final Year Student, Sri Eshwar College of Engineering, sreevishnuvarthini@gmail.com
- Shanmuga Sanjeevi P S, Pre-Final Year Student, Sri Eshwar College of Engineering, shanmugasanjeevi2004@gmail.com
- Sri Krishna M, Pre-Final Year Student, Sri Eshwar College of Engineering, srikrishna0017@gmail.com
- Mr. Vignesh, Technical Trainer, Sri Eshwar College of Engineering
- Mr. Kunal Ghosh, Director, VSD Corp. Pvt. Ltd., kunalpghosh@gmail.com

