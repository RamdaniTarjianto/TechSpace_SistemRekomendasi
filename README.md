# Progress TechSpace Media

#### Nama   : Ramdani Tarjianto
#### Role  : Data Scientist

#### MEMBUAT SISTEM REKOMENDASI ARTIKEL BERDASARKAN PREVERENSI PENGGUNA

#### Yang dilakukan:
 1. Data Collection
 2. Data Extraction
 3. Data Cleaning
 4. Modeling


### 1. Data Collection (Proses Pengumpulan Data)
Untuk tahapan pengumpulan data, saya menggunakan library python yang bernama BeautifulSoup. Sumber data yang saya gunakan berasal dari dua portal berita terkemuka di Indonesia, yaitu Kompas dan Sindo News. Dalam tahapan ini, saya fokus pada sub-kategori teknologi dan mengambil data artikel yang berkaitan dengan sub-kategori tersebut untuk diolah dan dianalisa lebih lanjut. Library BeautifulSoup mempermudah saya dalam mengambil data dengan cepat dan efisien, sehingga saya dapat menghemat waktu dan tenaga dalam tahapan pengumpulan data.

Berikut ini adalah kode yang digunakan dalam tahap pengumpulan data:
![code data collection](https://raw.githubusercontent.com/RamdaniTarjianto/TechSpace_SistemRekomendasi/master/images/code%20data%20collection.PNG)

Berikut adalah kumpulan file yang diperoleh melalui proses pengumpulan data:
![hasil data collection](https://raw.githubusercontent.com/RamdaniTarjianto/TechSpace_SistemRekomendasi/master/images/hasil%20data%20collection.PNG)

![hasil data collection](https://raw.githubusercontent.com/RamdaniTarjianto/TechSpace_SistemRekomendasi/master/images/gambar%20plot.png)

Dalam tahapan pengumpulan data, saya menggunakan library python BeautifulSoup untuk mengambil data dari portal berita Indonesia, yaitu Kompas dan Sindo News. Saya menentukan sub-kategori teknologi sebagai fokus pengambilan data dan berhasil mengumpulkan lebih dari 5000 artikel. Dari 5000 artikel tersebut, terdapat 9 kategori yang berbeda, dimana kategori Telco adalah kategori yang paling banyak muncul dan kategori advertorial tekno adalah kategori yang paling sedikit.

![hasil data collection](https://raw.githubusercontent.com/RamdaniTarjianto/TechSpace_SistemRekomendasi/master/images/final%20dataset.PNG)
Saya telah berhasil mengumpulkan 5000 data dari tahapan data collection dan data tersebut sudah siap untuk diproses lebih lanjut dalam tahapan berikutnya.


### 2. Data Extraction (Proses Pemilihan Variable)
Dalam data extraction, saya memastikan untuk memilih variabel yang relevan dan lengkap agar sistem rekomendasi yang akan saya buat dapat berjalan dengan baik. Variabel-variabel yang saya pilih antara lain: 
- judul artikel 
- isi artikel 
- tanggal rilis 
- nama penulis 
- kategori 
- link photo

Hal ini penting dilakukan agar sistem rekomendasi yang akan saya buat dapat menentukan rekomendasi berdasarkan preferensi pengguna atau yang dikenal sebagai content-based filtering dengan tepat. Dengan memiliki informasi lengkap tentang data artikel, backend dan frontend dapat memudahkan untuk menampilkan gambar yang relevan dengan data artikel yang sudah saya kumpulkan sehingga memberikan pengalaman pengguna yang lebih baik.

![hasil data collection](https://raw.githubusercontent.com/RamdaniTarjianto/TechSpace_SistemRekomendasi/master/images/hasil%20data%20collection%201.PNG)

### 3. Data Cleaning (Proses Pembersihan Data)
Dalam tahapan data cleaning, saya melakukan beberapa langkah penting untuk memastikan kelengkapan dan keakuratan data. Langkah-langkah yang saya lakukan antara lain: 
1. membersihkan kalimat yang tidak perlu seperti simbol dan tanda baca yang tidak relevan 
2. menyamakan nama kolom kategori yang diterapkan oleh penulis yang berbeda 
3. menyamakan format tanggal agar sesuai dengan standar yang sudah ditentukan sehingga memudahkan dalam analisis dan visualisasi data.

Langkah-langkah ini sangat penting dilakukan untuk memastikan kelengkapan dan keakuratan data sehingga dapat dipercaya dan dianalisis dengan baik.

### 4. Modeling
Dalam tahap pembuatan sistem rekomendasi, saya memutuskan untuk menggunakan teknik Content Based Filtering. Tujuannya adalah untuk merekomendasikan artikel yang memiliki kesamaan dengan artikel yang pernah disukai oleh pengguna. Dalam hal ini, target rekomendasi adalah judul artikel. Sistem akan menganalisa data riwayat interaksi pengguna dan mencari artikel dengan judul yang mirip dengan judul artikel yang pernah dibaca sebelumnya. Dengan demikian, saya berharap dapat memberikan rekomendasi artikel yang relevan dan berkualitas bagi pengguna.

TF-IDF adalah metode yang digunakan untuk menentukan nilai frekuensi kemunculan kata-kata dalam sebuah dokumen atau artikel. Tujuannya adalah untuk menemukan representasi fitur yang penting dari setiap kalimat dalam judul artikel. Proses ini bertujuan untuk membantu sistem merekomendasikan artikel yang relevan dengan minat dan preferensi pengguna.

Cosine Similarity adalah metode untuk menghitung derajat kesamaan antar judul artikel. Dengan menggunakan metode ini, sistem akan membandingkan judul artikel yang dibaca sebelumnya dengan judul artikel baru, dan memberikan skor kesamaan antar kedua judul tersebut. Skor ini akan membantu sistem dalam memutuskan apakah judul artikel baru ini relevan untuk direkomendasikan kepada pengguna atau tidak.

![hasil data collection](https://raw.githubusercontent.com/RamdaniTarjianto/TechSpace_SistemRekomendasi/master/images/hasil%20sistem%20rekomendasi.png)
