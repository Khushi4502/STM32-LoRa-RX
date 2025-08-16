#  STM32 LoRa RX Example

This project demonstrates how to use **STM32L051C8Tx** with an **EByte LoRa module (E32/E220)** for **data reception (RX)**.  
It continuously listens for incoming LoRa packets and prints debug messages over UART.

---

##  Hardware

- **MCU**: STM32L051C8Tx (tested)  
- **LoRa Module**: EByte E32/E220 (433/868/915 MHz)  
- **LEDs**: Indicators for RX status  
- **Power**: 3.3V  

---

##  Pin Connections

| STM32 Pin | Function      | LoRa Pin |
|-----------|--------------|----------|
| PA2       | USART2_TX    | RXD      |
| PA3       | USART2_RX    | TXD      |
| PB14      | MODE0 (M0)   | M0       |
| PB4       | MODE1 (M1)   | M1       |
| PB15      | AUX (INT)    | AUX      |
| 3.3V      | VCC          | VCC      |
| GND       | GND          | GND      |

---

##  Pin Diagram

<img width="543" height="498" alt="Screenshot 2025-08-16 232411" src="https://github.com/user-attachments/assets/c568c63b-c8b1-4de4-ae13-465dd1a35d12" />


*(This shows the STM32L051C8Tx with LoRa connections)*

---

## Features

- Continuously listens for incoming LoRa packets  
- Prints **received packet data + counter value** over UART2 (for monitoring on serial terminal)  
- LED1 → Turns ON when packet is successfully received  
- LED2 → Blinks if valid packet received (indicates activity)  
- Handles both **fixed packet size (4 bytes)** and dynamic messages  

---
