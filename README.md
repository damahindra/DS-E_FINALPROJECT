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

> **Alasan**: *Variasi faktor ini sering tidak diperhatikan dalam pendekatan konvensional, sehingga strategi pendidikan menjadi kurang optimal.*

2. Bagaimana membangun model prediksi nilai ujian yang dapat membantu pihak sekolah dan orang tua untuk mengidentifikasi potensi kelemahan akademik siswa lebih awal?

> **Alasan**: *Intervensi yang lebih awal dan terarah dapat meningkatkan hasil akademik siswa secara signifikan.*

3. Faktor mana yang memiliki dampak terbesar terhadap nilai ujian, sehingga dapat menjadi fokus dalam pengambilan keputusan pendidikan?

> **Alasan**: *Memahami prioritas ini penting untuk efisiensi alokasi sumber daya seperti bimbingan belajar atau tambahan jam pelajaran.*


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
   
    b. Random Forest: Untuk meningkatkan akurasi model dengan menggabungkan banyak pohon keputusan dan mengurangi overfitting melalui pemilihan acak fitur dan sampel data.
  
    c. Gradient Boosting: Untuk meningkatkan model prediksi secara bertahap dengan menggabungkan model pembelajaran lemah (weak learners) dan memperbaiki kesalahan model sebelumnya.
   
    d. Support Vector Regression (SVR): Untuk memodelkan hubungan kompleks dengan margin optimal.

    e. Decision Tree: Untuk membangun model prediksi yang mudah dipahami dengan membagi data berdasarkan keputusan logis pada setiap fitur, memungkinkan interpretasi yang jelas mengenai bagaimana prediksi dibuat.
   
**3. Menggunakan metrik evaluasi seperti:**

    a. Mean Squared Error (MSE) dan Mean Absolute Error (MAE) untuk mengukur seberapa jauh prediksi model dari nilai aktual. MSE memberikan penalti lebih besar terhadap kesalahan besar (karena menggunakan kuadrat dariselisih), sementara MAE mengukur rata-rata kesalahan absolut, yang lebih robust terhadap outlier.
   
    b. Memilih model terbaik berdasarkan nilai metrik evaluasi dengan performa tertinggi untuk memprediksi nilai ujian secara akurat dan efisien.


## Data Understanding

### Informasi Dataset

