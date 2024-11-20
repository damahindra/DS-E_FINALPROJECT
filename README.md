# Laporan Proyek Machine Learning - Student Performance Factors and Prediction Modelling
## Nama Anggota :
1. MUHAMMAD TEGAR ABHIRAM - 215150700111009
2. ADAM FADILAH ISLAMAWAN - 215150700111017
3. MUHAMMAD DAYFIT AL RASHAD - 215150701111013
4. RANGGA ANDHITO DAMAHINDRA - 215150707111001

## Domain Proyek (Latar Belakang)

Kinerja akademik merupakan indikator penting dalam mengevaluasi keberhasilan sistem pendidikan, dengan nilai ujian sebagai salah satu ukuran utamanya. Nilai ujian tidak hanya mencerminkan tingkat pemahaman siswa terhadap materi, tetapi juga menunjukkan efektivitas metode pembelajaran serta pengaruh berbagai faktor eksternal yang mendukung atau menghambat proses belajar.

Penelitian sebelumnya menunjukkan bahwa faktor-faktor seperti kebiasaan belajar, kehadiran di kelas, dukungan orang tua, akses terhadap sumber daya pendidikan, hingga kondisi fisik dan psikologis siswa memiliki peran penting dalam menentukan hasil akademik. Hasil studi yang dilakukan oleh Marlina et al. (2021) mengidentifikasi bahwa faktor-faktor yang mempengaruhi tingkah laku siswa seperti lingkungan, motivasi, pengaruh teman sebaya, serta kualitas pengajar memiliki pengaruh yang signifikan terhadap hasil belajar siswa. Selain itu, dari perspektif kesehatan, Dewald et al. (2010) menegaskan bahwa kebiasaan tidur yang sehat dan motivasi intrinsik merupakan prediktor kuat untuk pencapaian nilai ujian yang tinggi.

Meski demikian, hubungan antara berbagai faktor tersebut sering kali bersifat kompleks dan saling memengaruhi, sehingga menimbulkan tantangan dalam upaya memahami dan mengelolanya. Untuk mengatasi masalah ini, diperlukan pendekatan penelitian yang holistik, menggunakan analisis data yang mendalam untuk mengidentifikasi pola dan hubungan kausal antara faktor-faktor tersebut. Selain itu, implementasi intervensi berbasis data, seperti program pengembangan kebiasaan belajar, pelatihan motivasi, serta peningkatan kualitas pengajaran, dapat menjadi solusi untuk meningkatkan hasil akademik secara menyeluruh. Penelitian ini diharapkan dapat memberikan wawasan yang lebih komprehensif guna mendukung pendidik, orang tua, dan pembuat kebijakan dalam merancang strategi pendidikan yang lebih efektif.

Referensi:

