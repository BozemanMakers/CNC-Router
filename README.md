# CNC-Router

A repository to hold documentation and configuration related to the Bozeman Makerspace's CNC router.

## Technical Info

**New Controller:** 6 Pack CNC Driver w/ External controllers

**External Drivers:** DM542T 4.2A Drivers

**PSU:** Meanwell 24V PSU

**Firmware:** FluidNC for ESP32


## Usage

In order to run this controller with [Easel](easel.inventables.com), the patched USB driver from Samyk is necessary. Find it [here](https://github.com/samyk/easel-driver).

## Known Issues

### Homing doesn’t work in Easel

Option 1: Don’t home, be careful to not exceed the machine’s limits when setting work zero. You can still jog the machine around, just try not to crash into the hard limits.
Option 2: Run $H in a gcode sender of your choice

### Easel can’t see the CNC Machine

Fix this by turning off the CNC machine, and (crucially) unplugging and replugging the USB cable on the computer. This should be pretty rare.

### The Easel Driver has an OSS patch applied to make it work

Because of this, you should run Easel from the connected shop computer (and please, do not update the driver if asked to!) If you’re feeling adventurous or must run Easel from your machine, message Spencer C on Slack for instructions.
