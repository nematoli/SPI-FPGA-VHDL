# SPI-FPGA-VHDL
Serial Peripheral Interface (SPI) is a synchronous serial data protocol used for communication between digital circuits. Therefore with SPI interface FPGAs or microcontrollers can communicate with peripheral devices, sensors and also other FPGAs and microcontrollers quickly over short distances. 

In this implementation both SPI master and SPI slave components are written in VHDL and can be used for all FPGAs. 

# Features
* Configurable data length
* Configurable polarity and phase (All SPI Modes are supported)
* Configurable frequency

# SPI master

## Table of i/o ports:

Port name | IN/OUT | length [b]| Port description
---|:---:|:---:|---
CLK | IN | 1 | System Clock
reset_n | IN | 1 | Asynchronous Active Low Reset
enable | IN | 1 | Initiate Communication
cpol | IN | 1 | Clock Polarity Mode
cpha | IN | 1 | Clock Phase Mode
miso | IN | 1 | Master In Slave Out
sclk | OUT | 1 | Spi Clock
ss_n | OUT | 1 | Slave Select
mosi | OUT | 1 | Master Out Slave In
busy | OUT | 1 | Master Busy Signal
tx | IN | data_length | Data to Transmit
rx | OUT | data_length | Data Received

# SPI slave

## Table of i/o ports:
Port name | IN/OUT | length [b]| Port description
---|:---:|:---:|---
reset_n | IN | 1 | Asynchronous Active Low Reset
cpol | IN | 1 | Clock Polarity Mode
cpha | IN | 1 | Clock Phase Mode
sclk | OUT | 1 | Spi Clock
ss_n | OUT | 1 | Slave Select
mosi | IN | 1 | Master Out Slave In
miso | OUT | 1 | Master In Slave Out
rx_enable | IN | 1 | enable signal to wire rxBuffer to outside
tx | IN | data_length | Data to Transmit
rx | OUT | data_length | Data Received
busy | OUT | 1 | SLave Busy Signal

## License:

SPI Master and Slave components are available under the GNU LESSER GENERAL PUBLIC LICENSE Version 3.

