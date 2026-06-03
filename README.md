# Aquaforte-PoolHeater
RS485 integration through ESPHome on Aquaforte Heatpump for swimming-pool heater


All the information found in the YAML file is found on the internet on different forums.

The aquaforte runs the PCB-board: MWH367, this is also related to the Fairland PCB

Several documents were found that explained the RS485 commands to use for MWH367 PCB-boards
Another PDF-document indicated that for 3x,4x only max 8 registers could be read at once.

This is indeed personnly also encountered, therefor the modbus is split in different controllers each with max register-range.

I used a:
- ESP32-S3-1CH of Waveshare
- Connected: ESP32 A/B to the Aquaforte Wifi-port of the PCB-board
- Connected: ESP32 gnd to the Aquaforte Wifi-port of the PCB-Board
- NOT CONNECTED: +12v on the PCB-Board (as my ESP32 takes power of a dedicated transfo 5v


