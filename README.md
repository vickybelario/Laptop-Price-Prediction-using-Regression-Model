
![the-Fair-Price-When-You-Sell-Laptops](https://github.com/user-attachments/assets/5764204f-bbda-4bcf-ba8b-11793266a284)

# Laptop Price Prediction using Regression Model
---

# <a style="float:right; margin-right: 15px"><img src="https://png.pngtree.com/png-vector/20221010/ourmid/pngtree-paper-icon-png-image_6294297.png" alt="drawing" width="64" align="center"/></a> <a id="class1" style="">**Introduction**</a> 


Nama  : Vicky Belario

Project ini dilakukan untuk mengimplementasikan konsep Machine Learning terutama Supervised Learning dengan model Regression pada dataset harga laptop

Deployment proyek model pada website Huggingface : [Link](https://huggingface.co/spaces/vickybelario/Laptops-Price-Prediction-using-Regression-Model)
//
---

# <a style="float:right; margin-right: 15px"><img src="https://cdn-icons-png.flaticon.com/512/9805/9805668.png" alt="drawing" width="64" align="center"/></a> <a id="class1" style="">**Background**</a> 

Di era digital saat ini, laptop telah menjadi alat yang tak tergantikan bagi konsumen di seluruh dunia, digunakan untuk pekerjaan, pendidikan, dan hiburan.  Dengan teknologi yang berkembang pesat, beragam model dan fitur laptop tersedia dengan banyak pilihan. konsumen dihadapkan pada berbagai pilihan laptop yang sangat beragam.

proses pengambilan keputusan pembelian menjadi rumit ketika konsumen memilih laptop yang sesuai dengan kebutuhan mereka maupun sesuai dengan anggaran yang ada atau spesifikasi yang diinginkan, karena harga laptop dapat bervariasi berdasarkan spesifikasi, merek, dan tren pasar.

# <a style="float:right; margin-right: 15px"><img src="https://cdn-icons-png.flaticon.com/512/2724/2724931.png" alt="drawing" width="64" align="center"/></a> <a id="class1" style="">**Goal**</a> 

Tujuan utama dari proyek ini adalah mengembangkan model regresi multilinear untuk memprediksi harga laptop berdasarkan fitur-fitur laptop seperti kecepatan prosesor dan kapasitas penyimpanan. Dengan mencapai tujuan ini, konsumen dapat mendapatkan perkiraan harga laptop yang informatif, sehingga membantu mereka membuat keputusan saat membeli laptop 


# <a style="float:right; margin-right: 15px"><img src="https://cdn-icons-png.flaticon.com/512/2110/2110161.png" alt="data" width="64" align="center"/></a> <a id="class1" style="">**Dataset overview**</a> 

Pengambilan data melalui website Kaggle :  [Link](https://www.kaggle.com/datasets/pragatikumari928/cleaned-laptop-price-dataset?select=laptop_updated.csv)

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

---
Penjelasan kontent pada file modelling sebagai berikut : 

   1. Import Libraries
      > *Cell* pertama pada *notebook* **berisi dan hanya berisi** semua *library* yang digunakan dalam *project*.
   
   2. Data Loading
      > Bagian ini berisi proses penyiapan data sebelum dilakukan eksplorasi data lebih lanjut. Proses Data Loading dapat berupa memberi nama baru untuk setiap kolom, mengecek ukuran dataset, dll.
   
   3. Exploratory Data Analysis (EDA)
      > Bagian ini berisi explorasi data pada dataset diatas dengan menggunakan query, grouping, visualisasi sederhana, dan lain sebagainya.
   
   4. Feature Engineering
      > Bagian ini berisi proses penyiapan data untuk proses pelatihan model, seperti pembagian data menjadi train-test, transformasi data (normalisasi, encoding, dll.), dan proses-proses lain yang dibutuhkan.   
   
   5. Model Definition
      > Bagian ini berisi cell untuk mendefinisikan model. menjelaskan alasan menggunakan suatu algoritma/model, hyperparameter yang dipakai, jenis penggunaan metrics yang dipakai, dan hal lain yang terkait dengan model.

   6. Model Training
      > Cell pada bagian ini hanya berisi code untuk melatih model dan output yang dihasilkan. meLakukan beberapa kali proses training dengan hyperparameter yang berbeda untuk melihat hasil yang didapatkan. Analisis dan narasi hasil ini pada bagian Model Evaluation.
   
   7. Model Evaluation
      > Pada bagian ini, dilakukan evaluasi model yang menunjukkan bagaimana performa model berdasarkan metrics yang dipilih. Hal ini dibuktikan dengan visualisasi tren performa dan/atau tingkat kesalahan model. **dilakukan analisis terkait dengan hasil pada model dan menuliskan hasil analisisnya**.

   8. Model Saving
      > Pada bagian ini, dilakukan proses penyimpanan model dan file-file lain yang terkait dengan hasil proses pembuatan model. **Dengan melihat hasil Model Evaluation, memilih satu model terbaik untuk disimpan. Model terbaik ini akan digunakan kembali dalam melakukan Model Inference dan Model Deployment.**
   
   9. Model Inference
       > Model yang sudah dilatih akan dicoba pada data yang bukan termasuk ke dalam train-set ataupun test-set. Data ini dalam format yang asli, bukan data yang sudah di-scaled. Menggunakan model terbaik berdasarkan hasil Model Evaluation. Notebook Model Inference berbeda dengan notebook saat pembuatan model dilakukan.
---

## <a style="float:right; margin-right: 15px"><img src="https://cdn-icons-png.freepik.com/256/11063/11063232.png" alt="drawing" width="64" align="center"/></a> <a id="class10">**Conclusion**</a>

---

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
