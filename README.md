# Pengaruh-Sentimen-Twitter-pada-Prediksi-Saham-Netflix-dengan-CNN-BiLSTM
Repositori ini berisi proyek prediksi harga saham Netflix menggunakan CNN-LSTM dengan analisis sentimen Twitter. Sentimen dihitung menggunakan VADER dan digunakan sebagai fitur tambahan. Model dievaluasi menggunakan MAPE dan MSE untuk mengukur akurasi. Proyek ini menggabungkan analisis sentimen dan deep learning untuk prediksi saham.

## Prediksi Saham Netflix dengan CNN-BiLSTM dan Analisis Sentimen Twitter

Proyek ini bertujuan untuk memprediksi harga saham Netflix dengan menggunakan model CNN-LSTM, yang ditingkatkan dengan analisis sentimen Twitter sebagai fitur tambahan.

## Fitur Utama
- **Model CNN-LSTM**: Menggunakan kombinasi Convolutional Neural Network (CNN) dan Long Short-Term Memory (LSTM) untuk memprediksi harga saham berdasarkan data historis.
- **Analisis Sentimen Twitter**: Sentimen dihitung menggunakan pustaka VADER dan dimanfaatkan sebagai salah satu fitur prediktor.
- **Evaluasi Model**: Menggunakan metrik Mean Absolute Percentage Error (MAPE) dan Mean Square Error (MSE) untuk mengevaluasi performa model.

## Dataset
- **Data Saham Netflix**: Data historis harga saham dari Januari 2018 hingga Juli 2022.
- **Data Twitter**: Tweet terkait Netflix yang diproses untuk mendapatkan skor sentimen menggunakan pustaka VADER.

## Preprocessing Data
1. Data saham diskalakan menggunakan **MinMaxScaler**.
2. Data Twitter diproses menggunakan teknik berikut:
   - Membersihkan teks dari URL, mentions, dan karakter non-alfabet.
   - Mengubah emoji menjadi teks.
   - Tokenisasi, penghapusan stopwords, dan stemming.
   - Menghitung skor sentimen (positif, netral, negatif, compound) menggunakan VADER.
3. Sentimen harian dirata-ratakan untuk ditambahkan ke dataset saham.

## Arsitektur Model
Model CNN-LSTM terdiri dari:
- **Layer Convolutional**: Untuk ekstraksi fitur dari data historis.
- **Layer LSTM Bidirectional**: Untuk menangkap hubungan temporal dalam data.
- **Dense Layer**: Untuk menghasilkan output prediksi harga saham.

## Evaluasi Model
- **MAPE Tanpa Sentimen Twitter**:
  - Open: 0.89%
  - Adj Close: 67.57%
- **MAPE Dengan Sentimen Twitter**:
  - Open: 2.19%
  - Adj Close: 2.73%

Penambahan analisis sentimen Twitter secara signifikan meningkatkan akurasi model, terutama untuk prediksi harga penutupan saham.

## Teknologi yang Digunakan
- **Python**: Bahasa pemrograman utama.
- **TensorFlow/Keras**: Untuk pengembangan model CNN-LSTM.
- **NLTK dan VADER**: Untuk analisis sentimen.
- **Pandas dan Matplotlib**: Untuk manipulasi data dan visualisasi.

## Instalasi dan Penggunaan
1. Clone repositori ini:
   ```bash
   git clone https://github.com/Ivanderperdanamokhtar/Pengaruh-Sentimen-Twitter-pada-Prediksi-Saham-Netflix-dengan-CNN-LSTM.git
   ```
2. Install pustaka yang diperlukan:
   ```bash
   pip install -r requirements.txt
   ```
3. Jalankan preprocessing data Twitter dan saham.
4. Latih model CNN-LSTM:
   ```python
   python train_model.py
   ```
5. Evaluasi model dan buat prediksi.

## Hasil Visualisasi
Model menghasilkan grafik yang membandingkan prediksi dengan data aktual, serta plot loss untuk pelatihan dan validasi.



