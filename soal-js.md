
# Table of Contents

1.  [Program Perpustakaan](#org67770b8)
2.  [Program Resep Makanan](#orgc3a8980)
3.  [Program Penggajian Karyawan](#org33e6321)
4.  [Program Daftar Belanja](#orgc2bd141)
5.  [Program Registrasi Event Jejepangan](#orgdad7403)
6.  [Program Pencatatan Silsilah Keluarga](#orgeb00178)


<a id="org67770b8"></a>

# Program Perpustakaan

Pak Tono adalah seorang pustakawan yang memerlukan sebuah aplikasi perpustakaan
untuk membantu pekerjaannya dalam mengelola buku-buku yang ada di perpustakaan.
Pak Tono berharap dalam program ini dia bisa mencatat informasi buku yang terdiri
dari judul buku, pengarang, tahun terbit, dan stok buku. Selain itu, pak Tono
juga menginginkan program ini bisa mencatat peminjamn buku yang terdiri dari buku
yang dipinjam, nama peminjam, tanggal pinjam, dan tanggal pengembalian. 

Adapun spesifikasi teknis yang harus dipenuhi oleh aplikasi ini adalah sebagai
berikut:

1.  Aplikasi console yang dapat dibuat dengan bahasa pemrograman Javascript
2.  Data aplikasi disimpan dalam file plain text dengan ekten .txt atau .json
3.  Aplikasi memiliki fitur menambahkan buku baru, mencari data buku, dan menghapus
    data buku
4.  Aplikasi memiliki fitur menambahkan peminjam buku, mencari data peminjaman, dan menghapus
    data peminjaman. Adapun ketentuan dari peminjaman buku adalah:
    -   Jika buku yang dipinjam tersedia, maka buku tersebut dapat dipinjam
    -   Jika buku yang dipinjam tidak tersedia, maka buku tersebut tidak dapat dipinjam
    -   Jika buku yang dipinjam tersedia, maka stok buku tersebut berkurang 1
5.  Aplikasi dapat dijalankan dengan menggunakan argument. Sebagai contoh, untuk menambahkan
    data buku, maka perintah yang dijalankan adalah:
    
        node main.js tambah_buku -judul="Belajar Go" -pengarang="Agus Kopling" -tahun=2020 -stok=10
    
    Sedangkan untuk menambahkan data peminjaman buku, maka perintah yang dijalankan adalah:
    
        node main.js tambah_pinjam -judul="Belajar Go" -peminjam="Tugek DPS48" -tgl_pinjam="2020-01-01" -tgl_kembali="2020-01-08"

Ketentuan khusus:

-   Definisi data buku dan peminjam harus dibuat dalam bentuk object
-   Definisi data peminjaman buku juga harus dibuat dalam bentuk object
-   Daftar data buku dan peminjam disimpan dalam bentuk slice atau array

Pak Tono menggambarkan program yang dia inginkan sebagai berikut:

    Program Perpustakaan
    ====================
    1. Tambah Buku
    2. Cari Buku
    3. Hapus Buku
    4. Tambah Peminjaman
    5. Cari Peminjaman
    6. Hapus Peminjaman
    7. Keluar
    Pilih Menu [1-7]: 1
    Judul Buku: Belajar Go
    Pengarang: Agus Kopling
    Tahun Terbit: 2020
    Stok: 10
    Buku berhasil ditambahkan!
    Pilih Menu [1-7]: 2
    Judul Buku: Belajar Go
    Buku ditemukan!
    Judul Buku: Belajar Go
    Pengarang: Agus Kopling
    Tahun Terbit: 2020
    Stok: 10
    Pilih Menu [1-7]: 3
    1. Belajar Go
    2. Belajar Javascript
    3. Belajar Pemrograman Web
    Pilih Buku yang akan dihapus [1-3]: 1
    Buku berhasil dihapus!
    Pilih Menu [1-7]: 4
    1. Belajar Go
    2. Belajar Javascript
    3. Belajar Pemrograman Web
    Pilih buku yang akan dipinjam [1-2]: 1
    Buku yang dipinjam adalah Belajar Go
    Nama Peminjam: Tugek DPS48
    Tanggal Pinjam: 2020-01-01
    Tanggal Kembali: 2020-01-08
    Peminjaman berhasil ditambahkan!
    Pilih Menu [1-7]: 5
    Masukan Judul Buku: Belajar Go
    Peminjaman ditemukan!
    Judul Buku: Belajar Go
    Nama Peminjam: Tugek DPS48
    Tanggal Pinjam: 2020-01-01
    Tanggal Kembali: 2020-01-08
    Pilih Menu [1-7]: 6
    1. Belajar Go - Tugek DPS48
    2. Belajar Javascript - Tugus Tamvan
    Pilh Peminjaman yang akan dihapus [1-2]: 1
    Peminjaman berhasil dihapus!


<a id="orgc3a8980"></a>

# Program Resep Makanan

Ibu Markonah Supratman Purbalingga Extractsaridevi Ajeng Rembulan S.Kom adalah adalah
seorang ibu rumah tangga yang sangat hobi memasak. Dia memiliki banyak resep makanan
yang terbukti sudah membuat suaminya gemuk 10 kg dalam 1 bulan. Ibu Markonah ingin mewariskan
resep-resep masakannya kepada anaknya. Maka dari itu dia meminta bantuan kepada 3 mahasiswa
Primakara University untuk membuat sebuah program yang dapat mencatat resep masakan yang 
dimiliki oleh ibu Markonah. Ibu Markonah berharap program ini dapat digunakan dalam mencatat
resep makanan yang terdiri dari nama resep, bahan-bahan, dan langkah-langkah pembuatan. 
Setiap daftar bahan-bahan yang ada juga disertakan dengan jumlahnya. Ibu Markonah juga ingin
terdapat fitur untuk mencari resep berdasarkan nama resep. 

Adapun spesifikasi teknis yang harus dipenuhi oleh aplikasi ini adalah sebagai berikut:

1.  Aplikasi console yang dapat dibuat dengan bahasa pemrograman Javascript
2.  Data aplikasi disimpan dalam file plain text dengan ekten .txt atau .json
3.  Aplikasi memiliki fitur menambahkan resep baru, mencari data resep, dan menghapus
    data resep

Berikut merupakan contoh program yang diinginkan oleh ibu Markonah:

    Program Resep Makanan
    =====================
    1. Tambah Resep
    2. Cari Resep
    3. Hapus Resep
    4. Keluar
    Pilih Menu [1-4]: 1
    Nama Resep: Nasi Goreng
    Masukan bahan-bahan (tekan underscore untuk menghentikan penambahan bahan):
    Bahan ke - 1: Nasi
    Satuan bahan ke -1: piring
    Jumlah bahan ke -1: 1
    Bahan ke - 2: Telur
    Satuan bahan ke -2: butir
    Jumlah bahan ke -2: 2
    Bahan ke - 3: _
    Masukan langkah-langkah (tekan underscore untuk menghentikan penambahan langkah):
    Langkah ke - 1: Goreng telur
    Langkah ke - 2: Masukan nasi
    Langkah ke - 3: _
    Resep berhasil ditambahkan!
    Pilih Menu [1-4]: 2
    Masukan nama resep: Nasi Goreng
    Resep ditemukan!
    Nama Resep: Nasi Goreng
    Bahan-bahan:
    1. Nasi - 1 piring
    2. Telur - 2 butir
    Langkah-langkah:
    1. Goreng telur
    2. Masukan nasi
    Pilih Menu [1-4]: 3
    1. Nasi Goreng
    2. Nasi Uduk
    3. Nasi Kuning
    Pilih Resep yang akan dihapus [1-3]: 1
    Resep berhasil dihapus!


<a id="org33e6321"></a>

# Program Penggajian Karyawan

Neng Wijah adalah enterprener yang memiliki startup Kripik Singkong yang sangat sukses. Dia dijuluki
Gadis Kripik karena kripiknya yang berkualitas tinggi dan disukai banyak reviewer dan influencer
kuliner. Di tahun 2024 neng wijah berencana akan melakukan IPO sehingga dia perlu memastikan startupnya
memiliki inovasi yang keren. Salah satu usaha yang dia lakukan adalah menyediakan layanan antar
kripik langsung ke pintu rumah pelanggan. Neng Wijah memiliki armada sebanyak 10 motor yang digunakan
untuk mengantar kripik. Neng Wijah juga memiliki 10 karyawan yang bertugas untuk mengantar kripik
ke rumah pelanggan. Neng Wijah ingin membuat sebuah program yang dapat membantu dia dalam mengelola
gaji karyawan. Program ini akan mencatat data karyawan yang terdiri dari nama karyawan, gaji pokok, dan
tunjangan. Program ini juga mencatat performa pengantaran yang dilakukan oleh karyawan. Performa
pengantaran ini terdiri dari jumlah pengantaran yang dilakukan oleh karyawan dan jumlah pengantaran
yang berhasil dilakukan oleh karyawan. Neng Wijah juga ingin program ini dapat menghitung gaji karyawan
berdasarkan performa pengantaran yang dilakukan oleh karyawan.
Adapun ketentuan penggajian adalah sebagai berikut:

1.  Gaji pokok karyawan adalah Rp 4.000.000
2.  Jika karyawan memiliki istri, maka karyawan mendapatkan tunjangan sebesar Rp 1.000.000
3.  Jika karyawan memiliki anak, maka karyawan mendapatkan tunjangan sebesar Rp 500.000 per anak
4.  Upah per pengantaran adalah Rp 10.000
5.  Jika karyawan melakukan pengantaran berhasil lebih dari 10 kali, maka karyawan mendapatkan bonus sebesar
    Rp 500.000
6.  Jika karyawan berhasil melakukan pengantaran lebih dari 50 kali, maka karyawan mendapatkan bonus
    sebesar Rp 1.000.000
7.  Jika karyawan melakukan pengantaran berhasil kurang dari 5 kali, maka karyawan akan menderita pemotongan gaji
    sebesar Rp 500.000
8.  Jika terjadi pemotongan gaji, maka tunjangan karyawan juga akan dipotong sebesar 50%

Berikut merupakan contoh program yang diinginkan oleh Neng Wijah:

    Program Penggajian Karyawan
    ==========================
    1. Tambah Karyawan
    2. Cari Karyawan
    3. Hapus Karyawan
    4. Tambah Pengantaran
    5. Cari Pengantaran
    6. Hapus Pengantaran
    7. Hitung Gaji
    8. Keluar
    Pilih Menu [1-8]: 1
    Nama Karyawan: Tugus Tamvan
    Punya Istri (y/n): y
    Punya Anak (y/n): y
    Masukan jumlah anak: 2
    Karyawan berhasil ditambahkan!
    Pilih Menu [1-8]: 2
    Masukan nama karyawan: Tugus Tamvan
    Karyawan ditemukan!
    Nama Karyawan: Tugus Tamvan
    Keterangan: Sudah Menikah dan memiliki 2 anak
    Pilih Menu [1-8]: 3
    1. Tugus Tamvan
    2. Tugek DPS48
    Pilih Karyawan yang akan dihapus [1-2]: 1
    Karyawan berhasil dihapus!
    Pilih Menu [1-8]: 4
    1. Tugus Tamvan
    2. Tugek DPS48
    Pilih Karyawan yang akan melakukan pengantaran [1-2]: 1
    Masukan tujuan pengantaran: Jalan Satu Dua Tiga
    Apakah pengantaran berhasil (y/n): y
    Pengantaran berhasil ditambahkan!
    Pilih Menu [1-8]: 5
    1. Tugus Tamvan
    2. Tugek DPS48
    Pilih Karyawan yang akan dicari pengantarannya [1-2]: 1
    Pengantaran ditemukan!
    Nama Karyawan: Tugus Tamvan
    Jumlah Pengantaran: 10
    Jumlah Pengantaran Berhasil: 10
    Pilih Menu [1-8]: 6
    1. Tugus Tamvan
    2. Tugek DPS48
    Pilih Karyawan yang akan dihapus pengantarannya [1-2]: 1
    Pengantaran berhasil dihapus!
    Pilih Menu [1-8]: 7
    1. Tugus Tamvan
    2. Tugek DPS48
    Pilih Karyawan yang akan dihitung gajinya [1-2]: 1
    Gaji Tugus Tamvan adalah Rp 4.000.000
    Tunjangan Tugus Tamvan adalah Rp 1.500.000
    Upah Pengantaran Tugus Tamvan adalah Rp 100.000
    Bonus Tugus Tamvan adalah Rp 1.000.000
    Gaji Tugus Tamvan adalah Rp 6.500.000
    Pilih Menu [1-8]: 8

Adapun spesifikasi teknis yang harus dipenuhi oleh aplikasi ini adalah sebagai
berikut:

1.  Aplikasi console yang dapat dibuat dengan bahasa pemrograman Javascript
2.  Data aplikasi disimpan dalam file plain text dengan ekten .txt atau .json

Ketentuan khusus:

-   Definisi karyawan dibuat dalam bentuk object
-   Data pengantaran juga dibuat dalam bentuk object
-   Daftar karyawan dan pengantarn disimpan dalam bentuk slice atau array


<a id="orgc2bd141"></a>

# Program Daftar Belanja

Tugus Ganteng Ida Man Waynitia adalah seorang mahasiswa yang sangat suka belanja, tertuama
belanja ke pasar. Walaupun trend belanja online sedang marak, Tugus lebih memilih belanja
ke pasar karena dia suka melihat-lihat barang yang dijual di pasar. Namun seringkali, saat
Tugus sudah sampai di pasar, dia lupa barang apa saja yang harus dia beli. Oleh karena itu,
Tugus meminta bantuan kepada 3 mahasiswa Primakara University untuk membuat sebuah program
yang dapat membantu dia dalam mencatat daftar belanjaan yang harus dia beli. Program ini
akan mencatat daftar belanjaan yang terdiri dari nama barang dan jumlah barang yang harus
dibeli. Setiap daftar belanjaan juga disertakan dengan harga barang. Tugus juga ingin
program ini dapat menghitung total harga belanjaan yang harus dia bayarkan. Proses menambahkan
harga barang dan penghitungan dilakukan saat dia telah selesai berbelanja. Untuk mempermudah
ia melakukan pembelian barang, dia ingin memasukan setiap barang yang akan dibeli ke dalam
kategori-kategori. Kategori-kategori ini dapat dia tambahkan secara dinamis. Dalam program
yang ingin dibuat, dia juga ingin daftar belanjaan dapat dicari berdasarkan nama barang dan 
nama kategorinya. 

Adapun spesifikasi teknis yang harus dipenuhi oleh aplikasi ini adalah sebagai berikut:

1.  Aplikasi console yang dapat dibuat dengan bahasa pemrograman Javascript
2.  Data aplikasi disimpan dalam file plain text dengan ekten .txt atau .json
3.  Aplikasi memiliki fitur menambahkan daftar belanjaan, mencari data belanjaan, dan menghapus
    data belanjaan
4.  Aplikasi memiliki fitur menambahkan kategori, mencari data kategori, dan menghapus data kategori
5.  Aplikasi memiliki fitur menghitung total harga belanjaan

Berikut merupakan contoh program yang diinginkan oleh Tugus:

    Program Daftar Belanja
    ======================
    1. Tambah Kategori
    2. Cari Kategori
    3. Hapus Kategori
    4. Tambah Belanjaan
    5. Cari Belanjaan
    6. Hapus Belanjaan
    7. Hitung Total Belanjaan
    8. Keluar
    Pilih Menu [1-8]: 1
    Nama Kategori: Buah
    Satuan Kata Kunci: buah
    Kategori berhasil ditambahkan!
    Pilih Menu [1-8]: 2
    Masukan nama kategori: Buah
    Kategori ditemukan!
    Nama Kategori: Buah
    Pilih Menu [1-8]: 3
    1. Buah
    2. Sayur
    Pilih Kategori yang akan dihapus [1-2]: 1
    Kategori berhasil dihapus!
    Pilih Menu [1-8]: 4
    Daftar Kategori Tersedia:
    1. Buah
    2. Sayur
    Tambahkan rencana daftar belanja. Tekan underscore untuk menghentikan penambahan.
    Kategori Barang ke - 1 [1-2]: 1
    Nama Barang ke - 1: Apel
    Masukan jumlah barang ke - 1: 2
    Kategori Barang ke - 2 [1-2]: 1
    Nama Barang ke - 2: Jeruk
    Masukan jumlah barang ke - 2: 3
    Kategori Barang ke - 3 [1-2]: _
    Daftar belanja berhasil ditambahkan!
    Pilih Menu [1-8]: 5
    Masukan nama barang: Apel
    Belanjaan ditemukan!
    Nama Barang: Apel
    Jumlah Barang: 2
    Kateogri Barang: Buah
    Pilih Menu [1-8]: 6
    1. Apel
    2. Jeruk
    Pilih Barang yang akan dihapus [1-2]: 1
    Barang berhasil dihapus!
    Pilih Menu [1-8]: 7
    Berikut adalah daftar belanjaan:
    1. Apel - 2 buah
    Masukan harga beli: 15000
    Sub total harga belanjaan adalah Rp 30000
    2. Jeruk - 3 buah
    Masukan harga beli: 20000
    Sub total harga belanjaan adalah Rp 50000
    Total harga belanjaan adalah Rp 80000
    Pilih Menu [1-8]: 8


<a id="orgdad7403"></a>

# Program Registrasi Event Jejepangan

Tugus Tamvan adalah seorang mahasiswa yang sangat suka dengan budaya Jepang. Dia sangat
mengidolakan budaya Jepang, terutama anime. Dia juga sangat mengidolakan para cosplayer
yang berperan sebagai karakter anime. Dia sangat ingin bertemu dengan para cosplayer
tersebut. Oleh karena itu, dia meminta bantuan kepada 3 mahasiswa Primakara University
untuk membuat sebuah program yang dapat membantu dia dalam mengelola event-event yang
diadakan oleh para cosplayer. Program ini akan mencatat data event yang terdiri dari
nama event, tanggal event, dan lokasi event. Setiap event juga disertakan dengan
daftar cosplayer yang akan hadir dalam event tersebut. Daftar cosplayer ini terdiri
dari nama cosplayer, nama karakter yang diperankan, dan nama anime yang diperankan.
Tugus juga ingin program ini dapat mencari event berdasarkan nama event dan tanggal
event. Tugus juga ingin mengetahui event mana yang akan diadakan dalam 7 hari mendatang.

Adapun spesifikasi teknis yang harus dipenuhi oleh aplikasi ini adalah sebagai berikut:

1.  Aplikasi console yang dapat dibuat dengan bahasa pemrograman Javascript
2.  Data aplikasi disimpan dalam file plain text dengan ekten .txt atau .json
3.  Aplikasi memiliki fitur menambahkan event baru, mencari data event, dan menghapus
    data event
4.  Aplikasi memiliki fitur menambahkan cosplayer baru, mencari data cosplayer, dan menghapus
    data cosplayer
5.  Aplikasi memiliki fitur menambahkan cosplayer ke dalam event, mencari data cosplayer dalam
    event, dan menghapus data cosplayer dalam event
6.  Aplikasi memiliki fitur menampilkan event yang akan diadakan dalam 7 hari mendatang

Berikut merupakan contoh program yang diinginkan oleh Tugus:

    Program Registrasi Event Jejepangan
    ===================================
    1. Tambah Event
    2. Cari Event
    3. Hapus Event
    4. Tambah Cosplayer
    5. Cari Cosplayer
    6. Hapus Cosplayer
    7. Tambah Cosplayer ke Event
    8. Cari Cosplayer dalam Event
    9. Hapus Cosplayer dalam Event
    10. Event yang akan diadakan dalam 7 hari mendatang
    11. Keluar
    Pilih Menu [1-11]: 1
    Nama Event: Anime Festival
    Tanggal Event: 2020-01-01
    Lokasi Event: Jalan Satu Dua Tiga
    Event berhasil ditambahkan!
    Pilih Menu [1-11]: 2
    Masukan nama event: Anime Festival
    Event ditemukan!
    Nama Event: Anime Festival
    Tanggal Event: 2020-01-01
    Lokasi Event: Jalan Satu Dua Tiga
    Pilih Menu [1-11]: 3
    1. Anime Festival
    2. Anime Expo
    Pilih Event yang akan dihapus [1-2]: 1
    Event berhasil dihapus!
    Pilih Menu [1-11]: 4
    Nama Cosplayer: Tugus Tamvan
    Nama Karakter: Tugus Tamvan
    Nama Anime: Tugus Tamvan
    Cosplayer berhasil ditambahkan!
    Pilih Menu [1-11]: 5
    Masukan nama cosplayer: Tugus Tamvan
    Cosplayer ditemukan!
    Nama Cosplayer: Tugus Tamvan
    Nama Karakter: Tugus Tamvan
    Nama Anime: Tugus Tamvan
    Pilih Menu [1-11]: 6
    1. Tugus Tamvan
    2. Tugek DPS48
    Pilih Cosplayer yang akan dihapus [1-2]: 1
    Cosplayer berhasil dihapus!
    Pilih Menu [1-11]: 7
    1. Tugus Tamvan
    2. Tugek DPS48
    Pilih Cosplayer yang akan ditambahkan ke event [1-2]: 1
    Pilih Event yang akan ditambahkan cosplayer [1-2]: 1
    Cosplayer berhasil ditambahkan ke event!
    Pilih Menu [1-11]: 8
    1. Tugus Tamvan
    2. Tugek DPS48
    Pilih Cosplayer yang akan dicari dalam event [1-2]: 1
    Cosplayer ditemukan!
    Nama Cosplayer: Tugus Tamvan
    Nama Karakter: Tugus Tamvan
    Nama Anime: Tugus Tamvan
    Pilih Menu [1-11]: 9
    1. Tugus Tamvan
    2. Tugek DPS48
    Pilih Cosplayer yang akan dihapus dalam event [1-2]: 1
    Cosplayer berhasil dihapus dalam event!
    Pilih Menu [1-11]: 10
    Event yang akan diadakan dalam 7 hari mendatang adalah:
    1. Anime Festival - 2023-12-22
    2. Naruto SNK Festival - 2023-12-22
    Pilih Menu [1-11]: 11


<a id="orgeb00178"></a>

# Program Pencatatan Silsilah Keluarga

Tugek DPS48 adalah seorang mahasiswa yang sangat mencintai keluarganya. Dia sangat
menghayati filosofi keluarga yang dipegang oleh keluarganya. Dia juga sangat menghormati
leluhur keluarganya. Ia bertekad untuk mendokumentasikan silsilah keluarga dengan membuat
sebuah program yang dapat mencatat silsilah keluarga. Program ini akan mencatat data
keluarga yang terdiri dari nama dan jenis kelamin. Setiap data keluarga dapat dikaitkan
dengan data keluarga lainnya. Pengaitan ini dapat dilakukan dengan 3 jenis hubungan yaitu
ayah, ibu, dan anak. Setiap anggota keluarga setidaknya memiliki 1 orang ayah dan 1 orang 
ibu. Setiap anggota keluarga juga dapat memiliki lebih dari 1 orang anak. Fitur utama dari
aplikasi ini terdiri dari menambahkan data keluarga, mencari data keluarga, menghapus data
serta penelusuran data keluarga yang memiliki hubungan ayah, ibu, dan anak.

Adapun spesifikasi teknis yang harus dipenuhi oleh aplikasi ini adalah sebagai
berikut:

1.  Aplikasi console yang dapat dibuat dengan bahasa pemrograman Javascript
2.  Data aplikasi disimpan dalam file plain text dengan ekten .txt atau .json
3.  Aplikasi memiliki fitur menambahkan data keluarga, mencari data keluarga, dan menghapus
    data keluarga
4.  Aplikasi memiliki fitur mengaitkan data keluarga dengan data keluarga lainnya
5.  Aplikasi memiliki fitur mencari data keluarga yang memiliki hubungan ayah, ibu, dan anak

Ada pun contoh program yang diinginkan oleh Tugek adalah sebagai berikut:

    Program Pencatatan Silsilah Keluarga
    ====================================
    1. Tambah Keluarga
    2. Cari Keluarga
    3. Hapus Keluarga
    4. Kaitkan Keluarga
    5. Cari silsilah
    7. Keluar
    Pilih Menu [1-6]: 1
    Nama Keluarga: Tugus Tamvan
    Jenis Kelamin (l/p): l
    Keluarga berhasil ditambahkan!
    Pilih Menu [1-6]: 2
    Masukan nama keluarga: Tugus Tamvan
    Keluarga ditemukan!
    Nama Keluarga: Tugus Tamvan
    Jenis Kelamin: Laki-laki
    Pilih Menu [1-6]: 3
    1. Tugus Tamvan
    2. Tugek DPS48
    Pilih Keluarga yang akan dihapus [1-2]: 1
    Keluarga berhasil dihapus!
    Pilih Menu [1-6]: 4
    1. Tugus Tamvan
    2. Tugek DPS48
    Pilih Keluarga yang akan dikaitkan [1-2]: 1
    1. Tugus Tamvan
    2. Ajik Made
    3. Biang Sri Dewi Jayanti
    Pilih  yang akan dikaitkan [1-2]: 2
    Tugus Tamvan dengan merupakan [ayah/ibu/anak] dari Ajik Made: anak
    Keluarga berhasil dikaitkan!
    Pilih Menu [1-6]: 5
    1. Tugus Tamvan
    2. Tugek DPS48
    Pilih Keluarga yang akan dicari silsilahnya [1-2]: 1
    Data leluhur dari Tugus Tamvan adalah:
    Ibu: Biang Sri Dewi Jayanti
    Ayah: Ajik Made
    Kakek: Lanang Agus
    Nenenk: Ni Putu Arianti
    Kakek Buyut: Komang Sanjaya
    Nenenk Buyut: Ni Wayan Sari
    Data keturunan dari Tugus Tamvan adalah:
    Anak: Diana Putri
    Pilih Menu: [1-6]: 6
