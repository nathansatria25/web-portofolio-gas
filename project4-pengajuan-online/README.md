# Sistem Pengajuan Online
Aplikasi web sederhana berbasis Google Apps Script untuk pengajuan izin mahasiswa.
## Fitur
- Login mahasiswa menggunakan NIM (BigQuery)
- Submit pengajuan izin
- Riwayat pengajuan realtime
- Notifikasi sukses/gagal
- Tanpa database server (hemat biaya)
## Arsitektur
- **Login**: BigQuery
- **Insert & Riwayat**: Google Sheets
- **Frontend**: HTML + JS (Apps Script)
## Struktur Data
### BigQuery
Dataset: `app_pengajuan`
Table: `data_mahasiswa`
| Field | Type |
|-----|-----|
| nim | INTEGER |
| nama | STRING |
99 | prodi | STRING |
### Google Sheet
Sheet: `data_pengajuan`
| Kolom |
|------|
| id |
| nim |
| jenis |
| keterangan |
| status |
| created_at |
## Konfigurasi
Edit di `Code.gs`:
```js
const PROJECT_ID = 'project-id-anda';
const DATASET_ID = 'app_pengajuan';
const SPREADSHEET_ID = 'spreadsheet-id';
https://script.google.com/macros/s/AKfycbzV4AvlbhXO6h5zV46KS2TWBe4pAcc7N5Q1XirPKNY7w3q3-Dk5BTJhUqlfa1_69nPS/exec
