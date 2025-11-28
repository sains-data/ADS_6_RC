**Analisis Faktor Fisik & Jam Belajar terhadap IPK Mahasiswa**
Proyek ini menganalisis apakah tinggi badan, berat badan, dan jumlah jam belajar memiliki hubungan atau pengaruh terhadap IPK menggunakan metode EDA, Korelasi Pearson, dan Regresi Linear Berganda.

**1. Cara Menjalankan Script**

1. Pastikan R dan RStudio telah terpasang pada perangkat.
2. Instal semua paket yang diperlukan (lihat bagian *Paket R yang Digunakan*).
3. Pastikan file dataset ".csv" tersimpan pada direktori yang sesuai, atau sesuaikan path pada bagian berikut:
```r
data <- read.csv("C:/Users/.../Dataset Tugas Besar ADS 2025 Karakteristik Mahasiswa.csv")
```
4. Buka file ADS_KEL6.Rmd di RStudio.
5. Klik tombol Knit untuk menjalankan seluruh analisis dan menghasilkan laporan.

**2. Paket R yang Digunakan**

Paket-paket berikut digunakan dalam analisis:
- dplyr — manipulasi data
- stringr — pembersihan teks
- readr — pembacaan data
- MASS — uji normalitas residual
- lmtest — uji heteroskedastisitas
- car — uji multikolinearitas
- ggplot2 — visualisasi
- ggcorrplot — pembuatan heatmap korelasi

Instal seluruh paket jika belum tersedia:
install.packages(c("dplyr","stringr","readr","MASS","lmtest","car","ggplot2","ggcorrplot"))

**3. Penjelasan Singkat Dataset**

Dataset yang digunakan berisi karakteristik mahasiswa, digunakan untuk menganalisis faktor-faktor yang mempengaruhi IPK. Beberapa variabel penting dalam dataset:
- ipk – Indeks Prestasi Kumulatif
- jam_belajar – Durasi belajar per hari
- tinggi – Tinggi badan mahasiswa
-  berat – Berat badan mahasiswa
-  ariabel tambahan: prodi, gender, internet, beasiswa, pekerjaan, jarak, pendapatan, uang_saku, organisasi, tempat_tinggal, dan lainnya.

Proses pembersihan data mencakup:
- Mengganti nama seluruh kolom agar seragam
- Membersihkan angka campuran (misal "3 jam" → 3)
- Mengubah koma menjadi titik
- Mengonversi kolom teks menjadi Title Case
- Mengubah nilai kosong/"-" menjadi NA
- Menstandarisasi kolom numerik
- Dataset kemudian digunakan untuk korelasi, uji asumsi, serta regresi linear berganda.

4. Struktur Repositori
├── ADS_KEL6.Rmd # File utama berisi seluruh kode analisis
├── Dataset Mahasiswa.csv # Dataset yang digunakan
├── README.Rmd / README.md # Dokumentasi project
└── output/ # (opsional) folder penyimpanan hasil plot/knit

file sudah mencakup:
- Import data
- Cek struktur data
- Pembersihan data
- Uji normalitas residual
- Uji heteroskedastisitas
- Uji multikolinearitas
- Korelasi variabel
- Regresi linear berganda
- Plot Prediksi vs Aktual
- Visualisasi koefisien regresi

