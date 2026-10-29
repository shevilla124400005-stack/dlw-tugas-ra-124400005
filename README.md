# Studi Ablasi RNN, LSTM, GRU vs ANN untuk Prediksi Trafik Seluler Milan

Tugas Workshop Deep Learning — Teknik Telekomunikasi ITERA.

## Kelompok

| Peran | Nama | NIM |
|---|---|---|
| Ketua (kelompok beranggotakan satu orang) | Shevilla Octaria Fitri | 124400005 |

- **Kelas:** RA
- **Lokasi kelompok:** 5 — Bandara Linate, kotak 4489 (digit terakhir NIM terkecil)
- **Laporan:** [`laporan-latex/main.pdf`](laporan-latex/main.pdf)

## Cara Menjalankan

```bash
uv sync
uv run jupyter lab
```

Buka `tugas_ablasi.ipynb`, isi `LOKASI_KELOMPOK`, lalu jalankan semua sel. Semua run tercatat di `hasil/ablasi.csv`.

Perangkat yang kami pakai: laptop ASUS Vivobook (CPU [ISI: tipe prosesor, mis. Intel Core i5-xxxx]), total waktu training: [ISI: x] menit.

## Ringkasan Hasil

Pada konfigurasi acuan di Duomo, RNN paling akurat (test MAE 229,6 ± 5,1), disusul GRU (237,2 ± 9,3), LSTM (273,6 ± 25,4), dan ANN (309,9 ± 5,9); semuanya mengalahkan baseline naif terbaik (467,6). Gabungan nilai terbaik yang dipilih dengan val MAE menurunkan test MAE ANN menjadi 286,2, LSTM 244,2, dan GRU 231,2, tetapi tidak membantu RNN (247,7). Di Bandara Linate, RNN dan GRU acuan tetap terbaik (test MAE 7,5), dan konfigurasi terbaik dari Duomo hanya membantu ANN (8,8 menjadi 7,7).

## Struktur

```
tugas_ablasi.ipynb      notebook eksperimen (di-commit beserta output)
data/                   data trafik per jam (Duomo + 10 lokasi tugas)
hasil/                  CSV seluruh run, tabel, dan grafik
laporan-latex/          sumber laporan (LaTeX) + PDF
```

## Data

Telecom Italia Big Data Challenge (Barlacchi dkk., 2015, *Scientific Data*, lisensi ODbL), versi per jam dari Zhang dkk. (INFOCOM 2021). Disiapkan oleh pengajar di repo [mctosima/dl-workshop](https://github.com/mctosima/dl-workshop).

Telecom Italia Big Data Challenge (Barlacchi dkk., 2015, *Scientific Data*, lisensi ODbL), versi per jam dari Zhang dkk. (INFOCOM 2021). Disiapkan oleh pengajar di repo [mctosima/dl-workshop](https://github.com/mctosima/dl-workshop).
