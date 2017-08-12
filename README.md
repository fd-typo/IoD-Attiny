# IoD-Attiny
Interrupt driven Attiny for ESP8266

We use an Attiny 45 (final Attiny 25) in deep sleep mode. An sensor switch causes an interrupt on port change that will wake up the Attiny. The tiny then switches on the supply for an ESP8266 utilizing a P-channel MOSFET. After publishing the current switch state via MQTT the ESP signaling end of transfer to the Tiny, causing a power off of the ESP and deep sleep of the Tiny.

Quiescent current is about 0,12 µA guaranteeing a long battery life.
