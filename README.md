Here’s an updated README file for your Pong project, incorporating details about the STM32 microcontroller and its role in detecting hand proximity for paddle control.

---

# Pong Game Project

This repository contains a modified version of the classic Pong game, implemented in Python and utilizing an STM32 microcontroller to detect hand distance from electrodes. This project, developed as part of a school prototyping module, demonstrates a novel control method where players manipulate game elements using hand gestures.

## Overview

The project combines a classic arcade game with capacitive sensing technology, creating a unique interaction where each player controls their paddle through hand movements detected by an STM32 microcontroller and metal electrodes.

### Features
- **Capacitive Sensing Control:** The game reads hand proximity data from electrodes, allowing each player to control their paddle based on their hand’s distance.
- **STM32 Microcontroller Integration:** The STM32 controller measures the hand's proximity and transmits data via UART to the game.
- **Two-Player Mode:** Supports two players with independent hand sensors for competitive gameplay.
- **Real-Time Score Tracking:** Displays updated scores and messages for player interactions.

## Setup and Installation

### Requirements
- **Python 3.x**
- **Libraries:** Pygame and PySerial

Install dependencies with:
```bash
pip install pygame pyserial
```

### Running the Game
Execute the following command to start the game:
```bash
python pong.py
```

## Game Controls
Each player controls their paddle by adjusting their hand distance:
- **Left Paddle (Red Player):** Moves up or down based on hand distance from the first sensor.
- **Right Paddle (Blue Player):** Moves up or down based on hand distance from the second sensor.

In-game:
- **Press `Space`** to start the game.
- **Press `R`** to restart after a game ends.
- **Press `Esc`** to quit the game.

## System Components

1. **STM32 Microcontroller:** Configured to measure distance from the metal plates (acting as capacitive electrodes). The main controller code, `main.c`, handles input capture, timer configuration, and UART communication.
2. **Proximity Detection:** The STM32 captures timer data reflecting the distance from each player’s hand to the electrode and sends this data to the game via UART for real-time paddle adjustments.
3. **Python Game Engine:** The game logic and display are handled by Pygame, which reads sensor data to adjust paddle positions dynamically.

## How It Works

The STM32 microcontroller reads capacitive sensor data:
- The controller’s timers measure variations in capacitance due to hand proximity to the metal plates.
- These values are processed and transmitted over UART to the game, where paddle positions adjust based on the data.

### STM32 Firmware Files
- **main.c:** Primary code managing timers, UART communication, and data transmission.
- **stm32f3xx_it.c:** Interrupt handling for UART communication.
- **stm32f3xx_hal_msp.c:** Initializes peripherals like DMA and GPIO for handling sensor and communication tasks.

## Images
Include images showing the following:
- **System Diagram**: Diagram of the capacitive sensing setup.
- **Game Interface**: Screenshots of the game.
- **Hardware Setup**: Photos or diagrams showing the STM32 setup with metal plates.

## License
This project is open-source and available under the MIT License.

---

Place the images in an `images` folder within your repository and update the paths in the README as needed. This will give potential users and collaborators a comprehensive view of how the system is set up and functions.
