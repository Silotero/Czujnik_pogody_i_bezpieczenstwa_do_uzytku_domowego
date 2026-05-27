# Czujnik_pogody_i_bezpieczenstwa_do_uzytku_domowego
This is a device packed with MQ-7 (CO gas sensor), MQ-2 (smoke sensor), IR fire detector, as well as AHT20 (temperature and humidity sensor), along with the BMP280 (pressure sensor).

It is battery powered with USB-C non PD charging, usiong the MCP73831 battery charge IC, capable of charging the battery with 500 mA, with an AP9101 battery protection IC. The microcontroller used in this project is a barebone ESP32-C3, with external 4 MB of FLASH memory, using QSPI. The power coming from the battery gets passed to the PAM2423 boost converter circuit that boosts the battery voltage up to 5V. The 2 devices that use 5V (MQ-7 and MQ-2) are powered directly out of that output, while the rest such as the ESP32-C3, its FLASH memory, along with the AHT20 and BMP280 gets their 3.3V voltage out of a AP2114HA LDO

The ESP32-C3 RF pin is connected to an external antenna connector (IPEX4), used for transmitting data wirelessly.

The project is meant for use with a MQTT setup for data collection on a server type device.
