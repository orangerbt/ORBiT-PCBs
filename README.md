#ORBiT Avionics

Schematics and PCBS for ORBiT Avionics system.

## Modules

- Telemetry (GPS, IMU, atmospheric conditions, remote control)
- Power (battery management, charging, regulation)
- Actuation (power devices)
*********************************************

## Notes

- Make sure to power down HDMI framer via I2C0
- Add CAT24C256 EEPROMs to identify modules via I2C2
- Add RTC to telemetry board
- Add connector for ADIS IMU to telemetry board
- Add power sequencing to all boards
- Data acquisition to be based on PRUDAQ
- Add LTC2983/4/6 to DAQ???

## Hardware pin mapping

### Telemetry

- UART4 - P8 33 uart4_rtsn, 35 uart4_ctsn 							P9 11 uart4_rxd, 13 uart4_txd
- UART5 - P8 31 uart5_ctsn, 32 uart5_rtsn, 37 uart5_txd, 38 uart5_rxd
- SPI0 -	P8 26-28													P9 17 spi0_cs0, 18 spi0_d1 , 21 spi0_d0 , 22 spi0_sclk
    - SPI0 addressing
    - P8 26 = gpio61 = A0
    - P8 27 = gpio86 = A1
    - P8 28 = gpio88 = A2

### Power management

- I2C1 - P9 24 I2C1_SCL, 26 I2C1_SDA

### Actuator control

- I2C1 - P9 24 I2C1_SCL, 26 I2C1_SDA
- GPIO - P9 25, 27, 28

### PRUDAQ:
- P8 27-30, 39-46
- P9 25-31
