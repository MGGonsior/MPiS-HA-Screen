## Wieloparametrowy / wieloczujnikowy system akwizycji danych środowiskowych z integracją w środowisku Home Assistant z wykorzystaniem ESP32 ##

Wieloparametrowy węzeł akwizycji danych środowiskowych zbudowany w oparciu o ESP32. Projekt łączy lokalne pomiary klimatyczne z wielu sensorów z danymi telemetrycznymi pobieranymi na żywo z Home Assistant. Całość prezentowana jest na szerokim wyświetlaczu OLED.

## Główne funkcjonalności
* **Lokalny monitoring:** Równoległy odczyt temperatury, wilgotności, ciśnienia i wskaźników jakości powietrza (IAQ/CO2e) z czterech różnych czujników (próbkowanie co 60s).
* **Wiele widoków:** Automatyczna rotacja 3 (4) ekranów co 10 sekund:
  1. Zegar synchronizowany przez SNTP.
  2. Telemetria z HA.
  3. Zegar (powtórzenie).
  4. Zbiorcza tabela pomiarów lokalnych (BME680, BMP280, AHT20, AM2302).
* **Zdalna kontrola:** Możliwość płynnej zmiany jasności panelu OLED z poziomu Home Assistant.

## Hardware
* **Mikrokontroler:** ESP32
* **Ekran:** OLED 3.12" SSD1322 (256x64, SPI)
* **Czujniki I2C:** BME680, BMP280, AHT20
* **Czujniki GPIO:** AM2302 (DHT)
* **Konstrukcja wewnętrzna:** Montaż przestrzenny.
* **Obudowa:** Druk 3D z czarnego ABS.
## Software
System bazuje na frameworku **ESPHome** i korzysta z natywnego API do komunikacji z Home Assistant.
