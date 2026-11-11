*/
Nama: Kesya Elisa Martauli Pasaribu
Nim : 41426003
Prodi : D-IV TRPL
/*

1. Cara Menjalankan 

   Disini kita buat file html dan js nya dulu kemudian  di html kita sambungkan file js  
   kemudian di file html kita klik kanan pilih "Open With Live Server"
   baru di situlah kita dapat melihat hasil codingan java script kita.


2. tahapan perubahan kode dari HTML statis menuju render berbasis state dinamis:

(Starter DOM): Membuat struktur dasar HTML menggunakan tag utama <main>, heading <h1>, 
               paragraf status (<p id=pesan>), dan daftar tak berurutan (<ul id=daftar>).


(Teks & Elemen Baru): Belajar menyisipkan elemen <li> baru lewat JavaScript menggunakan 
                      document.createElement("li")` dan mengisi teksnya menggunakan textContent.


(State & Render): Memisahkan sumber data (state) dalam bentuk array of objects (let peserta =)
                  dari tampilan DOM. Fungsi `render()` dibuat untuk membersihkan elemen lama 
                  (replaceChildren()) dan menggambar ulang elemen berdasarkan isi array.

(Keadaan Kosong / Empty State): mambahkan logika conditional menggunakan operator ternary 
                                (`peserta.length ? "" : "Belum ada peserta"`) 
                                untuk memunculkan teks informasi secara otomatis apabila data peserta kosong.

 3. Hasil Uji 

 lemen berjalan null terdiagnosa di console

 Markup sebagai Nama Mengisi textContent dengan tag HTML (<b>Rina</b>), 
 data tidak ditafsirkan sebagai markup melainkan teks biasa.

 Tag muncul secara harfiah di layar sebagai teks biasa (`<b>Rina</b>`), tidak membuat elemen <b> baru.

 Render Dua KalI Memanggil fungsi render() dua kali berturut-turut untuk memastikan tidak terjadi duplikasi data di DOM.

 Jumlah elemen `li` di DOM tetap konsisten sesuai jumlah data state (tidak berlipat ganda).

Array Kosong ([]) Menguji kondisi saat array peserta diubah menjadi kosong, pesan keadaan kosong harus tampil.

Teks Belum ada peserta tampil di elemen paragraf pesan.

4. Batasan 

*Tanpa Framework:Seluruh manipulasi DOM murni menggunakan JavaScript (Vanilla JavaScript),
                 tidak boleh memasang atau menggunakan *framework* besar seperti React, Vue, atau Angular.


* **Keamanan Teks:Karena menggunakan `textContent`, aplikasi dibatasi untuk tidak mem-parsing 
                string HTML secara langsung demi menjaga keamanan dari celah *XSS (Cross-Site Scripting)*.

1. Perbedaan textContent dan HTML parsing 
            "TEXTCONTENT"
   - TextContent Definisi: Properti JavaScript yang digunakan untuk mengatur atau mengambil teks murni, di dalam suatu elemen DOM.   
   - Contohnya di kode saya : di sini saya memasukkan string yang mengandung tag HTML seperti <b>Rina</b>, browser akan menampilkan string tersebut secara mentah di layar persis apa adanya dan tidak akan membuat elemen tag baru di DOM.

            "HTML Parsing"
    - HTML Parsing Definisi : Proses saat browser membaca, menganalisis, dan menerjemahkan string teks yang mengandung tag HTML (misalnya <b>, <i>) menjadi elemen struktur DOM yang aktif dan dirender secara visual.
    - Contohnya, tag HTML diterjemahkan oleh parser browser sehingga tag tersebut benar-benar berfungsi (contohnya membuat teks menjadi tebal secara nyata).

    "Kesimpulan Perbedaan Utamanya"
1. Cara Membaca Data
di textContent, Dianggap dan diperlakukan murni sebagai teks biasa nah sedangkan di HTML Parsing Diterjemahkan sebagai elemen atau tag markup HTML

2. Hasil di Layar
di textContent, Menampilkan tag secara langsung kaya di kode saya tuh misalnya : teks <b>Rina</b> muncul di layar. nah sedangkan di HTML Parsing Menampilkan hasil format elemen (misal: teks Rina tercetak tebal)

3. Dari Segi Keamanan nya 
di textContent, Aman dari celah serangan siber seperti XSS (Cross-Site Scripting). nah sedangkan di HTML Parsing Berisiko jika langsung merender data mentah dari input pengguna.
