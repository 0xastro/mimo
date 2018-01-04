# mimo
This repository is a playground for MIMO experiments, the target is to build a gr-mimo out of tree module for GNU Radio to enable the MIMO expermints.

## TestBed Toplogy

1. `Two PCs with a free gigabit Ethernet port.`
2. `Two USRPs N series (Directly Connected via MIMO Cable) configured as transmitters.`
3. `Two USRPs N series (Directly Connected via MIMO Cable) configured as receivers.`

Each pair are directly connected with a MIMO cable, which shares Ethernet connectivity and common 10 MHz/PPS signals. 

<p align="center">
  <img src="https://github.com/astro7x/mimo/blob/master/pics/Mimotestbed?raw=true"/>
</p>

## Software Configuration

Transmitter pairs are configured to generate 2 streams -single tone- to be transmitted over the air.

The settings configurtion of Reciever Side:
+ The first USRP (Mb0) is set to use its default reference for clocking and timing.
+ The second USRP (Mb1) is configured to accept its frequency and timing reference from the MIMO cable. 
