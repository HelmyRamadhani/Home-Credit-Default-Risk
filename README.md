
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

Pada data set, pengajuan pinjaman terdapat 307511 nasabah yang
terdiri dari 91,93% berindikasi pengajuan pijaman diterima (akan membayar pinjaman
tepat waktu) dan 8,07% mengalami pengajuan pijaman ditolak (kesulitan dalam
membayar kembali pinjaman)

### Objective
- Mendapatkan insight mengenai profile naasabah yaang mengajukan pinjaman.
- Memprediksi nasabah yang akan membayar pinjaman tepat waktu atau kesulitan dalam
membayar kembali pinjaman
- Memberikan bisnis rekomendasi yang tepat untuk meningkatkan penerimaan pengajuan pinjaman

### Goals







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

- ·Dari 121 Features terdapat 16 Features bertipe
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

**Kegagalan Membayar berdasarkan Rentang Usia Klien**

<!-- Code gambar 3 -->
<p align="center">
<img src="https://github.com/HelmyRamadhani/Home-Credit-Default-Risk/blob/main/Picture/Kegagalan%20Membayar%20berdasarkan%20Rentang%20Usia%20Klien.JPG" width="600" height="500" />
<p align="center">
<em> Gambar.3 Distribusi Kegagalan Membayar berdasarkan Rentang Usia Klien) </em>
</p>
</p>
<!-- Code gambar 3 -->

- seiring bertambahnya usia klien, tingkat nasabah yang mengalami kesulitan
membayar pinjaman yang terus menurun




**Kegagalan Membayar berdasarkan Rentang Usia Klien**

<!-- Code gambar 3 -->
<p align="center">
<img src="https://github.com/HelmyRamadhani/Home-Credit-Default-Risk/blob/main/Picture/Kegagalan%20Membayar%20berdasarkan%20Rentang%20Usia%20Klien.JPG" width="600" height="500" />
<p align="center">
<em> Gambar.3 Distribusi Kegagalan Membayar berdasarkan Rentang Usia Klien) </em>
</p>
</p>
<!-- Code gambar 3 -->


































