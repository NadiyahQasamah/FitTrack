# FitTrack — Sistem Prediksi Nutrisi dan Aktivitas Fisik Berbasis AI

## Tentang Proyek

FitTrack merupakan sistem berbasis Data Science, Artificial Intelligence (AI), Machine Learning, dan Data Analytics yang dirancang untuk memperkirakan kandungan nutrisi makanan serta mengintegrasikan data aktivitas fisik dari perangkat seperti smartwatch.

Sistem ini menggabungkan data nutrisi makanan dan aktivitas fisik untuk menghasilkan nilai kalori termodifikasi. Data historis yang tersimpan dalam database kemudian diolah menggunakan model *time series forecasting* untuk memprediksi metrik nutrisi pada beberapa periode mendatang.

## Tujuan Proyek

- Memperkirakan kandungan nutrisi makanan menggunakan komponen AI.
- Mengintegrasikan data aktivitas fisik dari perangkat wearable, seperti smartwatch.
- Menyimpan data input dan aktivitas fisik ke dalam database Supabase.
- Mengambil dan mengolah data menggunakan SQL serta mengekspornya ke format CSV.
- Menerapkan model ARIMA untuk memprediksi data deret waktu.
- Mengintegrasikan hasil prediksi model ke dalam sistem FitTrack.

## Alur Kerja Sistem

1. **Estimasi Nutrisi Makanan**  
   Sistem memproses input makanan untuk memperkirakan kandungan nutrisi menggunakan komponen AI.

2. **Integrasi Aktivitas Fisik**  
   Sistem mengintegrasikan data aktivitas fisik yang diperoleh dari perangkat seperti smartwatch.

3. **Penyimpanan Data**  
   Data input makanan dan aktivitas fisik disimpan ke dalam database Supabase.

4. **Ekstraksi dan Pengolahan Data**  
   Data ditarik menggunakan query SQL dan diekspor ke dalam format CSV untuk kebutuhan analisis lebih lanjut.

5. **Perhitungan Kalori Termodifikasi**  
   Data kalori dan aktivitas fisik digunakan untuk menghitung nilai kalori termodifikasi dengan faktor pembobotan alpha sebesar 0,03 sesuai asumsi yang digunakan dalam proyek.

6. **Pemodelan Machine Learning**  
   Data historis diolah menggunakan model ARIMA (*AutoRegressive Integrated Moving Average*) untuk melakukan peramalan berdasarkan pola data deret waktu.

7. **Integrasi Hasil Prediksi**  
   Hasil pemodelan disiapkan untuk diintegrasikan ke dalam sistem agar dapat digunakan dalam memprediksi metrik nutrisi pada periode mendatang.

## Implementasi Data Science dan Machine Learning

### 1. Pengolahan Data

Data yang tersimpan di Supabase diekstraksi menggunakan query SQL, kemudian diekspor ke format CSV sebagai dataset untuk proses pengolahan dan pemodelan.

Tahapan pengolahan data meliputi:
- Ekstraksi data dari database.
- Persiapan dataset dalam format CSV.
- Pengolahan data historis.
- Rekayasa fitur (*feature engineering*) untuk perhitungan kalori termodifikasi.
- Persiapan data untuk pemodelan deret waktu.

### 2. Perhitungan Kalori Termodifikasi

FitTrack menggunakan faktor pembobotan alpha sebesar 0,03 untuk mengintegrasikan data aktivitas fisik ke dalam perhitungan kalori termodifikasi.

Representasi konseptual formula:

`Kalori Termodifikasi = Asupan Kalori − (Aktivitas Fisik × α)`

Keterangan:
- **Asupan Kalori:** Estimasi kalori yang diperoleh dari makanan.
- **Aktivitas Fisik:** Nilai aktivitas fisik yang digunakan dalam perhitungan sistem.
- **α (alpha):** Faktor pembobotan sebesar 0,03 berdasarkan asumsi metodologi proyek.

Nilai alpha digunakan sebagai parameter dalam perhitungan proyek dan perlu divalidasi berdasarkan satuan aktivitas fisik serta referensi yang digunakan. Hubungan antara jumlah langkah dan kalori terbakar dapat bervariasi berdasarkan karakteristik individu dan aktivitas.

### 3. Pemodelan ARIMA

FitTrack menerapkan ARIMA (*AutoRegressive Integrated Moving Average*) untuk menganalisis pola data historis dan memprediksi nilai pada periode mendatang.

Tahapan pemodelan meliputi:
- Persiapan data deret waktu.
- Analisis pola data historis.
- Penerapan model ARIMA.
- Peramalan nilai untuk beberapa periode mendatang.
- Persiapan hasil prediksi untuk integrasi ke dalam sistem.

Model ARIMA digunakan untuk meramalkan metrik berdasarkan pola historis. Model ini tidak secara langsung menentukan kandungan nutrisi makanan baru tanpa pendekatan estimasi tambahan.

## Teknologi yang Digunakan

- **Bahasa Pemrograman:** Python, SQL.
- **Database:** Supabase.
- **Pengolahan Data:** CSV dan query SQL.
- **Machine Learning:** ARIMA untuk peramalan deret waktu.
- **Artificial Intelligence:** Komponen estimasi nutrisi makanan.


# Estimasi Nutrisi
<img width="1920" height="1200" alt="Screenshot (4184)" src="https://github.com/user-attachments/assets/400d0f12-a5f3-4499-b232-894cab8a6e2e" />


# Aktivitas Fisik
<img width="1920" height="1200" alt="Screenshot (5822)" src="https://github.com/user-attachments/assets/9ce81e33-8798-4e6b-86c8-d28c29c11561" />


# Summary
<img width="1920" height="1200" alt="Screenshot (5842)" src="https://github.com/user-attachments/assets/5ac6ded9-5656-4ec6-a87f-4b0a128e51f0" />
<img width="1920" height="1200" alt="Screenshot (5843)" src="https://github.com/user-attachments/assets/db61ad25-2f7b-4e3f-b00e-4e0ba2ebd15c" />
<img width="1920" height="1200" alt="Screenshot (5844)" src="https://github.com/user-attachments/assets/74b3b2fe-5877-4af4-a03a-337c5bb747ba" />







