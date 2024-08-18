# Laptop Price Prediction using Regression Model

## Introduction
- Nama  : Vicky Belario

Milestone 2 ini dilakukan untuk mengimplementasikan konsep Machine Learning terutama Supervised Learning dengan model Regression pada dataset harga laptop

### **Objective**
- Memahami konsep Machine Learning.
- Dapat mempersiapkan data untuk digunakan dalam Supervised Learning model Regression.
- Bisa menerapkan Supervised Learning model Regression pada dataset harga lapptop.
- Sanggup melakukan Hyperparameter Tuning dan Cross Validation.
- Mampu melakukan Model Deployment.

### **Background**
Di era digital saat ini, laptop telah menjadi alat yang tak tergantikan bagi konsumen di seluruh dunia, digunakan untuk pekerjaan, pendidikan, dan hiburan.  Dengan teknologi yang berkembang pesat, beragam model dan fitur laptop tersedia dengan banyak pilihan. konsumen dihadapkan pada berbagai pilihan laptop yang sangat beragam.

proses pengambilan keputusan pembelian menjadi rumit ketika konsumen memilih laptop yang sesuai dengan kebutuhan mereka maupun sesuai dengan anggaran yang ada atau spesifikasi yang diinginkan, karena harga laptop dapat bervariasi berdasarkan spesifikasi, merek, dan tren pasar.

### **Goal**
Tujuan utama dari proyek ini adalah mengembangkan model regresi multilinear untuk memprediksi harga laptop berdasarkan fitur-fitur laptop seperti kecepatan prosesor dan kapasitas penyimpanan. Dengan mencapai tujuan ini, konsumen dapat mendapatkan perkiraan harga laptop yang informatif, sehingga membantu mereka membuat keputusan saat membeli laptop 

### **Dataset Overview**

Pengambilan data melalui website kaggle :  [Link](https://www.kaggle.com/datasets/pragatikumari928/cleaned-laptop-price-dataset?select=laptop_updated.csv)

Dataset tersusun dari kumpulan berbagai informasi harga laptop yang dapat digunakan untuk menganalisis dan memahami tren harga serta spesifikasi dari berbagai model laptop. 
Dataset ini memiliki kolom yang berdasarkan bentuk datanya bisa dikategorikan sebagai berikut : 

Numerik Diskrit<br>
Kolom numerik diskrit mewakili nilai integer dengan nilai yang terpisah dan berbeda.

- screen_size: Ukuran layar
- resolution_width: Resolusi lebar layar laptop.
- resolution_height: Resolusi tinggi layar laptop.
- Ram: Jumlah RAM di laptop.
- primary_storage: Kapasitas penyimpanan utama laptop.
- secondary_storage: Kapasitas penyimpanan sekunder laptop (jika ada).

Kategorikal Diskrit<br>
Kolom kategorikal diskrit mewakili kategori atau label.

- Company: Merek atau perusahaan yang memproduksi laptop.
- TypeName: Model atau tipe laptop.
- ips_panel: Menunjukkan apakah laptop memiliki panel IPS (biner: 0 atau 1).
- touchscreen: Menunjukkan apakah laptop memiliki fitur layar sentuh (biner: 0 atau 1).
- cpu_brand: Merek CPU laptop.
- cpu_name: Model CPU laptop.
- memory_type: Jenis memori yang digunakan di laptop.
- gpu_brand: Merek GPU laptop.
- OpSys: Sistem operasi yang terinstal di laptop.

Numerik Kontinu<br>
Kolom numerik kontinu mewakili pengukuran yang dapat mengambil nilai apa pun dalam suatu rentang.

- Inches: Ukuran layar laptop dalam inci.
- cpu_speed: Kecepatan clock CPU laptop.
- Weight: Berat laptop.
- price: Harga laptop.
- ppi: ukuran kerapatan piksel (Pixels Per Inch)

Deployment proyek model pada website huggingface : [Link](https://huggingface.co/spaces/vickybelario/milestone2)

## kesimpulan

- Rata-rata, merek laptop paling mahal adalah Razer dan yang paling populer adalah Dell dan Lenovo.

- Di antara jenis laptop, notebook adalah yang paling populer, sementara laptop gaming dan workstation adalah yang paling mahal.

- Ukuran layar laptop tidak memiliki pengaruh yang signifikan, karena rata-rata laptop dengan layar berukuran sedang (antara 14 dan 16 inci) memiliki harga terendah.

- Rata-rata, laptop paling mahal memiliki prosesor Intel Core generasi ke-7, sementara dibawahnya versi lama  prosesor Intel Core i3.

- Sebagian besar kartu grafis diproduksi oleh Nvidia dan biasanya memiliki harga tertinggi, sementara banyak laptop menggunakan grafis dari Intel.

- RAM secara definitif memengaruhi model - semakin besar jumlahnya dalam GB, semakin mahal harga laptop.

- Sistem operasi memiliki dampak relatif rendah pada harga laptop karena rata-rata laptop termahal memiliki Mac OS.

- dari hasil cross validation didapat dari 6 model yang dicoba, model terbaik adalah random forest regressor dengan nilai rmse 195 euro

- dari hasil RandomSearch didapat hyperparameter terbaik max_depth = 37, max_leaf_nodes = 47 , min_samples_leaf = 1 , min_samples_split = 5 , n_estimators = 155 <br>

- Kesalahan rata-rata (RMSE) pada model terbaik menggunakan hyperparameter adalah 168 euro 

- terdapat peningkatan rmse sebelum dan sesuah tuning dari 195 menjadi 169 menunjukan kesalahan rata-rata mengecil
