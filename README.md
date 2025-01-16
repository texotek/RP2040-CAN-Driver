A driver to run the MCP2515.  

## Introduction
This driver was modified for the SYT Class TGM 24/25.
The drivers `main.c` example now sends and receives messages delayed.

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

You will need 2 RP-Pico base on the RP2040 Chip and 2 MCP2515 to complete this example.
Now connect the 2 MCP2515 via CAN Low and CAN High to make them speak to each others.

## Building the driver
```
git clone https://github.com/texotek/RP2040-CAN-Driver
cd RP2040-CAN-Driver

mkdir build # Creating build folder
cmake ..    # Cmake configuration

make        # Compilation
```
