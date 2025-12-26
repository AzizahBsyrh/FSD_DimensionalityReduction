# FSD_DimensionalityReduction
Nama:
* Nur Azizah Basyirah Syamsuddin (24523238)
* Naila Reyhantyas Nurkhalisha (24523050)
  
# Dimensionality Reduction menggunakan PCA dan t-SNE

## 1. Deskripsi Kasus
Dataset yang digunakan memiliki 13 fitur numerik dan 1 target sehingga sulit dianalisis dan divisualisasikan secara langsung dalam ruang berdimensi tinggi. Oleh karena itu, dilakukan dimensionality reduction untuk memproyeksikan data ke dalam ruang dua dimensi agar pola, struktur, dan persebaran data dapat diamati secara visual.

Pada notebook ini, reduksi dimensi dilakukan menggunakan Principal Component Analysis (PCA) dan t-Distributed Stochastic Neighbor Embedding (t-SNE), kemudian hasilnya divisualisasikan dalam bentuk scatter plot 2D.

## 2. Dataset yang Digunakan
Dataset yang digunakan adalah dataset heart disease dari kaggle. Dataset ini terdiri dari 13 fitur numerik dan 1 target yang telah diproses pada tahap awal notebook, meliputi:
* Pemilihan fitur numerik dari dataset asli
* Standardisasi data menggunakan StandardScaler agar setiap fitur memiliki skala yang sebanding
* Data hasil scaling digunakan sebagai input untuk PCA dan t-SNE

Tahap ini dapat dilihat pada bagian awal notebook sebelum penerapan algoritma reduksi dimensi.

## 3. Ringkasan Metode
Metode yang digunakan pada notebook adalah sebagai berikut:
* Principal Component Analysis (PCA)

PCA diterapkan dengan mereduksi data menjadi dua komponen utama (PC1 dan PC2). Notebook juga menampilkan nilai explained variance ratio untuk menunjukkan seberapa besar informasi data yang berhasil dipertahankan oleh masing-masing komponen.
* t-Distributed Stochastic Neighbor Embedding (t-SNE)
  
t-SNE digunakan untuk memproyeksikan data ke dua dimensi dengan mempertahankan kedekatan lokal antar data. Parameter seperti n_components dan random_state ditentukan pada notebook untuk menjaga konsistensi hasil visualisasi.

Hasil dari kedua metode divisualisasikan dalam bentuk scatter plot dua dimensi.

## 4. Analisis Hasil
Berdasarkan output PCA pada notebook, dua komponen utama pertama mampu merepresentasikan sebagian besar variasi data, seperti yang ditunjukkan oleh nilai explained variance ratio. Scatter plot PCA (PC1 vs PC2) menunjukkan persebaran data yang relatif menyebar secara global, namun belum membentuk klaster yang terpisah secara tegas. Hal ini menunjukkan bahwa PCA efektif untuk merangkum variasi data secara linier, tetapi kurang optimal dalam menangkap struktur non-linier.

Visualisasi PCA yang diberi warna berdasarkan salah satu fitur asli memperlihatkan adanya gradasi warna yang mengikuti arah tertentu pada sumbu PC1 atau PC2. Hal ini menunjukkan bahwa fitur tersebut berkontribusi signifikan terhadap pembentukan komponen utama, sesuai dengan konsep PCA yang memaksimalkan varians.

Pada output t-SNE, scatter plot menunjukkan pola pengelompokan data yang lebih jelas dibandingkan PCA. Titik-titik data dengan karakteristik serupa cenderung berdekatan dan membentuk klaster lokal. Hal ini membuktikan keunggulan t-SNE dalam menangkap struktur non-linier dan hubungan lokal antar data, sebagaimana terlihat langsung pada visualisasi pada notebook.

Secara keseluruhan, hasil pada notebook menunjukkan bahwa PCA cocok digunakan untuk analisis awal dan pemahaman variansi data, sedangkan t-SNE memberikan visualisasi yang lebih informatif untuk melihat struktur dan potensi klaster dalam dataset.
