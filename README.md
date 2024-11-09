# Pong Game Project

This repository contains a modified version of the classic arcade game Pong, implemented in Python. This project was developed as part of a prototyping module at school, showcasing the use of capacitive sensing technology to control game elements. Each player controls their paddle using proximity sensors, allowing them to move their paddle up or down based on hand distance from an electrode sensor.

## Overview

This project is based on a smart controller prototype designed to simulate a game controller using capacitive electrodes. The aim was to create a responsive and interactive gaming experience by using hand movements to control in-game objects.

### Features
- **Capacitive Sensor Control:** Each player's paddle is controlled by moving their hand closer to or farther from a designated electrode.
- **Two-Player Game:** The game allows two players to compete against each other.
- **Score Tracking:** Real-time score updates for each player.
- **Responsive Controls:** Paddle movement dynamically adjusts based on hand distance from the sensor, creating an immersive gaming experience.

## Setup and Installation

### Requirements
- Python 3.x
- Pygame library
- Serial communication library for Python

Install dependencies with:
```bash
pip install pygame pyserial
```

### Running the Game
To start the game, run:
```bash
python pong.py
```

## Game Controls
Each player can control their paddle with proximity sensors:
- **Left Paddle (Red Player):** Moves up or down based on hand distance from the first sensor.
- **Right Paddle (Blue Player):** Moves up or down based on hand distance from the second sensor.

In-game instructions:
- **Press `Space`** to start.
- **Press `R`** to restart after a game ends.
- **Press `Esc`** to quit the game.

## Project Structure

- **pong.py**: Contains the main code to run the game.
- **images/**: Directory with screenshots and diagrams of the system setup (add relevant images here).

## System Architecture

1. **Sensor Module:** Utilizes capacitive electrodes to detect hand movement.
2. **Communication Protocol:** The STM32 microcontroller captures sensor data and sends it to the game via serial communication.
3. **Game Logic:** The Python game engine reads sensor values to adjust paddle positions in real-time, using Pygame for visual display.

## How It Works

The game interacts with sensor data collected via serial communication:
- The hand distance is detected by the electrode sensors and converted into paddle movement.
- Paddle positions update in real-time as hand positions change, allowing each player to control their paddle with proximity gestures.

## Images
Include relevant images here, such as:
- **System Diagram**: A general overview of the capacitive sensing setup.
- **Game Interface**: Screenshots of the game in action.
- **Sensor Integration**: Photos or diagrams showing the sensors and electrode placement.

## License
This project is open-source and available under the MIT License.
