# XiaoZhi ESP32-WROOM ST7789 – Relay - DHT22

Firmware XiaoZhi untuk ESP32-WROOM dengan:

- ST7789 TFT 240x240
- INMP441 microphone
- MAX98357A amplifier
- DHT22 temperature & humidity
- 2-channel relay
- Bahasa Indonesia
- Jam analog saat standby

## Firmware

Firmware siap flash tersedia di **Releases**.

Download:

**esp32_analogjam.bin**

Tidak perlu build source code.

## Wiring

### ST7789 240x240

| ST7789 | ESP32-WROOM |
|---|---|
| GND | GND |
| VCC | 3.3V |
| SCK | GPIO18 |
| SDA | GPIO23 |
| RES | GPIO13 |
| DC | GPIO17 |
| BLK | GPIO4 |
| CS | Tidak digunakan |

### INMP441

| INMP441 | ESP32-WROOM |
|---|---|
| WS | GPIO25 |
| SCK | GPIO26 |
| SD | GPIO32 |
| VCC | 3.3V |
| GND | GND |

### MAX98357A

| MAX98357A | ESP32-WROOM |
|---|---|
| DIN | GPIO33 |
| BCLK | GPIO14 |
| LRC | GPIO27 |
| GND | GND |
| VIN | Supply amplifier |

### DHT22

| DHT22 | ESP32-WROOM |
|---|---|
| DATA | GPIO19 |
| VCC | 3.3V |
| GND | GND |

Jika modul DHT22 tidak memiliki resistor pull-up, gunakan resistor 4.7K–10K antara DATA dan 3.3V.

### Relay

| Relay | ESP32-WROOM |
|---|---|
| Relay 1 IN | GPIO21 |
| Relay 2 IN | GPIO22 |
| GND | GND |

Logika relay:

**HIGH = ON**  
**LOW = OFF**

Gunakan modul relay/driver yang kompatibel dengan logika 3.3V.

## Cara Kerja

Saat perangkat dinyalakan:

1. Startup screen tampil.
2. XiaoZhi terhubung ke Wi-Fi.
3. Saat standby, layar menampilkan jam analog.
4. Perintah suara dapat digunakan untuk mengontrol Relay 1 dan Relay 2.
5. DHT22 menyediakan data suhu dan kelembapan.

## Status

Firmware sudah tested dan working pada ESP32-WROOM 4MB.

**Created by Arsiparis – XiaoZhi Cimahi**