Sumber: [Student Performance Factors](https://www.kaggle.com/datasets/lainguyn123/student-performance-factors/data), Kaggle

Dataset yang digunakan memuat dimensi sebesar **6,607 baris** dan **20 kolom**. Untuk kolom yang terdapat pada dataset dijabarkan sebagai berikut:

| No. | Nama Fitur               | Penjelasan Fitur                                                                                       | Tipe Data |
|-----|--------------------------|--------------------------------------------------------------------------------------------------------|-----------|
| 1   | Hours_Studied            | Jumlah jam yang dihabiskan untuk belajar per minggu.                                                   | int64     |
| 2   | Attendance               | Persentase kehadiran siswa di kelas.                                                                   | int64     |
| 3   | Parental_Involvement     | Tingkat keterlibatan orang tua dalam pendidikan siswa (Low, Medium, High).                             | object    |
| 4   | Access_to_Resources      | Ketersediaan sumber daya pendidikan (Low, Medium, High).                                               | object    |
| 5   | Extracurricular_Activities | Partisipasi dalam kegiatan ekstrakurikuler (Yes, No).                                                 | object    |
| 6   | Sleep_Hours              | Rata-rata jumlah jam tidur per malam.                                                                  | int64     |
| 7   | Previous_Scores          | Nilai dari ujian sebelumnya.                                                                           | int64     |
| 8   | Motivation_Level         | Tingkat motivasi siswa (Low, Medium, High).                                                            | object    |
| 9   | Internet_Access          | Ketersediaan akses internet (Yes, No).                                                                 | object    |
| 10  | Tutoring_Sessions        | Jumlah sesi bimbingan belajar yang dihadiri per bulan.                                                 | int64     |
| 11  | Family_Income            | Tingkat pendapatan keluarga (Low, Medium, High).                                                       | object    |
| 12  | Teacher_Quality          | Kualitas guru (Low, Medium, High).                                                                     | object    |
| 13  | School_Type              | Jenis sekolah yang dihadiri (Public, Private).                                                         | object    |
| 14  | Peer_Influence           | Pengaruh teman sebaya terhadap kinerja akademik (Positive, Neutral, Negative).                         | object    |
| 15  | Physical_Activity        | Rata-rata jumlah jam aktivitas fisik per minggu.                                                       | int64     |
| 16  | Learning_Disabilities    | Keberadaan gangguan belajar (Yes, No).                                                                 | object    |
| 17  | Parental_Education_Level | Tingkat pendidikan tertinggi orang tua (High School, College, Postgraduate).                           | object    |
| 18  | Distance_from_Home       | Jarak dari rumah ke sekolah (Near, Moderate, Far).                                                     | object    |
| 19  | Gender                   | Jenis kelamin siswa (Male, Female).                                                                    | object    |
| 20  | Exam_Score               | Nilai akhir ujian siswa.                                                                               | int64     |

### Cek Nilai Null dan Nilai Duplikat

Skrip Python cek nilai null
```
pd.DataFrame({'Missing Value':df_cleaned.isnull().sum()})
```

| No. | Nama Fitur               | Missing Value |
|-----|--------------------------|---------------|
| 1   | Hours_Studied            | 0             |
| 2   | Attendance               | 0             |
| 3   | Parental_Involvement     | 0             |
| 4   | Access_to_Resources      | 0             |
| 5   | Extracurricular_Activities | 0           |
| 6   | Sleep_Hours              | 0             |
| 7   | Previous_Scores          | 0             |
| 8   | Motivation_Level         | 0             |
| 9   | Internet_Access          | 0             |
| 10  | Tutoring_Sessions        | 0             |
| 11  | Family_Income            | 0             |
| 12  | Teacher_Quality          | 78            |
| 13  | School_Type              | 0             |
| 14  | Peer_Influence           | 0             |
| 15  | Physical_Activity        | 0             |
| 16  | Learning_Disabilities    | 0             |
| 17  | Parental_Education_Level | 90            |
| 18  | Distance_from_Home       | 67            |
| 19  | Gender                   | 0             |
| 20  | Exam_Score               | 0             |

Skrip Python cek nilai duplikat
```
df_cleaned.duplicated().sum()
```

0

Dari hasil di atas, kolom **Teacher_Quality** terdapat 78 missing values, **Parental_Education_Level** terdapat 90 missing values dan **Distance_from_home** terdapat 67 missing values sehingga dibutuhkan proses _handling_ untuk menangani nilai-nilai _null_ tersebut. Tidak terdapat nilai duplikat dalam dataset yang digunakan.

### Null Value Handling

Berikut adalah fitur-fitur yang memiliki nilai _null_:
- **Teacher_Quality**: 78
- **Parental_Education_Level**: 90
- **Distance_from_home**: 67

Total nilai _null_ pada dataset adalah 78 + 90 + 67 = **235**

Dengan dimensi dataset 6,607 baris dan 20 kolom menjadikan total data pada dataset adalah 6,607 * 20 = **132,140**

Dengan demikian, persentase jumlah nilai _null_ pada dataset adalah 235/132,140 * 100 = **0.18%**, di mana persentase tersebut sangat kecil sehingga untuk _handling_ nilai _null_ pada dataset, baris yang memuat nilai-nilai _null_ tersebut cukup dihapuskan karena tidak akan mempengaruhi informasi yang dimuat oleh keseluruhan data. Untuk menghapus nilai _null_ menggunakan sintaks:

```
# Menghapus baris yang memiliki missing values
df_cleaned = data.dropna()
```

### Outlier Detection

![image](https://github.com/user-attachments/assets/33c547e1-3af9-4f4e-969b-66780eead2dd)

Berikut adalah interpretasi dari boxplot yang ditampilkan di atas:

- Pada kolom Hours_Studied, terlihat beberapa outlier di sisi kiri (sekitar 0-5 jam) dan di sisi kanan (sekitar 35-45 jam). Meski demikian, 0-5 jam per minggu Ini mungkin terjadi, terutama jika seorang siswa tidak terlalu fokus pada studi, memiliki komitmen lain. 35-45 jam per minggu juga mungkin, terutama untuk siswa yang sangat berdedikasi. Outlier ini tidak akan dihapus karena memberikan gambaran lengkap tentang bagaimana siswa berbeda dalam waktu belajar.

- Pada kolom Tutoring_Sessions, dapat dilihat bahwa nilai 4 hingga 8 sesi per bulan, dianggap sebagai outliers secara statistik. Namun nilai-nilai ini sangat memungkinkan karena ada siswa yang mungkin merasa perlu belajar lebih banyak sehingga outlier tidak akan dihapus.

- Pada kolom Exam_Score, dapat dilihat bahwa mayoritas exam_score di rentang 65-70. Terdapat beberapa outlier, yaitu exam_score 75 ke atas. Namun terdapat outlier yaitu Exam_Score yang bernilai 101 yang mana tidak mungkin pada konteks ujian. Outlier lainnya akan dipertahankan karena sangat memungkinkan jika siswa mendapatkan nilai 75 keatas dan tidak melebihi 100.

- Pada kolom-kolom lainnya, dapat dilihat bahwa persebaran data merata dan tidak terdapat outlier yang signifikan. Secara keseluruhan, data ini siap untuk diproses dan dianalisis lebih mendalam tanpa perlu melakukan penghapusan outlier.

Berikut adalah sintaks kode Python untuk menghapus baris yang memiliki Exam_Score lebih dari 100:
```
df_cleaned.drop(df_cleaned[df_cleaned["Exam_Score"] > 100].index, inplace=True)
```

### Exploratory Data Analysis (EDA)

**Univariate Analysis**

Berikut adalah analisis jumlah nilai dari masing-masing fitur kategorikal:

![image](https://github.com/user-attachments/assets/92f50b2e-ef9f-4bd0-ba25-3b5651ea1909)

Secara umum, plot-plot pada gambar diatas dapat diinterpretasikan sebagai berikut:

- **Parental_Involvement**: Sebagian besar siswa memiliki keterlibatan orang tua di level medium.
- **Access_to_Resources**: Sebagian besar siswa memiliki akses ke sumber daya pada level medium.
- **Extracurricular_Activities**: Sebagian besar siswa terlibat dalam aktivitas ekstrakurikuler.
- **Motivation_Level**: Sebagian besar siswa memiliki tingkat motivasi pada level medium.
- **Internet_Access**: Sebagian besar siswa memiliki akses internet.
- **Family_Income**: Sebaran data pendapatan keluarga siswa cukup merata antara level medium dan low.
- **Teacher_Quality**: Sebagian besar siswa memiliki kualitas guru di level medium.
- **School_Type**: Sebagian besar siswa berasal dari sekolah negeri (public).
- **Peer_Influence**: Sebaran data pengaruh teman sebaya cukup merata di level neutral dan positive.
- **Learning_Disabilites**: Sebagian besar siswa tidak memiliki disabilitas belajar.
- **Parental_Education_Level**: Sebagian besar siswa memiliki orang tua dengan tingkat pendidikan setara sekolah menengah atas.
- **Distance_from_Home**: Sebagian besar siswa memiliki jarak tempat tinggal yang dekat dari sekolah.
- **Gender**: Sebagian besar siswa adalah laki-laki.

Berikut adalah analisis distribusi nilai dari masing-masing fitur numerikal:

![image](https://github.com/user-attachments/assets/25bc4205-44df-4a88-9cf2-fc8d191b2110)

Berdasarkan hasil plot histogram yang disajikan, dapat diinterpretasikan sebagai berikut:

- **Hours_Studied**: Distribusi data membentuk kurva normal dengan puncak di sekitar 20-25 jam. Mayoritas mahasiswa belajar sekitar 20-30 jam. Terdapat beberapa mahasiswa dengan jam belajar yang lebih ekstrim, baik sangat sedikit maupun sangat banyak.
- **Attendance**: Distribusi data menunjukkan pola bimodal, dengan dua puncak di sekitar 70-80% dan 90-100%. Mayoritas mahasiswa memiliki kehadiran di atas 80%. Terdapat beberapa mahasiswa dengan kehadiran yang rendah.
- **Sleep_Hours**: Distribusi data menunjukkan pola normal dengan puncak di sekitar 6-8 jam tidur. Mayoritas mahasiswa tidur sekitar 6-8 jam per hari. Terdapat beberapa mahasiswa dengan jam tidur yang ekstrim, baik sedikit maupun banyak.
- **Previous_Scores**: Distribusi data cenderung simetris dengan puncak di sekitar 70-80. Mayoritas mahasiswa memiliki skor sebelumnya di rentang 70-80. Terdapat beberapa mahasiswa dengan skor yang sangat rendah maupun sangat tinggi.
- **Tutoring_Sessions**: Distribusi data menunjukkan pola bimodal dengan dua puncak di sekitar 1 dan 6 sesi. Mayoritas mahasiswa mengikuti 1-2 sesi tutorial atau 5-6 sesi tutorial. Terdapat beberapa mahasiswa dengan jumlah sesi tutorial yang sangat sedikit maupun sangat banyak.
- **Physical_Activity**: Distribusi data menunjukkan pola bimodal dengan dua puncak yang jelas. Mayoritas mahasiswa memiliki aktivitas fisik yang rendah atau sangat tinggi. Terdapat sedikit mahasiswa dengan aktivitas fisik yang moderat.
- **Exam_Score**: Distribusi data cenderung normal dengan puncak di sekitar 70-80. Mayoritas mahasiswa memperoleh skor ujian di rentang 70-80. Terdapat beberapa mahasiswa dengan skor ujian yang sangat rendah maupun sangat tinggi.

**Multivariate Analysis**

![image](https://github.com/user-attachments/assets/8db8b289-7e22-4aef-9799-eaabba62ea75)

| Feature                      | Category          | Average Exam Score |
|------------------------------|-------------------|---------------------|
| Parental Involvement         | High              | 68.112200          |
|                              | Low               | 66.351938          |
|                              | Medium            | 67.113196          |
| Access to Resources          | High              | 68.103158          |
|                              | Low               | 66.223705          |
|                              | Medium            | 67.145801          |
| Extracurricular Activities   | No                | 66.951770          |
|                              | Yes               | 67.446138          |
| Motivation Level             | High              | 67.743931          |
|                              | Low               | 66.746108          |
|                              | Medium            | 67.338894          |
| Internet Access              | No                | 66.483471          |
|                              | Yes               | 67.309520          |
| Family Income                | High              | 67.814483          |
|                              | Low               | 66.853215          |
|                              | Medium            | 67.371005          |
| Teacher Quality              | High              | 67.664391          |
|                              | Low               | 66.775889          |
|                              | Medium            | 67.118662          |
| School Type                  | Private           | 67.316358          |
|                              | Public            | 67.216332          |
| Peer Influence               | Negative          | 66.582707          |
|                              | Neutral           | 67.215631          |
|                              | Positive          | 67.623433          |
| Learning Disabilities        | No                | 67.358557          |
|                              | Yes               | 66.291916          |
| Parental Education Level     | College           | 67.358432          |
|                              | High School       | 66.884104          |
|                              | Postgraduate      | 67.972656          |
| Distance from Home           | Far               | 66.498428          |
|                              | Moderate          | 66.969072          |
|                              | Near              | 67.513812          |
| Gender                       | Female            | 67.262179          |
|                              | Male              | 67.235629          |

Hasil analisis di atas dapat diinterpretasikan sebagai berikut:

- Learning_Disabilities: Mahasiswa tanpa learning disabilities memiliki rata-rata skor ujian yang lebih tinggi (67.36) dibandingkan dengan yang memiliki learning disabilities (66.29).
- Parental_Involvement: Mahasiswa dengan keterlibatan orang tua yang tinggi memiliki rata-rata skor ujian yang lebih tinggi (68.11) dibandingkan dengan yang rendah (66.35) atau sedang (67.11).
- Access_to_Resources: Mahasiswa dengan akses sumber daya yang tinggi memiliki rata-rata skor ujian yang lebih tinggi (68.10) dibandingkan dengan yang rendah (66.22) atau sedang (67.15).
- Extracurricular_Activities: Mahasiswa yang terlibat dalam kegiatan ekstrakurikuler memiliki rata-rata skor ujian yang lebih tinggi (67.45) dibandingkan dengan yang tidak terlibat (66.95).
- Motivation_Level: Mahasiswa dengan motivasi tinggi memiliki rata-rata skor ujian yang lebih tinggi (67.74) dibandingkan dengan yang rendah (66.75) atau sedang (67.34). Variabel lainnya juga menunjukkan perbedaan rata-rata skor ujian, meskipun mungkin tidak terlalu signifikan.

## Data Preparation
### Encoding
Encoding adalah proses mengubah nilai kategorikal dalam dataset menjadi nilai numerikal. Hal ini dicapai dengan membuat nilai-nilai unik dalam sebuah fitur menjadi fitur-fitur baru yang didalamnya (sebagai contoh) bernilai 1 untuk mewakili 'ya' dan 0 untuk mewakili 'tidak'. Terdapat 3 macam teknik encoding yang digunakan, yaitu Categorical Encoding, One Hot Encoding, dan Ordinal Encoding.

Berikut adalah penjelasan singkat mengenai tiga teknik encoding yang digunakan:

1. **Categorical Encoding**  
   Categorical encoding adalah teknik untuk mengubah kategori dalam data menjadi angka. Teknik ini sering digunakan untuk data dengan kategori biner, seperti 'ya' dan 'tidak' menjadi nilai numerik, seperti 1 dan 0.

2. **One Hot Encoding**  
   One Hot Encoding adalah teknik yang mengubah setiap nilai kategori menjadi fitur biner terpisah. Setiap kategori diwakili oleh kolom baru dengan nilai 0 atau 1. Misalnya, untuk kategori "Merah", "Hijau", dan "Biru", kita akan membuat tiga kolom terpisah, dengan satu kolom yang bernilai 1 untuk kategori yang ada, sementara yang lainnya bernilai 0.

3. **Ordinal Encoding**  
   Ordinal Encoding digunakan untuk data kategorikal yang memiliki urutan tertentu. Setiap kategori diberikan nilai numerik yang mencerminkan urutan atau ranking. Misalnya, untuk kategori "Rendah", "Sedang", dan "Tinggi", kita bisa memberikan nilai 1, 2, dan 3, yang menunjukkan urutan dari yang terendah ke yang tertinggi.

**Encoding Kategorikal dilakukan terhadap 3 variabel, yaitu :**
```
- Extracurricular_Activities : Apakah Siswa Berpartisipasi dalam kegiatan ekstrakurikuler
- Internet_Access : Apakah Siswa Memiliki Akses ke Internet
- Learning_Disabilities : Apakah Siswa Memiliki Gangguan Pembelajaran
```
Karena masing-masing dari empat variabel tersebut hanya memiliki kategori ya (iya) dan tidak (tidak).

**One Hot Encoding diterapkan pada 2 variabel, yaitu :**
```
- School_Type : Jenis sekolah yang dihadiri siswa (Negeri, Swasta)
- Gender : Jenis kelamin siswa (Laki-laki, Perempuan)
```
Karena kategori Gender tidak memiliki urutan tertentu (nominal).

**Encoding Ordinal dilakukan terhadap 8 variabel, yaitu :**
```
- Parental_Involvement : Tingkat keterlibatan orang tua dalam pendidikan siswa (Rendah, Sedang, Tinggi)
- Access_to_Resources : Ketersediaan akses ke sumber daya pendidikan (Rendah, Sedang, Tinggi)
- Motivation_Level : Tingkat motivasi siswa (Rendah, Sedang, Tinggi)
- Family_Income : Tingkat pendapatan keluarga (Rendah, Sedang, Tinggi)
- Teacher_Quality : Kualitas pengajaran (Rendah, Sedang, Tinggi)
- Peer_Influence : Pengaruh teman sebaya terhadap kinerja akademik (Positif, Netral, Negatif)
- Parental_Education_Level : Tingkat pendidikan tertinggi orang tua (Sekolah Menengah, Perguruan Tinggi, Pascasarjana)
- Distance_from_Home : Jarak dari rumah ke sekolah (Dekat, Sedang, Jauh)
```
Karena ada urutan dan makna yang jelas, data diatas termasuk dalam kategori ordinal.

### Data Splitting
Split data dilakukan untuk membagi dataset menjadi bagian pelatihan dan pengujian. Ini penting untuk mengevaluasi kinerja model pada data yang tidak terlihat, mencegah overfitting, dan memastikan model dapat generalisasi dengan baik. Pembagian data menjadi data training dan data testing dilakukan dengan rasio sebagai berikut:

- Data training sebesar 80% untuk melatih model
- Data testing sebesar 20% untuk menguji model

## Modeling
Seluruh model yang akan dibuat tidak menggunakan hyperparameter tuning melainkan akan menggunakan beberapa algoritma dan memilih model terbaik sebagai solusi. Sesuai solusi yang ditawarkan pada bagian **_Solution Statement_**, beberapa algoritma yang akan digunakan untuk masalah regresi pada proyek ini adalah _Linear Regression_, _Decision Tree_, _Random Forest_, _Gradient Boosting_, dan _Support Vector regression_. Berikut adalah analisis kelebihan dan kekurangan dari masing-masing algoritma yang digunakan dalam proyek ini:

| **Model**               | **Kelebihan**                                                                                                                                       | **Kekurangan**                                                                                                  |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| **Linear Regression (LR)** | - Sederhana dan mudah dipahami. <br> - Cepat dalam pelatihan dan prediksi. <br> - Memiliki interpretasi yang jelas (koefisien menunjukkan pengaruh variabel). | - Hanya dapat menangkap hubungan linear. <br> - Sensitif terhadap outlier. <br> - Mengasumsikan hubungan linear. |
| **Decision Tree (DT)**    | - Mudah diinterpretasikan dan divisualisasikan. <br> - Mampu menangkap hubungan non-linear. <br> - Tidak memerlukan scaling data.                     | - Rentan terhadap overfitting, terutama dengan data yang kompleks. <br> - Sensitif terhadap perubahan kecil.    |
| **Random Forest (RF)**   | - Lebih robust dibandingkan Decision Tree, mengurangi risiko overfitting. <br> - Mampu menangkap interaksi yang kompleks antar fitur. <br> - Memberikan estimasi pentingnya fitur. | - Lebih lambat dalam pelatihan dan prediksi. <br> - Kurang interpretatif dibandingkan model linear. <br> - Memerlukan lebih banyak memori. |
| **Gradient Boosting (GB)**| - Mampu menangkap hubungan non-linear yang kompleks. <br> - Umumnya memberikan performa yang sangat baik dalam banyak kasus. <br> - Mampu mengatasi missing values. | - Rentan terhadap overfitting jika tidak dituning dengan baik. <br> - Lebih lambat dalam pelatihan. <br> - Memerlukan pemahaman yang lebih dalam tentang hyperparameter. |
| **Support Vector Regression (SVR)** | - Mampu menangkap hubungan non-linear dengan kernel yang tepat. <br> - Robust terhadap overfitting, terutama di dimensi tinggi. <br> - Efektif pada dataset kecil hingga menengah. | - Tidak efisien pada dataset yang sangat besar. <br> - Memerlukan pemilihan kernel yang tepat dan tuning hyperparameter. <br> - Sulit dalam interpretasi model. |

Berikut adalah sintaks kode Python untuk instansiasi algoritma-algoritma yanng digunakan, pelatihan model, dan prediksi nilai oleh model:

**Linear Regression**
```
# Membuat dan melatih model regresi linier
model_lr = LinearRegression()
model_lr.fit(X_train, y_train)

# Prediksi
predictions_lr = model_lr.predict(X_test)
```

**Decision Tree**
```
# Membuat dan melatih model decision tree
model_dt = DecisionTreeRegressor(max_depth=10)
model_dt.fit(X_train, y_train)

# Prediksi dan evaluasi
predictions_dt = model_dt.predict(X_test)
```

**Random Forest**
```
# Membuat dan melatih model random forest
model_rf = RandomForestRegressor(n_estimators=100, random_state=30)
model_rf.fit(X_train, y_train)

# Prediksi
predictions_rf = model_rf.predict(X_test)
```

**Gradient Boosting**
```
# Membuat dan melatih model gradient boosting
model_gb = GradientBoostingRegressor(n_estimators=100, learning_rate=0.1, max_depth=3)
model_gb.fit(X_train, y_train)

# Prediksi dan evaluasi
predictions_gb = model_gb.predict(X_test)
```

**Support Vector Regression (SVR)**
```
# Membuat dan melatih model support vector regression
model_svr = SVR(kernel='rbf')
model_svr.fit(X_train, y_train)

# Prediksi dan evaluasi
predictions_svr = model_svr.predict(X_test)
```

### Contoh 10 Data Prediksi
Berikut adalah 10 contoh perbandingan nilai asli dan hasil prediksi model yang digunakan:

| **Index** | **y_true** | **prediksi_LR** | **prediksi_DT** | **prediksi_RF** | **prediksi_GB** | **prediksi_SVR** |
|-----------|------------|-----------------|-----------------|-----------------|-----------------|------------------|
| 3024      | 62         | 62.123519       | 61.625000       | 63.71           | 63.707048       | 63.343930        |
| 2754      | 65         | 65.053911       | 64.888889       | 64.17           | 65.266467       | 63.599576        |
| 6363      | 70         | 69.709080       | 67.287500       | 68.32           | 68.856883       | 68.401405        |
| 3753      | 63         | 63.315235       | 62.645161       | 63.10           | 62.564249       | 63.268075        |
| 5154      | 62         | 61.858399       | 61.285714       | 61.59           | 61.404107       | 62.536896        |
| 2339      | 66         | 65.883455       | 66.500000       | 66.75           | 66.371123       | 66.859308        |
| 3500      | 68         | 67.799348       | 68.000000       | 69.08           | 68.613654       | 68.869134        |
| 1563      | 66         | 66.603065       | 65.000000       | 68.31           | 67.139535       | 65.750518        |
| 4493      | 65         | 64.944518       | 65.650000       | 65.15           | 65.212079       | 65.453077        |
| 1001      | 72         | 72.611754       | 71.500000       | 72.90           | 72.266877       | 72.486120        |

Berdasarkan tabel di atas, kita dapat melihat bahwa model Linear Regression (LR) memiliki prediksi yang paling mendekati nilai aktual (y_true) di antara model-model yang dibandingkan.

## Evaluation
### Metrik Evaluasi
Berikut adalah metrik evaluasi yang digunakan:

1. **Mean Squared Error (MSE)**  
   Formula:
   
   MSE = $\frac{1}{n} \sum_{i=1}^{n} (y_{\text{true},i} - y_{\text{pred},i})^2$
   
   Dimana:  
   - $\( y_{\text{true},i} \)$ adalah nilai sebenarnya untuk data ke-\(i\).  
   - $\( y_{\text{pred},i} \)$ adalah nilai prediksi untuk data ke-\(i\).  
   - $\( n \)$ adalah jumlah data.  

3. **Mean Absolute Error (MAE)**  
   Formula:
   
   MAE = $\frac{1}{n} \sum_{i=1}^{n} \lvert y_{\text{true},i} - y_{\text{pred},i} \rvert$

   Dimana:  
   - $\( y_{\text{true},i} \)$ adalah nilai sebenarnya untuk data ke-\(i\).  
   - $\( y_{\text{pred},i} \)$ adalah nilai prediksi untuk data ke-\(i\).  
   - $\( n \)$ adalah jumlah data.  

### Evaluasi Model
Berikut adalah hasil metrik yang didapatkan dari masing-masing proses evaluasi algoritma:

| Model | Mean Squared Error (MSE) | Mean Absolute Error (MAE) |
|-------|--------------------------|---------------------------|
| LR    | 3.508515                 | 0.454501                  |
| DT    | 13.946788                | 1.773880                  |
| RF    | 5.225100                 | 1.142210                  |
| GB    | 4.387732                 | 0.832583                  |
| SVR   | 5.093583                 | 1.139980                  |

Lebih jelasnya, hasil evaluasi model-model yang digunakan digambarkan pada grafik berikut:

![image](https://github.com/user-attachments/assets/e1fbe47c-94a6-4beb-8858-347cdcec3672)

- Berdasarkan grafik "Perbandingan Performa Model", model Linear Regression (LR) memiliki nilai Mean Squared Error (MSE) terendah, yaitu 3.51, serta nilai Mean Absolute Error (MAE) yang juga cukup rendah. Ini menunjukkan bahwa model Linear Regression memiliki akurasi prediksi terbaik di antara model-model yang dibandingkan.

- Model Gradient Boosting (GB) juga menunjukkan performa yang sangat baik, dengan nilai MSE 4.39 dan MAE yang relatif rendah. Meskipun sedikit lebih tinggi dibandingkan Linear Regression, Gradient Boosting masih merupakan salah satu model terbaik dalam kasus ini.

- Sementara itu, model Random Forest (RF) memiliki nilai MSE 5.23 dan MAE yang sedikit lebih tinggi. Support Vector Regression (SVR) memiliki nilai MSE 5.09 dan MAE yang juga lebih tinggi daripada Linear Regression dan Gradient Boosting. Meskipun masih menunjukkan performa yang cukup baik, model-model ini tidak unggul dibandingkan Linear Regression dan Gradient Boosting.

- Model Decision Tree (DT) memiliki nilai MSE paling tinggi, yaitu 12.82, serta nilai MAE yang juga lebih buruk daripada model-model lainnya. Ini menunjukkan bahwa model Decision Tree memiliki performa paling rendah di antara model-model yang dibandingkan.

**Secara keseluruhan, dapat disimpulkan bahwa model Linear Regression merupakan model terbaik berdasarkan nilai MSE dan MAE yang paling rendah.**

## Conclusion
Proyek ini bertujuan untuk memahami faktor-faktor yang memengaruhi kinerja akademik siswa, menentukan faktor utama, serta membangun model prediksi nilai ujian. Berdasarkan analisis data dan eksperimen model, berikut adalah poin-poin utama kesimpulan yang dapat menjawab problem statement dan mencapai goals proyek ini:

### Hubungan Faktor dengan Nilai Ujian  
Faktor-faktor seperti **jumlah jam belajar**, **tingkat motivasi**, **kehadiran**, **keterlibatan orang tua**, **kualitas guru**, dan **akses sumber daya pendidikan** memiliki hubungan signifikan dengan nilai ujian. Faktor lain seperti **aktivitas ekstrakurikuler** dan **jam tidur** juga berkontribusi terhadap hasil akademik siswa.

### Faktor Utama yang Mempengaruhi Nilai Ujian  
Berdasarkan analisis feature importance dan korelasi, **motivasi siswa**, **jam belajar**, dan **kualitas pengajaran** menjadi faktor yang memiliki pengaruh terbesar terhadap nilai ujian.
- **Motivasi siswa**: Berdasarkan tabel rata-rata skor ujian, siswa dengan motivasi tinggi memiliki rata-rata skor ujian tertinggi (67.74), dibandingkan dengan yang memiliki motivasi sedang atau rendah​.
- **Jam belajar**: Distribusi data menunjukkan bahwa siswa yang belajar lebih banyak jam cenderung memiliki nilai ujian yang lebih baik, yang mencerminkan hubungan positif antara jam belajar dan skor.
- **Kualitas pengajaran**: Siswa dengan kualitas pengajaran tinggi menunjukkan rata-rata skor ujian yang lebih baik (67.66), dibandingkan dengan yang menerima pengajaran berkualitas sedang atau rendah​.

### Model Prediksi Terbaik  
Dari berbagai model yang diuji (**Linear Regression**, **Decision Tree**, **Random Forest**, **Gradient Boosting**, dan **Support Vector Regression**), **Linear Regression** menunjukkan performa terbaik dengan nilai **MSE terendah (3.51)** dan **MAE terendah (0.45)**. Hal ini mengindikasikan bahwa model ini memiliki kemampuan prediksi yang paling akurat dalam kasus ini.

### Implikasi Praktis  
- **Untuk Sekolah**: Fokus pada peningkatan kualitas guru dan memberikan dukungan motivasi kepada siswa. Program tambahan, seperti sesi bimbingan belajar, dapat dirancang untuk siswa dengan hasil prediksi rendah.  
- **Untuk Orang Tua**: Keterlibatan aktif dalam pendidikan anak dan menciptakan lingkungan belajar yang kondusif dapat meningkatkan hasil akademik.  
- **Untuk Kebijakan Pendidikan**: Investasi dalam infrastruktur pendidikan, akses sumber daya, dan pelatihan guru dapat memberikan dampak positif yang signifikan.  

### Rekomendasi Intervensi Berbasis Data  
1. Program pengembangan motivasi intrinsik siswa.  
2. Pengelolaan jam belajar dan jadwal tidur yang sehat.  
3. Peningkatan keterlibatan orang tua melalui workshop atau seminar.

