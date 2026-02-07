# NVIDIA Jetson Orin Nano Developer Kit

## Overview

Entry-level edge AI development board based on the NVIDIA Jetson Orin Nano module.

## Serial Console Access

The debug UART is on the **J14 button header** (not the 40-pin GPIO header).

| J14 Pin | Signal | Description |
|---------|--------|-------------|
| 3 | UART2_RXD | Debug RX (connect adapter TXD) |
| 4 | UART2_TXD | Debug TX (connect adapter RXD) |
| 7 | GND | Ground |

Serial settings: 115200 8N1 (115200 baud, 8 data bits, no parity, 1 stop bit)

All signals are **3.3V TTL** level.

## Headers

- **J12**: 40-pin GPIO expansion header (Raspberry Pi HAT compatible)
- **J14**: Button header (power, reset, recovery, debug UART)

## SSH Access

Hostname: `jetson.local`

```bash
ssh jdjones@jetson.local
```

To enable passwordless login, copy your SSH key:
```bash
ssh-copy-id jdjones@jetson.local
```

## Documentation

- [Carrier Board Specification (PDF)](https://developer.nvidia.com/downloads/assets/embedded/secure/jetson/orin_nano/docs/jetson_orin_nano_devkit_carrier_board_specification_sp.pdf)
- [Developer Kit User Guide](https://developer.nvidia.com/embedded/learn/jetson-orin-nano-devkit-user-guide/hardware_spec.html)
- [JetsonHacks GPIO Pinout](https://jetsonhacks.com/nvidia-jetson-orin-nano-gpio-header-pinout/)
