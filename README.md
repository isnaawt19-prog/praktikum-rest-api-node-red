# Praktikum REST API Node-RED untuk Sistem IoT

## Identitas
- Nama: Isnawati
- NIM: 2410010336
- Program Studi: Teknik Informatika

## Deskripsi
Proyek ini merupakan praktikum REST API menggunakan Node-RED untuk sistem Internet of Things (IoT). Sistem menerima data suhu dan kelembapan melalui MQTT, menyediakan REST API untuk mengambil data sensor dan mengirim perintah kontrol, serta menampilkan data pada dashboard berbasis web.

## Teknologi
- Node-RED
- MQTT / Mosquitto
- Python
- Paho-MQTT
- HTML, CSS, dan JavaScript

## Struktur Proyek
- `simulasi_esp32.py`: simulasi pengiriman data sensor.
- `flows.json`: flow Node-RED hasil export.
- `dashboard/dashboard.html`: dashboard monitoring IoT.

## Endpoint REST API
- `GET /api/suhu` — mengambil data sensor terakhir.
- `GET /api/history` — mengambil riwayat data sensor.
- `POST /api/kontrol` — mengirim perintah kontrol melalui MQTT.

## Cara Menjalankan
1. Jalankan MQTT Broker Mosquitto.
2. Jalankan Node-RED.
3. Import `flows.json` ke Node-RED jika diperlukan.
4. Jalankan simulator dengan `python simulasi_esp32.py`.
5. Buka dashboard melalui `http://localhost:1880/dashboard.html`.

## Catatan
Proyek ini menggunakan simulator Python sebagai pengganti perangkat ESP32 fisik. Pengujian kontrol lampu dilakukan melalui pengiriman pesan MQTT.
