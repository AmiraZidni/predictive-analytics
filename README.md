# Laporan Proyek Machine Learning - Zidni Iman Sholihati

## Domain Proyek
Domain proyek ini akan membahas bidang ekonomi dan bisnis dengan judul **"Prediksi Keputusan Pelanggan Dalam Pembelian Asuransi Perjalanan"**.

Latar belakang proyek ini adalah diperlukannya pemetaan pelanggan yang memiliki kemungkinan untuk membeli asuransi perjalanan. Asuransi perjalanan memungkinkan orang bepergian mendapatkan perlindungan selama melakukan perjalanan dari kejadian tidak terduga seperti sakit, keterlambatan pesawat, atau hal tidak terduga yang mungkin terjadi dengan rumah yang ditinggal [1](https://kc.umn.ac.id/13580/).

Hasil proyek ini adalah sebuah *machine learning* yang dapat digunakan sebagai pendukung pembuatan keputusan sebuah perusahaan asuransi perjalanan dalam menyasar pelanggannya mengingat kemungkinan bidang bisnis ini akan diprediksi kembali naik setelah hampir punah selama pandemi [2](https://www.tandfonline.com/doi/full/10.1080/02513625.2020.1794120). Seiring pemulihan penerbangan, jasa asuransi perjalanan ini dapat menjadi produk menarik tersendiri bagi orang bepergian mengingat risiko pandemi yang membutuhkan waktu untuk kembali normal. 

## Business Understanding

### Problem Statements
Dari latar belakang di atas, dapat ditarik rumusan masalah sebagai berikut:
1. Bagaimana melakukan pra-pemrosesan data asuransi perjalanan agar menghasilkan data latih bagi *machine learning* prediksi keputusan pelanggan dalam pembelian asuransi perjalanan?
2. Bagaimana membuat model *machine learning* yang mampu memprediksi keputusan pelanggan dalam pembelian asuransi perjalanan?

### Goals
Tujuan proyek yang ingin dicapai adalah:
1. Melakukan pra-pemrosesan data asuransi perjalanan agar menghasilkan data latih yang cukup bagi *machine learning* prediksi keputusan pelanggan dalam pembelian asuransi perjalanan.
2. Membuat model *machine learning* yang mampu memprediksi keputusan pelanggan dalam pembelian asuransi perjalanan dengan akurasi >= 80%.

### Solution statements
1. Pra-pemrosesan dilakukan dengan langkah-langkah berikut:
- **Pengolahan kolom fitur** dengan memilah serta memilih kolom yang memiliki korelasi tinggi dengan kolom target.
- **Pembagian dataset** dengan data latih 80% dan data uji 20%.
- **Standarisasi data** dengan mengubah skala data menjadi relatif sama atau mendekati distribusi normal. 
2. Pembuatan model pada proyek ini menggunakan dua model sebagai berikut:
- **KNN**. KNN adalah algoritma yang menggunakan kesamaan fitur untuk memprediksi nilai baru. Nilai baru ini didasarkan pada seberapa mirip dengan tetangganya sejumlah  k, oleh karena itu disebut K-Nearest Neighbor.
- **Gradient Boosting Algorithm**. Algoritma ini bekerja dengan meningkatkan (*boosting*) model yang dianggap memiliki performa rendah atau akurasi yang belum memuaskan.

## Data Understanding
Dataset proyek ini berasal dari platform Kaggle yang dipublikasi oleh TejasTheBard dengan judul [Travel Insurance Prediction Data](https://www.kaggle.com/tejashvi14/travel-insurance-prediction-data). Berdasarkan metadata, dataset ini bersumber basis data perusahaan perjalanan di India. Dari dataset TravelInsurancePrediction.csv yang diunduh, dataset memiliki 10 kolom dengan keterangan berikut:

| Fitur               | Deskripsi                                                                                             |
| --------------------| ----------------------------------------------------------------------------------------------------- |
| Index               | Indeks atau nomor baris.                                                                              |
| Age                 | Umur pelanggan.                                                                                       |
| Employment Type     | Sektor pelanggan bekerja (Pemerintah (Government Sector) atau Swasta (Private Sector/Self Employed'). |
| GraduateOrNot       | Status lulusan perguruan tinggi.                                                                      |
| AnnualIncome        | Pendapatan tahunan (Rupee).                                                                           |
| FamilyMembers       | Jumlah anggota keluarga.                                                                              |
| ChronicDiseases     | Status ada tidaknya penyakit kronis pelanggan (asma, diabetes, darah tinggi, dll).                    |
| FrequentFlyer       | Status jika sering bepergian berdasarkan riwayat 2 tahun terakhir.                                    |
| EverTravelledAbroad | Status bepergian ke luar negeri.                                                                      |
| TravelInsurance     | Status pelanggan membeli paket asuransi.                                                              |

## Data Preparation
Pada bagian ini Anda menjelaskan teknik yang digunakan pada tahapan Data Preparation. 
- Terapkan minimal satu teknik data preparation dan jelaskan proses yang dilakukan.
- Jelaskan alasan mengapa Anda perlu menerapkan teknik tersebut pada tahap Data Preparation. 

## Modeling
Seperti yang telah dituliskan dalam *solution statement*, model machine learning yang digunakan untuk menyelesaikan permasalahan dalam proyek ini adalah KNN dan Gradient Boosting.

**1. KNN.** Model KNN proyek ini akan menggunakan library sklearn. Model dilatih dengan data yang telah melewati pra-pemrosesan. Selanjutnya akan dikembangkan model KNN ini menggunakan GridSearchCV untuk mencari hyperparameter terbaik.
  
**2. Gradient Boosting.** Model Gradient Boosting ini juga menggunakan library sklearn GradientBoostingClassifier dan dilatih dengan data yang telah melewati pra-pemrosesan.
Tahapan ini membahas mengenai model machine learning yang digunakan untuk menyelesaikan permasalahan. Seperti model KNN, Gradient Boosting ini juga akan dikembangkan modelnya dengan GridSearchCV untuk mencari hyperparameter terbaik.

Hasil pelatihan dan pengujian model dapat dilihat sebagai berikut:

![Hasil Model](/hasil_model.png?raw=true "Hasil Model")

Dari hasil seluruh model yang dibuat, model Gradient Boosting yang dikembangkan memiliki nilai terbaik dan oleh karena itu model ini yang akan digunakan pada tahap selanjutnya.

## Evaluation
Sebagai evaluasi, proyek klasifikasi akan menggunakan metrik akurasi, presisi, recall, dan F1 score. Kita juga akan melihat hasil *confusion matrix* dari prediksi model.

- Penjelasan mengenai metrik yang digunakan dan bagaimana formulanya
- Kelebihan dan kekurangan metrik
- Bagaimana cara menerapkannya ke dalam kode.

Ingatlah, metrik evaluasi yang digunakan harus sesuai dengan konteks data, problem statement, dan solusi yang diinginkan.

**---Ini adalah bagian akhir laporan---**




