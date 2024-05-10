# PCD_UTS_202231113_2024_ITPLN

Pada laporan ini, saya Muhammad Faqih Nefawan dengan NIM 202231113 akan menjelaskan pengerjaan proyek UTS yang dikerjakan terkait dengan deteksi warna dan pencarian ambang pada gambar RGB dengan Python.

## Pendahuluan
### Latar Belakang
Dengan banyak aplikasi praktis dalam berbagai bidang, pengolahan gambar digital terus berkembang dengan cepat. Deteksi warna adalah bagian penting dari pengolahan gambar karena memungkinkan komputer untuk mengenali dan memisahkan objek berdasarkan warnanya. Teknik ini sangat bermanfaat untuk pengenalan objek dalam gambar dan video, serta untuk segmentasi gambar medis. Deteksi warna juga memiliki banyak aplikasi di luar bidang pengolahan citra. Ini termasuk analisis kualitas produk, kontrol kualitas industri, robotika, dan navigasi. Kami akan menggunakan library OpenCV dan bahasa pemrograman Python untuk menerapkan teknik deteksi warna dan pencarian ambang pada gambar berwarna RGB dalam proyek ini.

### Tinjauan pustaka
Thresholding dan algoritma Otsu digunakan untuk mendeteksi warna pada proyek ini. Thresholding mengklasifikasikan pixel berdasarkan intensitas warna, sedangkan algoritma Otsu mencari nilai threshold optimal untuk memaksimalkan perbedaan antara background dan foreground. Menggabungkan gambar biner dari setiap channel warna menghasilkan informasi warna yang lebih lengkap.


### Tujuan
- Mempelajari dan menerapkan metode deteksi warna pada gambar RGB menggunakan library OpenCV. 
- Menggunakan metode Otsu untuk menemukan nilai ambang optimal untuk deteksi warna.
- Memahami dan menganalisis hasil deteksi warna menggunakan histogram dan visualisasi.
- Mendokumentasikan langkah-langkah proyek dan hasilnya.

## Langkah Pengerjaan
### Deteksi Warna pada Citra
#### Membaca Citra
Langkah pertama yang dilakukan adalah membaca citra RGB dari file menggunakan fungsi cv2.imread. Citra yang digunakan dalam proyek ini adalah file "namargb.jpg".
#### Ekstraksi Channel Warna
Menggunakan pemanggilan berdasarkan indeks pada array NumPy, channel warna Biru, Hijau, dan Merah dibuat dari citra RGB.
#### Deteksi Warna dengan Thresholding
Nilai threshold dipilih secara manual dalam kode ini (200 untuk merah, 100 untuk hijau, dan 120 untuk biru), dan algoritma ambang digunakan untuk mendeteksi objek berwarna dalam citra.
#### Visualisasi Hasil Deteksi Warna
Untuk menunjukkan hasil deteksi warna, menggunakan library matplotlib.pyplot untuk membuat subplot yang menampilkan gambar asli dan gambar biner hasil thresholding pada masing-masing channel warna. Pada hasil visualisasi menunjukkan bahwa warna yang teridentifikasi akan menjadi putih, dengan nilai mendekati 255.
#### Analisis Histogram
Histogram menunjukkan distribusi intensitas pixel pada gambar. Ini dihitung untuk citra asli dan citra biner hasil thresholding pada tiap channel warna.
### Mencari Ambang Batas
#### Pencarian Thresholdi yang Optimal dengan Metode Otsu
Nilai threshold yang ditetapkan manual diganti dengan nilai threshold optimal yang dihitung menggunakan Otsu's method. Otsu's method adalah algoritma otomatis untuk mencari threshold optimal yang memaksimalkan perbedaan antara foreground dan background pada citra biner.
#### Menggabungkan Channel Warna Hasil Thresholding
Citra biner hasil thresholding digabungkan menggunakan operasi bitwise OR. Kombinasi ini menghasilkan citra baru yang mendeteksi objek berwarna merah atau biru (Red-Blue) dan objek berwarna merah, hijau, dan biru (Red-Green-Blue).
#### Visualisasi Hasil Akhir
Visualisasi menunjukkan bahwa thresholding berhasil mendeteksi objek berwarna dalam citra. Metode Otsu menghasilkan nilai ambang terbaik, namun detail objek mungkin masih hilang. Penggabungan citra biner memberikan informasi warna yang lebih lengkap dan detail objek yang lebih terjaga. Pemilihan nilai threshold dan metode thresholding yang tepat sangat penting untuk hasil deteksi warna yang optimal. Metode Algoritma Otsu menghasilkan nilai ambang batas optimal dengan menganalisis distribusi intensitas pixel melalui histogram. Nilai ambang batas optimal dipilih untuk meminimalkan kesalahan klasifikasi pixel dan menghasilkan deteksi warna yang akurat.

## Penutup
### Kesimpulan
Dengan menggunakan library OpenCV dan Python untuk mencapai tujuan deteksi warna dan pencarian ambang pada gambar RGB dalam proyek ini. Metode Algoritma Otsu terbukti efektif dalam menemukan nilai ambang ideal untuk deteksi warna. Dengan menggunakan subplot dan histogram, hasil deteksi warna dapat divisualisasikan secara efektif.
### Saran
- Mencoba algoritma thresholding yang berbeda dari metode Otsu dan membandingkan hasilnya.
- Menggunakan metode deteksi warna pada gambar dalam berbagai kondisi pencahayaan.
- Mempelajari metode pengolahan gambar khusus untuk deteksi warna.