[Dewald, J. F., Meijer, A. M., Oort, F. J., Kerkhof, G. A., & Bögels, S. M. (2010). The influence of sleep quality, sleep duration and sleepiness on school performance in children and adolescents: A meta-analytic review. Sleep Medicine Reviews, 14(3), 179–189.](https://d1wqtxts1xzle7.cloudfront.net/42509143/Dewald_JF_Meijer_AM_Oort_FJ_et_al._The_i20160209-26034-13mkbov-libre.pdf?1455057577=&response-content-disposition=inline%3B+filename%3DThe_influence_of_sleep_quality_sleep_dur.pdf&Expires=1732092513&Signature=QTs7m3wynWWbGAaSaicfhVHI3VZq8Vitvg07EyDU1cmc71BnPk37e9VJm7c7pZl79FYoJxZFNdUKOlzm2wvHOX32VHeraXUzMHS1YkcFRRdA35kbFXSxpUo1RszSWq~8ekxGfTQIsH4lXwRQSaUQm0KwoDhH6FQoq31jzdhvr9QWW7fjgC9XhL04vlmxB7se6N1v~TTNpSVQQtTI4m3zW4QzRAnOEKC9DEBK68cIyfubU21yHxjHoxgQmC-I8uFDui3P~w9gApYi7ZoL1IyxmnyIHYRdLDH2ReTKZNW-8~RezqJ9idfk~3QHYQq4oCFRTwKm0PtdYULoRlVqEKyaJA__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA)

Studi ini menunjukkan korelasi positif antara kebiasaan tidur yang cukup dengan performa akademik yang lebih baik.

[Marlina, E., Tjahjadi, B., & Ningsih, S. (2021). Factors Affecting Student Performance in E-Learning: A Case Study of Higher Educational Institutions in Indonesia. The Journal of Asian Finance, Economics and Business, 8(4), 993–1001.](https://koreascience.kr/article/JAKO202109554061599.page)

Studi ini bertujuan untuk memahami faktor-faktor yang memengaruhi kinerja mahasiswa dalam pembelajaran e-learning

## Business Understanding

### Problem Statements

Proyek ini bertujuan untuk mengatasi beberapa masalah yang diidentifikasi terkait prediksi nilai ujian siswa berdasarkan berbagai faktor yang mempengaruhi kinerja akademik mereka. Pernyataan masalah diuraikan sebagai berikut:

1. Bagaimana memahami hubungan antara faktor-faktor seperti jam belajar, tingkat kehadiran, motivasi, dan faktor-faktor relevan lainnya terhadap nilai ujian siswa?

**Alasan**: *Variasi faktor ini sering tidak diperhatikan dalam pendekatan konvensional, sehingga strategi pendidikan menjadi kurang optimal.*

2. Bagaimana membangun model prediksi nilai ujian yang dapat membantu pihak sekolah dan orang tua untuk mengidentifikasi potensi kelemahan akademik siswa lebih awal?

**Alasan**: *Intervensi yang lebih awal dan terarah dapat meningkatkan hasil akademik siswa secara signifikan.*

3. Faktor mana yang memiliki dampak terbesar terhadap nilai ujian, sehingga dapat menjadi fokus dalam pengambilan keputusan pendidikan?

**Alasan**: *Memahami prioritas ini penting untuk efisiensi alokasi sumber daya seperti bimbingan belajar atau tambahan jam pelajaran.*


### Goals

Berdasarkan problem statements, berikut tujuan yang ingin dicapai pada proyek ini:

1. Mengetahui hubungan antara faktor-faktor seperti jam belajar, tingkat kehadiran, dukungan orang tua, dan motivasi terhadap nilai ujian siswa.
2. Mengidentifikasi faktor utama yang memiliki dampak terbesar terhadap nilai ujian siswa.
3. Menemukan model terbaik dengan akurasi tertinggi untuk memprediksi nilai ujian siswa berdasarkan faktor-faktor yang telah ditentukan.

### Solution statements

**1. Melakukan proses Exploratory Data Analysis (EDA) untuk:**

    a. Mengetahui hubungan antara jam belajar, kehadiran, motivasi, dan faktor lainnya dengan nilai ujian siswa.
   
    b. Mengidentifikasi pola atau tren dalam data yang relevan dengan nilai ujian siswa.
   
    c. Menentukan faktor utama yang memiliki dampak terbesar terhadap kinerja akademik siswa.
   
**2. Menggunakan 4 model machine learning untuk memprediksi nilai ujian siswa:**

    a. Linear Regression: Untuk memahami hubungan linier antar variabel.
   
    b. Random Forest Regressor: Untuk menangani hubungan non-linear dan analisis feature importance.
   
    c. XGBoost: Untuk meningkatkan performa prediksi dengan teknik boosting.
   
    d. Support Vector Regression (SVR): Untuk memodelkan hubungan kompleks dengan margin optimal.
   
**3. Menggunakan metrik evaluasi seperti:**

    a. Mean Absolute Error (MAE) dan Root Mean Squared Error (RMSE) untuk mengukur seberapa jauh prediksi model dari nilai aktual.
   
    b. R²-score untuk mengukur kemampuan model dalam menjelaskan variabilitas nilai ujian siswa.
   
    c. Memilih model terbaik berdasarkan nilai metrik evaluasi dengan performa tertinggi untuk memprediksi nilai ujian secara akurat dan efisien.


## Data Understanding
Paragraf awal bagian ini menjelaskan informasi mengenai data yang Anda gunakan dalam proyek. Sertakan juga sumber atau tautan untuk mengunduh dataset. Contoh: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Restaurant+%26+consumer+data).

Selanjutnya uraikanlah seluruh variabel atau fitur pada data. Sebagai contoh:  

### Variabel-variabel pada Restaurant UCI dataset adalah sebagai berikut:
- accepts : merupakan jenis pembayaran yang diterima pada restoran tertentu.
- cuisine : merupakan jenis masakan yang disajikan pada restoran.
- dst

**Rubrik/Kriteria Tambahan (Opsional)**:
- Melakukan beberapa tahapan yang diperlukan untuk memahami data, contohnya teknik visualisasi data atau exploratory data analysis.

## Data Preparation
Pada bagian ini Anda menerapkan dan menyebutkan teknik data preparation yang dilakukan. Teknik yang digunakan pada notebook dan laporan harus berurutan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan proses data preparation yang dilakukan
- Menjelaskan alasan mengapa diperlukan tahapan data preparation tersebut.

## Modeling
Tahapan ini membahas mengenai model machine learning yang digunakan untuk menyelesaikan permasalahan. Anda perlu menjelaskan tahapan dan parameter yang digunakan pada proses pemodelan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan kelebihan dan kekurangan dari setiap algoritma yang digunakan.
- Jika menggunakan satu algoritma pada solution statement, lakukan proses improvement terhadap model dengan hyperparameter tuning. **Jelaskan proses improvement yang dilakukan**.
- Jika menggunakan dua atau lebih algoritma pada solution statement, maka pilih model terbaik sebagai solusi. **Jelaskan mengapa memilih model tersebut sebagai model terbaik**.

## Evaluation
Pada bagian ini anda perlu menyebutkan metrik evaluasi yang digunakan. Lalu anda perlu menjelaskan hasil proyek berdasarkan metrik evaluasi yang digunakan.

Sebagai contoh, Anda memiih kasus klasifikasi dan menggunakan metrik **akurasi, precision, recall, dan F1 score**. Jelaskan mengenai beberapa hal berikut:
- Penjelasan mengenai metrik yang digunakan
- Menjelaskan hasil proyek berdasarkan metrik evaluasi

Ingatlah, metrik evaluasi yang digunakan harus sesuai dengan konteks data, problem statement, dan solusi yang diinginkan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan formula metrik dan bagaimana metrik tersebut bekerja.

**---Ini adalah bagian akhir laporan---**

_Catatan:_
- _Anda dapat menambahkan gambar, kode, atau tabel ke dalam laporan jika diperlukan. Temukan caranya pada contoh dokumen markdown di situs editor [Dillinger](https://dillinger.io/), [Github Guides: Mastering markdown](https://guides.github.com/features/mastering-markdown/), atau sumber lain di internet. Semangat!_
- Jika terdapat penjelasan yang harus menyertakan code snippet, tuliskan dengan sewajarnya. Tidak perlu menuliskan keseluruhan kode project, cukup bagian yang ingin dijelaskan saja.

