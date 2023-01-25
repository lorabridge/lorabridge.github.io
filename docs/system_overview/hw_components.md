# Hardware components

All components necessary to build LoRaBridge bridge and gateway units are listed below. *Please note: the components listed here are the ones used to build
the first proof-of-concept LoRaBridge implementation with verified functionality*. Some components such as different Raspberry PI models or other Zigbee coordinator sticks might work out-of-the-box. Other components like external LoRaWAN gateways or alternative LoRa modems require adjustments to the LoRaBridge software.

## Table of components

| Device  | Manufacturer (link) | Distributor (link)  |  
|---|---|---|
| Raspberry PI 4B  | [Raspberry PI Foundation](https://www.raspberrypi.com/products/raspberry-pi-4-model-b/) |   |
| Adafruit LoRa Funk Bonnet mit OLED - RFM95W @ 915MHz  | [Adafruit](https://www.adafruit.com/product/4074)  | [Sertronics](https://b2b.sertronics-shop.de/Raspberry-Pi/Raspberry-Pi-Computer/GPIO-HATs-/-pHATS/Funk-/-GPS/Adafruit-LoRa-Funk-Bonnet-mit-OLED-RFM95W--915MHz/)   |
| CC2652RB Zigbee USB development stick | [slae.sh](https://slae.sh/projects/cc2652/)| [Ewelink](https://ewelinkstore.com/product/cc2652rb-zigbee-usb-development-stick/?v=fa868488740a)|
| Dragino PG1301 LoRaWAN GPS Concentrator | [Dragino](https://www.dragino.com/products/lora/item/149-lora-gps-hat.html) |    |

## Hardware Setup

### Bridge

To set up a bridge you need:

- [Raspberry Pi 4](https://www.raspberrypi.com/products/raspberry-pi-4-model-b/)
- Power adapter
- Micro SD card  (16+ GB recommended)
- Adafruit LoRa Funk Bonnet mit OLED - RFM95W @ 915MHz
- CC2652RB Zigbee USB development stick

![Bridge](../assets/Bridge.png)

___

### Gateway

To set up a gateway you need:

- [Raspberry Pi 4](https://www.raspberrypi.com/products/raspberry-pi-4-model-b/)
- Power adapter
- Micro SD card  (16+ GB recommended)
- Dragino PG1301 LoRaWAN GPS Concentrator

![Gateway](../assets/Gateway.png)