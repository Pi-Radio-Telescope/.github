# PiRaTe - The Pi Radio Telescope

## Overview
This is a collection of repositories mainly around an Az/Alt mount radio telescope originally written for the 3m radio antenna at the astronomical observatory in Radebeul/Dresden (Germany) but may be utilized for similar instruments. 

The main features are:
* The hardware is based on Raspberry Pi (tested for model 4) connecting via GPIOs to easy-to-acquire ubiquitous periphery modules for motor control, position sensing, GPS reception, I/O, ADCs etc. The employed components and connections are documented on this page: https://oshwlab.com/antrares/pirate-mainboard
* The abstraction to the hardware is managed through a custom Instrument-Neutral-Device-Interface (INDI) driver, which allows access to the scope through the quasi-standard XML-message-based INDI protocol. INDI is utilized in many remote observatories and enjoys a large community. The RPi-based PiRaTe INDI driver is found in the repository https://github.com/Pi-Radio-Telescope/indi-rpi-radiotelescope.
* An observation task manager (Radio Telescope Task Scheduler - RaTSche) which runs as daemon and manages tasks such as measurements, parking, maintenance etc. New tasks are added through a message queue interface e.g. through the included command-line-interface (CLI) client which allows easy integration into web-based interfaces. RaTSche is also part of the main repository under https://github.com/Pi-Radio-Telescope/indi-rpi-radiotelescope.
* A simple visualization front-end for intensity data acquired with the radio telescope https://github.com/Pi-Radio-Telescope/RTData.
* Web-Front-Ends for control and data visualization of the radio telescope

