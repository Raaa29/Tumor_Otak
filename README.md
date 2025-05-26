# Tumor_Otak
# 🧠 Klasifikasi Gambar Tumor Otak dengan CNN

Halo! Selamat datang di proyek menarik ini yang memanfaatkan kekuatan Deep Learning untuk membantu dalam deteksi dini tumor otak melalui analisis gambar MRI.

## ✨ Gambaran Umum Proyek

Proyek ini membangun dan melatih sebuah model Convolutional Neural Network (CNN) untuk mengklasifikasikan gambar MRI otak menjadi dua kategori: "dengan tumor" dan "tidak ada tumor". Tujuannya adalah untuk menyediakan alat bantu yang dapat diandalkan dalam proses diagnosis awal.

## 🚀 Teknologi yang Digunakan

Proyek ini dibangun dengan menggunakan beberapa teknologi inti dalam ekosistem Python untuk Deep Learning dan pemrosesan gambar:

*   **Python**: Bahasa pemrograman utama.
*   **TensorFlow**: Framework Deep Learning yang kuat untuk membangun dan melatih model CNN.
*   **Keras**: API tingkat tinggi dalam TensorFlow yang mempermudah pembangunan arsitektur jaringan saraf.
*   **NumPy**: Untuk operasi numerik dan manipulasi array.
*   **Pillow (PIL)**: Untuk memproses dan memanipulasi gambar.
*   **Matplotlib**: Untuk visualisasi data dan hasil (plot akurasi dan loss).
*   **Scikit-learn**: Digunakan untuk membagi dataset (train-test split).
*   **KaggleHub**: Untuk mengunduh dataset langsung dari Kaggle.

## 🏗️ Arsitektur Model CNN

Model yang digunakan dalam proyek ini adalah sebuah CNN Sequential dengan arsitektur sebagai berikut:

1.  **Convolutional Layer (Conv2D)**:
    *   Jumlah Filter: 32
    *   Ukuran Kernel: 3x3
    *   Fungsi Aktivasi: ReLU (Rectified Linear Unit)
    *   Input Shape: (224, 224, 3) - Sesuai dengan ukuran gambar yang telah diubah ukurannya.
    *   Padding: 'valid'

2.  **Pooling Layer (MaxPooling2D)**:
    *   Ukuran Pool: 2x2

3.  **Flatten Layer**:
    *   Mengubah output dari lapisan konvolusi dan pooling menjadi vektor 1D.

4.  **Dense Layer**:
    *   Jumlah Neuron: 256
    *   Fungsi Aktivasi: ReLU

5.  **Dropout Layer**:
    *   Rate: 0.5 - Secara acak menonaktifkan 50% neuron selama pelatihan untuk mencegah overfitting.

6.  **Output Layer (Dense)**:
    *   Jumlah Neuron: 1
    *   Fungsi Aktivasi: Sigmoid - Menghasilkan probabilitas untuk klasifikasi biner.

## 💡 Cara Kerja Sistem

Alur kerja sistem deteksi tumor otak ini adalah sebagai berikut:

1.  **Pengumpulan Data**: Dataset gambar MRI otak diunduh dari Kaggle.
2.  **Pre-processing Data**:
    *   Gambar dimuat dan diubah ukurannya menjadi 224x224 piksel.
    *   Gambar dikonversi ke format RGB.
    *   Nilai piksel dinormalisasi antara 0 dan 1.
    *   Gambar diberi label (1 untuk tumor, 0 untuk tidak ada tumor).
3.  **Pembagian Data**: Dataset dibagi menjadi set pelatihan, validasi, dan pengujian.
4.  **Pembangunan Model**: Model CNN dengan arsitektur yang dijelaskan di atas dibangun.
5.  **Pelatihan Model**: Model dilatih menggunakan data pelatihan dengan optimizer Adam dan Binary Cross-Entropy sebagai fungsi loss.
6.  **Evaluasi Model**: Performa model dievaluasi menggunakan data pengujian (akurasi dan loss).
7.  **Penyimpanan Model**: Model yang telah dilatih disimpan.
8.  **Prediksi (Testing)**: Pengguna dapat mengunggah gambar MRI baru, yang kemudian diproses dan digunakan oleh model untuk membuat prediksi (tumor terdeteksi atau tidak).

## 📊 Hasil Evaluasi

Setelah proses pelatihan, model dievaluasi untuk melihat performanya. Plot akurasi dan loss pada set pelatihan dan validasi dapat dilihat di notebook untuk memvisualisasikan proses pembelajaran model.

*(Anda dapat menambahkan placeholder di sini jika Anda ingin menambahkan gambar plot akurasi dan loss di masa depan.)*

## ✅ Hasil Prediksi

Bagian "Test Model" di notebook memungkinkan pengguna untuk mengunggah gambar MRI mereka sendiri dan mendapatkan prediksi dari model yang telah dilatih.

*([Anda dapat menambahkan placeholder di sini jika Anda ingin menambahkan contoh gambar yang diuji dan hasil prediksinya.](https://freeimage.host/i/3bsgP6l))*

Contoh output prediksi akan berupa teks yang menunjukkan apakah model mendeteksi adanya tumor atau tidak.

## 🤝 Kontribusi

Jika Anda memiliki saran atau ingin berkontribusi pada proyek ini, silakan hubungi saya atau buat pull request.


 dibuat dengan ❤️ oleh [Nama Anda]
