
# 💳Home Credit Default Risk💳

## 📂  **Stage 0 : Problem Statement**

### Problem Statement

Banyak orang berjuang untuk mendapatkan pinjaman karena riwayat kredit yang tidak mencukupi atau tidak ada. Dan sayangnya, populasi ini sering dimanfaatkan oleh pemberi pinjaman yang tidak dapat dipercaya.

Home Credit merupakan perusahaan penyedia credit ingin memperluas inklusi keuangan bagi masyarakat yang belum tersentuh layanan perbankan dengan memberikan pengalaman meminjam yang positif dan aman.

Untuk mencapai hal tersebut, Home credit ingin dapat memastikan calon nasabah yang mampu melakukan pelunasan tidak ditolak ketika melakukan pengajuan pinjaman, dan pinjaman dapat diberikan dengan principal, maturity, dan repayment calendar yang akan memotivasi pelanggan dengan menggunakan berbagai data alternatif, seperti telekomunikasi dan informasi transaksional untuk memprediksi kemampuan pembayaran klien mereka.

 <!-- Code gambar 1 -->
<p align="center">
<img src="https://github.com/HelmyRamadhani/Home-Credit-Default-Risk/blob/main/Picture/Persentase%20pengajuan%20pinjaman%20diterima%20dan%20ditolak.png" width="600" height="350" />
<p align="center">
<em> Gambar.1 Persentase pengajuan pinjaman diterima dan ditolak </em>
</p>
</p>
<!-- Code gambar 1 -->

Pada data set test, pengajuan pinjaman terdapat 307511 nasabah yang
terdiri dari 91,93% berindikasi pengajuan pijaman diterima (akan membayar pinjaman
tepat waktu) dan 8,07% mengalami pengajuan pijaman ditolak (kesulitan dalam
membayar kembali pinjaman)

### Objective
- Mendapatkan insight mengenai profile naasabah yaang mengajukan pinjaman.
- Memprediksi nasabah yang akan membayar pinjaman tepat waktu atau kesulitan dalam
membayar kembali pinjaman
- Memberikan bisnis rekomendasi yang tepat untuk meningkatkan penerimaan pengajuan pinjaman

### Goals
- Membuat model machine learning yang dapat memprediksi nasabah yang berpeluang membayar pinjaman tepat waktu.
- Diharapkan model dapat menigkatkan Take Up Rate diatas 1%

### Business Matrics
Take Up Rate

<br>

## 📂  **Stage 1 : Exploratory Data Analysis**

### **Dataset**

 <!-- Code tabel 1 -->
<p align="center">
  <em> Tabel.1 Ringkasan Data Set </em>
</p>
<p align="center">
  <img src="https://github.com/HelmyRamadhani/Home-Credit-Default-Risk/blob/main/Picture/dataset.JPG" width="800" height="400" />
</p>
<!-- Code tabel 1 -->

- Dataset pelatihan terdiri dari 307.511 baris
dengan 122 Features. Dataset pengujian terdiri
dari 48.744 baris dengan 121 Features (memiliki
Features yang sama seperti Dataset pelatihan
tetapi dikurangi variabel 'TARGET')

- Dari 121 Features di Dataset latih, 40,99% fitur
memiliki lebih dari 50% nilai yang hilang

- Dari 121 Features terdapat 16 Features bertipe
Categorical

- Pada Dataset terdapat data yang menampilkan 20 variabel yang
terkait dengan apakah klien telah menyediakan
formulir tertentu ('FLAG_DOCUMENT')

- Terdapat masalah kelas yang tidak seimbang pada
Features "TARGET"

<!-- Code gambar 2 -->
<p align="center">
<img src="https://github.com/HelmyRamadhani/Home-Credit-Default-Risk/blob/main/Picture/Distribusi%20Variabel%20Target%20(Dataset%20Pelatihan).JPG" width="500" height="400" />
<p align="center">
<em> Gambar.2 Distribusi Variabel Target (Dataset Pelatihan) </em>
</p>
</p>
<!-- Code gambar 2 -->

