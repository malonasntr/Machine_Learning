# # 🎯 Analisis Clustering dan Klasifikasi - BMLP Sarma Elvita

## 🧩 Deskripsi Proyek
Proyek ini merupakan bagian dari submission akhir pada program **Belajar Machine Learning untuk Pemula (BMLP)**.  
Analisis dilakukan dalam dua tahap utama yaitu **Clustering** dan **Klasifikasi** menggunakan dataset transaksi pelanggan.

### 🔹 Tahap 1: Clustering
Tahap ini bertujuan untuk mengelompokkan data pelanggan berdasarkan karakteristik tertentu menggunakan algoritma **K-Means Clustering**.

Langkah-langkah yang dilakukan:
1. **Memuat Dataset dan EDA**
   - Menampilkan data awal (`head()`), struktur (`info()`), dan statistik deskriptif (`describe()`).
2. **Pembersihan dan Pra-pemrosesan**
   - Mengecek data kosong dan duplikat (`isnull().sum()` dan `duplicated().sum()`).
   - Melakukan **feature scaling** (MinMaxScaler atau StandardScaler).
   - Melakukan **feature encoding** untuk kolom kategorikal.
   - Menghapus kolom ID seperti `TransactionID`, `AccountID`, `DeviceID`, `IPAddress`, dan `MerchantID`.
3. **Membangun Model Clustering**
   - Menentukan jumlah cluster terbaik menggunakan **Elbow Method** dengan `KElbowVisualizer`.
   - Melatih model menggunakan `KMeans` dari `sklearn.cluster`.
   - Menyimpan model hasil training dengan `joblib.dump()` sebagai `model_clustering.joblib`.
4. **Interpretasi Hasil**
   - Menganalisis karakteristik tiap cluster berdasarkan hasil agregasi (mean, min, max).
   - Menambahkan kolom `Target` untuk menandai hasil cluster.
   - Mengekspor dataset hasil clustering untuk tahap klasifikasi selanjutnya.

### 🔹 Tahap 2: Klasifikasi
Tahap ini bertujuan untuk membangun model prediksi menggunakan hasil cluster sebagai **label target**.

Langkah-langkah yang dilakukan:
1. **Persiapan Data**
   - Membagi data menggunakan `train_test_split()`.
2. **Membangun Model Klasifikasi**
   - Menggunakan algoritma **Decision Tree Classifier** dari `sklearn.tree`.
   - Melatih model dan mengevaluasi akurasi.
   - Menyimpan model dalam format `.h5` menggunakan `joblib.dump()` dengan nama `decision_tree_model.h5`.

---

## 📊 Dataset
Dataset digunakan dalam format CSV dari Google Sheets:
[Link Dataset CSV](https://docs.google.com/spreadsheets/d/e/2PACX-1vTbg5WVW6W3c8SPNUGc3A3AL-AG32TPEQGpdzARfNICMsLFI0LQj0jporhsLCeVhkN5AoRsTkn08AYl/pub?gid=2020477971&single=true&output=csv)

Dataset ini kemudian disimpan secara lokal pada folder `dataset/` sebagai `clustering_dataset.csv` agar dapat digunakan berulang kali tanpa koneksi internet.

---

## 🧠 Teknologi yang Digunakan
- Python 3.x  
- pandas  
- numpy  
- matplotlib  
- seaborn  
- scikit-learn  
- yellowbrick  
- joblib  

---

## 📂 Struktur Folder

