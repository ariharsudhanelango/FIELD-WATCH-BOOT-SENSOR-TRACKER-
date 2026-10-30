# FieldWatch: Boot Sensor and Tracker

A simulation of a boot-mounted motion sensing system that turns every step
into a live heading, bearing and track on a command screen.

## How it works
Sense → Filter → Link
- Sense: ICM-20948 motion unit captures acceleration and rotation
- Filter: STM32F407 applies a low-pass filter and packs readings with a checksum
- Link: LR900 radio relays packets to command, where corrupt ones are rejected

## Features
- Field Unit: drag on a forest map to simulate walking (8 Hz updates)
- Command Console: live heading, bearing and dead-reckoning track log
- Packet and checksum-error counters
- Demo motion mode, no hardware needed

## Tech
HTML, CSS, JavaScript, Canvas

## Note
Educational demo. A touch pad stands in for the real boot hardware.
Dead-reckoning position drifts. Not for navigation or safety decisions.