### **Insight**

**Distribusi usia nasabah dalam tahun**

<!-- Code gambar 3 -->
<p align="center">
<img src="https://github.com/HelmyRamadhani/Home-Credit-Default-Risk/blob/9092f2cf7b4a036c89b0e6f9a1fcc4a75bebafd9/Picture/Distribusi%20usia%20klien%20(dalam%20tahun).JPG" width="600" height="400" />
<p align="center">
<em> Gambar.3 Distribusi usia nasabah dalam tahun </em>
</p>
</p>
<!-- Code gambar 3 -->

- Plot diatas dengan jelas menunjukkan bahwa seiring bertambahnya usia nasabah, tingkat nasabah yang kesulitan dalam
membayar kembali pinjaman terus menurun. 

**Jenis Kontrak Berdasarkan Nilai Target**

<!-- Code gambar 4 -->
<p align="center">
<img src="https://github.com/HelmyRamadhani/Home-Credit-Default-Risk/blob/9092f2cf7b4a036c89b0e6f9a1fcc4a75bebafd9/Picture/Jenis%20Kontrak%20berdasarkan%20Nilai%20Target.JPG" width="600" height="400" />
<p align="center">
<em> Gambar.4 Jenis Kontrak Berdasarkan Nilai Target </em>
</p>
</p>
<!-- Code gambar 4 -->

- Rasio pinjaman tidak dilunasi (Target =1) untuk pinjaman Tunai(cash Loans) adalah 8,35%, sedangkan rasio untuk pinjaman Revoling(Revoling Loans) adalah 5,48%.

**Distribusi Jumlah Kredit Berdasarkan Nilai Target**

<!-- Code gambar 5 -->
<p align="center">
<img src="https://github.com/HelmyRamadhani/Home-Credit-Default-Risk/blob/ce1121495c524e469c5e95bbae6e084fa7448962/Picture/Distibusi%20Jumlah%20Kredit%20Berdasarkan%20Nilai%20Target.JPG" width="700" height="350" />
<p align="center">
<em> Gambar.5 Distribusi Jumlah Kredit Berdasarkan Nilai Targe </em>
</p>
</p>
<!-- Code gambar 5 -->

- Distribusi jumlah kredit yang dibayar tepat waktu dan mengalami kesulitan membayar adalah serupa. Tetapi terdapat anomali pada jumlah kredit kisaran antara 400.000 hingga 600.000 memiliki rasio pinjaman yang tidak dilunasi lebih tinggi.


**Distribusi Days_Employed berdasarkan Nilai Target**

<!-- Code gambar 6 -->
<p align="center">
<img src="https://github.com/HelmyRamadhani/Home-Credit-Default-Risk/blob/a20c658639d41dcec2f962b2a966984abc91477e/Picture/Distribution%20DAYS_EMPLOYED%20Berdasarkan%20Nilai%20Target.JPG" width="650" height="350" />
<p align="center">
<em> Gambar.6 Distribusi Days_Employed berdasarkan Nilai Target </em>
</p>
</p>
<!-- Code gambar 6 -->

- Distibusi pinjaman mengalami kesulitan membayar memuncak pada
DAYS_EMPLOYED sekitar nol. Nilai yang sama dengan dan di bawah nol cenderung
mengindikasikan bahwa nasabah tersebut menganggur. Sehingga kemampuan
seseorang untuk memperbaiki pinjaman mereka tampaknya berkorelasi positif
dengan masa kerja di pekerjaan mereka saat ini


<br>

## 📂  **Stage 2 : Data Pre-processing**

### **Workflow Data Pre-processing**


