# 🌤️ Kemarin adem, hari ini gerah!
## Yuk kita prediksi suhu di Indonesia menggunakan Machine Learning.

Selamat datang di tutorial memprediksi suhu rata-rata di Indonesia, menggunakan machine learning! Dalam proyek ini, kita akan melalui semua tahapan—dari eksplorasi dataset cuaca, pelatihan model, hingga evaluasi hasil menggunakan visualisasi yang informatif.

### 📁 Dataset
Kita akan bekerja dengan dataset cuaca yang berisi data cuaca per jam seperti suhu, lama penyinaran matahari, dan informasi lainnya.
Datasets tersedia di directory project ini (climate_data.csv).

### 📌 Tujuan
Memprediksi suhu rata-rata harian berdasarkan data cuaca historis dengan target RMSE (Root Mean Square Error) di bawah 3°C.

---

### 🔍 Langkah 1: Exploratory Data Analysis (EDA)
Pada tahap ini, kita melakukan analisis awal terhadap data:
- Mengonversi kolom date menjadi format datetime.
- Mengekstrak fitur day, month, dan year dari tanggal.
- Menampilkan heatmap untuk memeriksa nilai yang hilang.
- Mengelompokkan data berdasarkan tahun dan bulan untuk melihat tren suhu dari waktu ke waktu.
- Membuat visualisasi garis untuk suhu rata-rata bulanan.
- Menampilkan heatmap korelasi antar fitur untuk memahami hubungan antar variabel.

### 🧠 Langkah 2: Preprocessing & Feature Selection
Selanjutnya, kita memilih fitur penting dan membersihkan data:
- Menentukan fitur yang akan digunakan sebagai input (misalnya Tx, Tn, RH_avg, dll).
- Menghapus baris yang tidak memiliki nilai target (Tavg).
- Memisahkan data menjadi data latih dan data uji.
- Melakukan imputasi pada nilai kosong dengan rata-rata.
- Melakukan feature scaling data agar model bekerja optimal.

### 🤖 Langkah 3: Modeling
Pada tahap ini, kita melatih 3 jenis model:
1. Linear Regression
2. Decision Tree Regression dengan max_depth=10
3. Random Forest Regression dengan max_depth=10

Setelah model dilatih, kita mengevaluasi performa mereka menggunakan RMSE. Hasil evaluasi menunjukkan bahwa model Random Forest memiliki performa terbaik dengan nilai RMSE sekitar 0.71.

### 📊 Langkah 4: Visualisasi
Kita membandingkan hasil prediksi model Random Forest dengan data aktual:
- Data prediksi dan aktual digabung ke dalam satu DataFrame berdasarkan tanggal.
- Dirata-ratakan per hari untuk mengatasi data yang semula per jam.
- Diurutkan berdasarkan tanggal dan diambil 100 data terakhir.
- Dibuat visualisasi garis untuk membandingkan nilai aktual vs prediksi dalam 100 hari terakhir.

Visualisasi ini memberikan gambaran bahwa prediksi cukup mendekati data aktual, membuktikan model bekerja dengan baik.

---

### 🚀 Pengembangan Selanjutnya
- Gunakan fitur tambahan seperti lokasi atau ketinggian.
- Lakukan hyperparameter tuning untuk meningkatkan performa model.
- Coba pendekatan time-series seperti ARIMA atau LSTM.

---

### Silakan fork proyek ini, coba dengan model lain, dan kontribusikan ide kamu!
