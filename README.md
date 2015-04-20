Optiboot for nRF24L01+
======================

This is a modifed Optiboot bootloader for Arduino.  The feature added are:

*   Flash from SD card that has been updated using the radio transreceiver - nRF24L01+.

The nRF24L01+ is a cheap SPI radio transciever chip that works in simplex mode (can't receive
and transmit at the same time, unlike serial communication).  This version of optiboot can
receive commands from a program like avrdude or an Arduino IDE either through serial or
through the nRF24L01+ chip if one is connected.  Over serial it behaves as normal.

The nRF24L01+ modules (PCB with the radio chip, antenna and a few other things) can be had
for less than $1 from the likes of ebay.  Add an Arduino clone for $2.50 and it's a wireless
Arduino for $3.50.

Optiboot
========

Optiboot is a minimal Arduino bootloader that takes only around 500 bytes of your Flash memory
instead of the 2 kB the default bootloader needs.  I believe it ships with the Arduino IDE
in more recent versions so you can replace the default bootloader on your Arduino board with
it if you want.  See optiboot/bootloaders/optiboot/README.TXT for more information.

This repository was forked from https://code.google.com/p/optiboot/ using fast-export for
Mercurial to Git conversion.

Building
========

To build a normal optiboot for an atmega328 just run:

    $ make atmega328