<!-- Code gambar 7 -->
<p align="center">
<img src="https://github.com/HelmyRamadhani/Home-Credit-Default-Risk/blob/1f8f39e00be7349680901d547300fe00b2a9b1e9/Picture/Workflow%20Data%20Pre-processing.JPG" width="650" height="300" />
<p align="center">
<em> Gambar.7 Workflow Data Pre-processing </em>
</p>
</p>
<!-- Code gambar 7 -->


**1. Handling Missing Value**
- Menghapus kolom yang memiliki jumlah data null lebih dari 60% jumlah baris dataset "train"
- Memisahkan kolom yang bertipe kategorical dan numerik
- Pada kolom numerik yang memiliki jumlah data null kurang dari 60%. Akan di isi dengan median dari masih masih kolomnya.
- Pada kolom kategorical yang memiliki jumlah data null kurang dari 60%. Akan di isi dengan mode dari masih masih kolomnya.
- Hal ini juga dilakuakn pada dataset "test"

**2. Handling Outlier**
- Handling Outlier hanya dilakukan pada seluruh kolom numerik kecuali target
- Handling Outlier dilakukan dengan cara mengganti nilai outlier. Pada nilai-nilai yang upper outlier akan diganti dengan nilai '9999999' dan pada nilai-nilai yang lower outlier akan diganti dengan nilai '1111111'

**3. Label Encoder**
- Label Encoder hanya dilakukan pada kolom ketegorical
- Karena pada kolom "ORGANIZATION_TYPE" memiliki terlalu banyak nilai maka, kolom ini dihapus

**4. Splitting Data Train dan Test**
- Splitting dataset train dan test dilakukan dengan proporsi 70 : 30
- Data set "test" menjadi data validasi

**5. Feature Transformation**
- Feature Transformation yang dipilih yaitu Normalization karena tidak merubah bentuk sebaran dat dan merubah range dari nilai fitur dengan batas range
yang pasti/rigid
- Normalization dilakukan hanya pada dataset train

**6. Handling Class Imbalance**
- Dikarenakan jumlah kelas antar fitur target cukup besar maka Handling Class Imbalance dilakukan pada data train dengan menggunakan metode Oversampling.


## 📂  **Stage 3 : Modeling and Evaluation**

**Modeling and Evaluation**

- Algoritma yang digunakan yaitu Logistic Regression, dan Light GBM. Salain itu juga, dilakukan tuning pada setiap algortima yang digunakan
- Cross-Validation Score dipilih sebagai matriks evaluasi digunakan untuk mengukur seberapa baik kinerja model dalam memprediksi data yang belum pernah dilihat sebelumnya (data yang tidak digunakan pada saat training).

<!-- Code gambar 8 -->
<p align="center">
<img src="https://github.com/HelmyRamadhani/Home-Credit-Default-Risk/blob/fe349bfc1285e401180686a76ecd5d5d6875b73a/Picture/Hasil%20Cross-Validation%20Score%20%20dari%20Masing%20Masing%20Algoritma.jpg" width="600" height="300" />
<p align="center">
<em> Gambar.8 Hasil Cross-Validation Score dari Masing-Masing Algoritma </em>
</p>
</p>
<!-- Code gambar 8-->

Berdasarkan beberapa algoritma yang telah diterapkan untuk uji coba performa model, algoritma Light GBM yang telah dilakukan Hyperparameter Tuning dipilih untuk diterapkan karena miliki ross-Validation Score tertinggi dibandingkan dengana algoritma lainnya yaitu 0,742355.

**Feature Importances**

<!-- Code gambar 9 -->
<p align="center">
<img src="https://github.com/HelmyRamadhani/Home-Credit-Default-Risk/blob/94504d4fb40560d148cf8a88a63478f5133310f7/Picture/Grafik%20Summaryplot%20Beeswarm%20SHAP%20Value.JPG" width="300" height="400" />
<p align="center">
<em> Gambar.8 Hasil Cross-Validation Score dari Masing-Masing Algoritma </em>
</p>
</p>
<!-- Code gambar 8-->





























