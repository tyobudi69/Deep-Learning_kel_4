# Deteksi Penyakit Tanaman Berdasarkan Citra Daun Menggunakan CNN

## Deskripsi Proyek
Proyek ini bertujuan untuk membangun sistem klasifikasi penyakit tanaman berdasarkan citra daun menggunakan metode Convolutional Neural Network (CNN). Sistem dikembangkan untuk membantu proses deteksi penyakit tanaman secara otomatis dengan memanfaatkan citra daun, sehingga dapat mengurangi ketergantungan pada identifikasi manual yang memerlukan keahlian khusus dan waktu yang lama.

Dataset yang digunakan adalah PlantVillage yang terdiri dari citra daun tanaman paprika, kentang, dan tomat dengan berbagai kondisi penyakit maupun kondisi sehat.

## Tujuan
- Menerapkan metode Convolutional Neural Network (CNN) untuk klasifikasi citra daun tanaman
- Mengklasifikasikan kondisi daun tanaman ke dalam kelas sehat dan sakit
- Mengevaluasi performa model CNN dalam mendeteksi penyakit tanaman secara otomatis

## Dataset
- **Nama Dataset**: PlantVillage
- **Sumber**: Kaggle
- **Jumlah Data**: ±20.600 citra daun
- **Jumlah Kelas**: 15 kelas (sehat dan berbagai penyakit tanaman)
- **Jenis Tanaman**: Paprika, Kentang, Tomat

## Metode yang Digunakan
- Convolutional Neural Network (CNN)
- Data Preprocessing (resize, normalisasi)
- Data Augmentation (rotasi, flip, zoom, shift)
- Optimizer: Adam
- Loss Function: Categorical Cross-Entropy

## Arsitektur Model
Model CNN terdiri dari:
- 3 Convolutional Layer dengan filter 32, 64, dan 128
- MaxPooling Layer setelah setiap convolution
- Flatten Layer
- Dense Layer dengan 256 neuron
- Dropout Layer untuk mengurangi overfitting
- Output Layer dengan Softmax (15 kelas)

## Struktur Folder
```
project/
│── dataset/
│   ├── train/
│   └── validation/
│── model/
│   └── cnn_model.h5
│── notebook/
│   └── training_model.ipynb
│── README.md
```

## Cara Instalasi
1. Pastikan Python telah terinstal (disarankan Python 3.8+)
2. Install library yang dibutuhkan:
```
pip install tensorflow keras numpy matplotlib pandas scikit-learn
```

## Cara Menjalankan Program
1. Buka file notebook `training_model.ipynb`
2. Pastikan path dataset sudah sesuai
3. Jalankan seluruh cell untuk melakukan training dan evaluasi model

## Hasil dan Evaluasi
- Akurasi Training: **86,52%**
- Akurasi Validasi: **84,79%**
- Akurasi Klasifikasi Sehat vs Sakit: **96,19%**

Hasil evaluasi menunjukkan bahwa model CNN mampu mengklasifikasikan citra daun tanaman dengan tingkat akurasi yang tinggi dan stabil.

## Contoh Output
Model mampu mengidentifikasi daun sehat dan daun yang terinfeksi penyakit berdasarkan pola visual seperti perubahan warna, tekstur, dan bercak pada daun.

## Keterbatasan
- Dataset memiliki ketidakseimbangan jumlah data antar kelas
- Beberapa penyakit memiliki karakteristik visual yang mirip
- Model belum diuji pada citra lapangan (real-world data)

## Pengembangan Selanjutnya
- Menerapkan transfer learning (VGG, ResNet, MobileNet)
- Menambah data dari kondisi lapangan
- Mengembangkan sistem berbasis web atau mobile

## Kredit
Proyek ini dikembangkan sebagai bagian dari tugas Evaluasi Akhir Semester (EAS) Mata Kuliah Deep Learning.

Dataset: PlantVillage Dataset (Kaggle)
