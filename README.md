# upskillcampus
# Smart Obstacle Detection and Automatic Motor Control System

## Project Overview

This project is an Embedded Systems application that uses an HC-SR04 Ultrasonic Sensor to detect obstacles and automatically control a DC motor. When an obstacle is detected within a predefined distance, the motor stops automatically to prevent collisions. If no obstacle is detected, the motor continues running.

## Objective

The objective of this project is to develop a simple obstacle detection system that can be used in robotics, industrial automation, and smart vehicle applications.

## Components Used

* Arduino Uno
* HC-SR04 Ultrasonic Sensor
* DC Motor
* Breadboard
* Jumper Wires
* Motor Driver (L298N/L293D recommended)

## Working Principle

1. The ultrasonic sensor continuously measures the distance to nearby objects.
2. The Arduino processes the distance data.
3. If the detected distance is less than 20 cm:

   * Motor is turned OFF.
   * Obstacle detection message is displayed on Serial Monitor.
4. If the distance is greater than or equal to 20 cm:

   * Motor is turned ON.
   * Path clear message is displayed on Serial Monitor.

## Circuit Connections

### HC-SR04 to Arduino

| HC-SR04 Pin | Arduino Pin |
| ----------- | ----------- |
| VCC         | 5V          |
| GND         | GND         |
| TRIG        | D9          |
| ECHO        | D10         |

### Motor Control

| Motor Driver Input | Arduino Pin |
| ------------------ | ----------- |
| IN1                | D7          |

## Arduino Code File

```text
ObstacleDetectionMotorControl.ino
```

## Expected Output

### Obstacle Detected

```text
Distance: 15 cm
Obstacle Detected -> Motor OFF
```

### Path Clear

```text
Distance: 35 cm
Path Clear -> Motor ON
```

## Applications

* Smart Vehicles
* Obstacle Avoidance Robots
* Industrial Conveyor Systems
* Automated Safety Systems
* Robotics Projects

## Future Scope

* Add Wi-Fi connectivity using ESP32.
* Send alerts to a mobile application.
* Integrate IoT cloud monitoring.
* Add buzzer and LED indicators.
* Implement autonomous robot navigation.

## Author

Dhruv

Industrial Internship Project

2026
