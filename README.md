# MAX30205 STM32 Demo

This repository contains a demonstration project for reading temperature from the **MAX30205** digital temperature sensor using an **STM32** microcontroller. The project is implemented with STM32 HAL libraries in C.

---

## Features

- Reads temperature from MAX30205 via **I2C**.
- Prints raw data and calculated temperature in Celsius to **UART1**.
- Simple initialization of GPIO, I2C1, and USART1.
- Demonstrates basic HAL usage and error handling.

---

## Hardware Requirements

- STM32 microcontroller (any STM32 with I2C and UART peripherals).
- MAX30205 temperature sensor.
- I2C wiring between STM32 and MAX30205.
- UART connection for debugging (e.g., USB-to-serial).

---

## Software Requirements

- STM32CubeIDE or STM32 HAL libraries.
- C compiler for STM32 (included in CubeIDE).

---

## Wiring

| STM32 Pin | MAX30205 Pin |
|-----------|--------------|
| I2C1_SCL  | SCL          |
| I2C1_SDA  | SDA          |
| 3.3V      | VDD          |
| GND       | GND          |

UART pins are optional for debug output.

---

## Usage

1. Open the project in **STM32CubeIDE**.
2. Build and flash to the STM32.
3. Open UART terminal at **115200 baud**.
4. Observe temperature readings in Celsius printed every 1 second.

---

## Code Overview

- **main.c**: main application code including HAL initialization, I2C/UART setup, and infinite loop for reading temperature.
- **MAX30205_Init()**: initializes the sensor.
- **MAX30205_Read()**: reads the temperature and prints debug info over UART.
- **Error_Handler()**: handles errors in HAL functions.

---

## License

This project is provided **as-is**. See the LICENSE file for details.
