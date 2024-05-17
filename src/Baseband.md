# Baseband

ESP32 basebands implement the PHY (Physical Layer) of WiFi and Bluetooth. Each baseband is it's own peripheral and is controlled individually.


## WiFi

The WiFi peripheral on the ES32 is controlled by two FreeRTOS tasks, one of which handles the MAC (Medium Access Control) and the other one the PHY (Physical Layer).

They interface with each other through a number of message queues, on top of which an `ioctl`-interface exists.

Espressif chose a SoftMAC architecture for the ESP32, with only ACKing implemented in hardware.
