# Pollution-Monitoring-system-using-IoT
A basic system which measures the temperature and humidity also the gas sensor readings and displays it back on the LCD screen.

## Introduction

The Pollution Monitoring System is a critical solution aimed at addressing the pressing issue of air pollution. With the rapid industrialization, urbanization, and increase in vehicular traffic, the levels of air pollutants such as CO, CO2, SO2, NO2, O3, and volatile organic compounds have risen significantly, posing serious health risks to the population. This project leverages Internet of Things (IoT) technology and hardware to develop a simple, reliable and cost-effective system for monitoring air quality parameters in real-time.

## Hardware and Software Components

### Hardware Components:
1. Arduino UNO: Core microcontroller board for project implementation.
2. Gas Sensor MQ 135: Detects various gases, including CO2 and volatile organic compounds.
3. Gas Sensor MQ 7: Specifically designed for carbon monoxide (CO) detection.
4. DHT 22 Sensor: Digital temperature and humidity sensor for environmental monitoring.
5. I2C Serial Interface Adapter: Facilitates communication with LCD display.
6. LCD Display: Provides visual output of sensor data.
7. Breadboard and Jumper Wires: Prototyping tools for circuit connections.

### Software Components:
1. Arduino IDE: Integrated Development Environment for programming the Arduino microcontroller.
2. Libraries: dht.h, LiquidCrystal_I2C.h, and MQ135.h for interfacing sensors and LCD display.
3. TinkerCAD: Web-based platform that offers a range of tools for designing, simulating, and creating electronic circuits and 3D models

## Architecture

The architecture of the Air Quality Monitoring System consists of interconnected hardware and software components. The sensors, including MQ 135, MQ 7, and DHT 22, are connected to the Arduino UNO microcontroller, which processes data and transmits it to the LCD display for visualization. Power and ground connections ensure proper functionality of the components. The system enables real-time monitoring of air quality parameters such as temperature, humidity, carbon monoxide levels, and other harmful gases. Leveraging IoT technology, this architecture provides a scalable and cost-effective solution for monitoring and mitigating air pollution.

