# DTECH USB to TTL Serial Cable (6-pin)

## Overview

USB to UART adapter cable with FT232RL chipset and 3.3V TTL signal levels.

## Pinout

| Pin | Name | Color  | Description |
|-----|------|--------|-------------|
| 1   | GND  | Black  | Ground |
| 2   | CTS  | Brown  | Clear to Send |
| 3   | VCC  | Red    | +5V output (typically leave disconnected) |
| 4   | TXD  | Orange | Transmit data |
| 5   | RXD  | Yellow | Receive data |
| 6   | RTS  | Green  | Request to Send |

## Wiring to Jetson Orin Nano (J14)

| Cable | J14 Pin | Signal |
|-------|---------|--------|
| Black (GND) | 7 | GND |
| Orange (TXD) | 3 | UART2_RXD |
| Yellow (RXD) | 4 | UART2_TXD |

Leave VCC, CTS, and RTS disconnected.

## Usage

```bash
# macOS
screen /dev/tty.usbserial-* 115200

# Linux
screen /dev/ttyUSB0 115200
```

To exit screen: `Ctrl-a` then `k`, then `y` to confirm.
