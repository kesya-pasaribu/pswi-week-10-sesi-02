*/
Nama: Kesya Elisa Martauli Pasaribu
Nim : 41426003
Prodi : D-IV TRPL
/*

Penjelasan textContent :

1. TextContent hanya berisi teks, propertinya hanya berfokus pada tulisan atau teks biasa tanpa memperdulikan elemen atau tag HTML di dalam nya.

2. Mengabaikan tag html jika teks yang saya masukkan mengandung tag seperti <b> atau <i> browser tidak akan mengubahnya menjadi format tebal atau judul tetapi akan mencetak tag tersebut secara mentah sebagai teks biasa.

Cara Menjalankan :

1. Jalankan melalui live server
2. lalu klik tombol muat kegiatan ketika di klik maka yang keluar adalah data data yang saya isi di kegiatan.json
3. lalu buka devtools untuk melihat array nya

Penjelasan Perubahan :

1. Penanganan Error : Menambahkan pengecekan if (!r.ok) pada proses fetch untuk mendeteksi respons error dari server seperti status 404 secara manual ke dalam blok catch.

2. Validasi Struktur Data: Memastikan data yang diterima dari server wajib berbentuk Array menggunakan fungsi Array.isArray data.

3. Keamanan Teks (textContent): Menggunakan properti textContent saat merender data ke elemen HTML untuk menampilkan teks murni secara aman.

Hasil Uji :

1. Uji Praktikum : Data JSON yang valid berhasil dimuat dan ditampilkan pada halaman web.

2. Uji 404 file hilang : Ketika path saya ubah ke file yang tidak ada sistem mendeteksi error HTTP 404 dan menampilkan pesan "Gagal memuat"

3. Uji Bentuk Objek (Bukan Array): Saat format JSON diubah menjadi objek tunggal {} program mendeteksi bahwa data bukan Array lalu masuk ke blok catch dan menampilkan "Gagal memuat".

4. Uji Judul dengan Markup: Saat nilai judul saya isi tag HTML seperti <b>, textContent berhasil menampilkan tag tersebut secara mentah dan aman sebagai teks biasa tanpa merendernya.

Uji Batasan :

Akses Lokal : Aplikasi wajib dijalankan melalui server HTTP lokal dan tidak dapat dibuka langsung menggunakan protokol file:/// 