# joirc

A small ESP-12F (ESP8266)-based project for DIY IR controller

## Description

Use IRController
(originally from [ESP8266-HTTP-IR-Blaster](https://github.com/mdhiggins/ESP8266-HTTP-IR-Blaster))
with NodeMCU (or IRCapture for Arduino Nano) and IR receiver to capture IR codes (usually RAW with length 48).
Use IRSender with ESP-12F and IR LED to send the codes.

IR receiver and transmitter modules are from 37-in-1 sensors set. 3.3V regulator is AMS1117-based.
Note that ESP12-F dies from 5V in about a week. NodeMCU modules are better (built in UART and 3.3V LDO) but they're a little bit expensive.

There are a few types of IR codes, I couldn't make short codes work on my devices so I went with raw ones (long sequences of numbers) sent at 38 KHz.
They ought to be [F12](http://www.hifi-remote.com/johnsfine/DecodeIR.html#F12) codes (download [IrScrutinizer](https://github.com/bengtmartensson/IrScrutinizer/releases/) to decode raw format).

You can also capture codes using [IrScrutinizer](https://github.com/bengtmartensson/IrScrutinizer/releases) with Arduino Nano
and [GirsLite 1.0.2](https://github.com/bengtmartensson/AGirs/releases)
firmware. Hook up IR receiver module to pins D5, GND and 5V, check "Use receive for capture" in the Girs client settings.
Export as Arduino Raw or Bracketed Raw.

## Video

[![](http://img.youtube.com/vi/UZf-yPra764/maxresdefault.jpg)](https://youtu.be/UZf-yPra764)

## Pictures

* https://imgur.com/a/qzOVUFb

## Web

* https://joric.github.io/joirc

## References

* https://joric.github.io/joirc
* https://imgur.com/a/qzOVUFb
* https://www.techdesign.be/projects/011/011_waves.htm
* https://clearwater.com.au/code/rc5
* http://www.hifi-remote.com/johnsfine/DecodeIR.html
* https://github.com/probonopd/irdb
* https://github.com/bengtmartensson/IrScrutinizer
* https://github.com/bengtmartensson/AGirs
* https://github.com/probonopd/decodeir
