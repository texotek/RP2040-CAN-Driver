A driver to run the MCP2515.  

## Introduction
This driver was modified for the SYT Class TGM 24/25.
The drivers `main.c` example now sends and receives messages delayed.

You will need 2 RP-Pico base on the RP2040 Chip and 2 MCP2515 to complete this example.
Now connect the 2 MCP2515 via CAN Low and CAN High to make them speak to each others.

![RP Picos with MCP2515s](./img/image.jpg)

In the serial output you will see the received and sent message that are incremented by one
in each exchange.

```
Sent Message: 395 Received Message: 401

Sent Message: 396 Received Message: 402

Sent Message: 397 Received Message: 403

Sent Message: 398 Received Message: 404

Sent Message: 399 Received Message: 405

Sent Message: 400 Received Message: 406

Sent Message: 401 Received Message: 407
```

Here the logic analyzer output is diplayed. The CAN Packets are displayed here.
NOTE: The can_error message only appear because logic analyzer interprets them as such because the CAN protocol defines 5 bits sequentially send as high as an error.

![Logic Analyzer image](./img/logicanalyzer.jpg)

## Building the driver

To build the driver you will need the `PICO_SDK_PATH` variable set that points to the installed pico sdk.

And you will need `cmake`, `make`, `arm-gcc-noabi`.

```
git clone https://github.com/texotek/RP2040-CAN-Driver
cd RP2040-CAN-Driver

mkdir build # Creating build folder
cmake ..    # Cmake configuration

make        # Compilation
```
