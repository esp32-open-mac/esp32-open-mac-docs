# Architecture

```mermaid
block-beta
    columns 2
    block:wifi["Wi-Fi"]:1
        columns 1
        wifimac["Wi-Fi MAC"]
        wifibb["Wi-Fi Baseband"]
    end
    block:bt["Bluetooth"]:1
        columns 1
        btlc["Bluetooth Link Controller"]
        btbb["Bluetooth Baseband"]
    end
    block:rf["Radio frequency"]:2
        clkgen["Clock generator"]
        switch["Switch"]
        balun["Balun"]
        rfrx["RF receiver"]
        rftx["RF transmit"]
    end
```

Wireless communications on the ESP32 chip are interfaced via an RF (Radio Frequency) [peripheral designed by Riviera-Waves](https://www.ceva-ip.com/press/espressif-licenses-and-deploys-ceva-bluetooth-in-esp32-iot-chip/) (now [Ceva-Waves](https://www.ceva-ip.com/)).

On top of that, software stacks for Wi-Fi, Bluetooth and others can be run.