# UAS-STKI

UAS STKI </br>
Rabu, 14 Desember 2022 </br>
Rokhana Diyah Rusdiati (21/486134/PPA/06236) </br>

**Jawaban Nomor 1** </br>
Metode kueri pencarian dan similarity search pada proyek pengembangan STBI di Kelompok 4 “Aksara Jawa” adalah dengan menggunakan _brute force string matching_, yaitu algoritma pencocokan _string_ secara _straight forward_. Pencarian pola dilakukan secara satu per satu dalam suatu teks dari kiri atau kanan sampai akhir dari string tersebut. Apabila terdapat salah satu karakter dari pola yang tidak sesuai dengan teks, maka pencarian ulang akan dilakukan dari awal pola yang ada. Pada proyek STBI Kelompok 4 “Aksara Jawa”, _query_ merupakan nama huruf aksara Jawa yang ditulis dengan alfabet roman, misalnya “ha”, “na”, “ca”, dll. Dataset dalam proyek ini telah dilabeli terlebih dahulu sesuai dengan cara baca aksara Jawa dalam bentuk dasar. Label tersebut akan dicocokkan dengan _query_ untuk mengeluarkan _output_ berupa huruf aksara Jawa dalam bentuk huruf dasar, kata, maupun kalimat.
</br>
**Jawaban Nomor 2** </br>
Metode evaluasi yang digunakan untuk mengevaluasi prototype STBI Kelompok 4 “Aksara Jawa” adalah dengan menghitung waktu pencarian dan hasil pencarian dengan status “ditemukan”. Rata-rata keseluruhan waktu pencarian dalam proyek ini yaitu 0.59 detik, pencarian tercepat yaitu pada percobaan ke-1 dengan dataset huruf dasar aksara Jawa, sedangkan pencarian terlama yaitu pada percobaan ke-3 dengan dataset gabungan antara huruf dasar aksara Jawa serta contoh penggunaannya dalam bentuk kata dan kalimat. Sementara itu, hasil evaluasi menunjukkan bahwa sistem dalam proyek ini adalah 100% akurat dengan menggunakan berbagai macam bentuk _query_ aksara Jawa dalam bentuk dasar yang terdiri dari kombinasi _upper case_ maupun _lower case_. Misal _query_ = “hA”, maka sistem akan mengeluarkan _output_ untuk semua data gambar yang memiliki label “ha”.
</br>
**Jawaban Nomor 3** </br>
Perbedaan antara sistem rekomendasi dan sistem tanya jawab adalah sebagai berikut. </br>
a. Sistem rekomendasi merupakan suatu sistem yang digunakan oleh _user_ untuk mendapatkan produk yang diinginkan, yaitu dengan berdasarkan beberapa sumber informasi yang ada sehingga dapat meningkatkan penjualan produk. </br>
b. Sistem tanya jawab merupakan sistem yang digunakan untuk menjawab pertanyaan berdasarkan koleksi dokumen yang tidak terstruktur dalam bahasa alami, yaitu dengan melakukan pencarian _query_ sebagai pertanyaan sehingga bisa menghasilkan _output_ berupa jawaban yang sesuai. </br> </br>

Dengan demikian, proyek STBI Kelompok 4 “Aksara Jawa” termasuk ke dalam kategori sistem tanya jawab. Hal ini disebabkan karena sistem bekerja dengan cara menerima _input_ berupa _query_ yang akan melalui _text preprocessing_ terlebih dahulu, kemudian dilakukan proses _string matching_ dengan _label_ yang ada pada dataset. _Output_ yang dikeluarkan yaitu berupa gambar dengan _label_ yang sama seperti pada _query_.

**Jawaban Nomor 4** Tentang proyek STBI Kelompok 4 “Aksara Jawa” </br>
a. Rangkuman proyek STBI </br>
**Introduction**: Indonesia memiliki beragam bahasa daerah, salah satunya yaitu bahasa Jawa yang memiliki huruf khusus bernama aksara Jawa. De Casparis menyebutkan bahwa aksara Jawa merupakan perkembangan dari aksara Kawi yang digunakan oleh masyarakat Jawa sejak pertengahan abad ke-15 sampai pertengahan abad ke-20 [1]. Seiring berjalannya waktu, aksara Jawa tergantikan keberadaannya dengan aksara Latin yang umum digunakan sampai saat ini. Untuk melestarikan peninggalan budaya daerah, para siswa dari tingkat sekolah dasar perlu mempelajari penggunaan aksara Jawa. Ekowati menyebutkan bahwa minat belajar bahasa Jawa pada anak semakin rendah karena aksara Jawa sudah jarang digunakan pada kegiatan sehari-hari [2]. Hal ini menyebabkan kurangnya motivasi pada anak untuk belajar aksara Jawa. Selain itu, media pembelajaran aksara Jawa yang monoton dan kurang interaktif membuat para siswa menjadi semakin tidak tertarik untuk mempelajari aksara Jawa. Oleh sebab itu, diperlukan adanya inovasi baru yang bisa membantu meningkatkan minat belajar aksara Jawa pada anak. Pada penelitian ini akan dikembangkan sistem temu kembali informasi yang akan mengeluarkan output berupa huruf aksara Jawa dengan memanfaatkan metode brute force dalam pencocokan string query. Pengguna cukup memasukkan satu huruf aksara Jawa dalam bentuk latin saja untuk mendapatkan berbagai contoh penulisan huruf dalam aksara Jawa.</br>
**Metode**: Secara umum, proses yang dilakukan dalam penelitian ini digambarkan sebagai berikut. Setiap aksara Jawa dan contoh penggunaannya akan disimpan dalam bentuk gambar berekstensi JPG. Masing-masing gambar tersebut akan diberi label secara manual sesuai dengan cara baca dari masing-masing aksara Jawa. Sistem akan menerima query berupa huruf latin dari aksara Jawa. Selanjutnya akan dilakukan prapemrosesan _query_ oleh sistem, lalu _query_ akan dibandingkan dengan label gambar aksara Jawa menggunakan _brute force string matching_. _Brute force string matching_ adalah algoritma pencocokan _string_ secara _straight forward_, yaitu pencarian pola dilakukan secara satu per satu dalam suatu teks dari kiri atau kanan sampai akhir dari _string_ tersebut. Apabila terdapat salah satu karakter dari pola yang tidak sesuai dengan teks, maka pencarian ulang akan dilakukan dari awal pola yang ada [11]. Misalkan terdapat string x yang memiliki panjang karakter m, akan dicocokkan dengan teks y yang memiliki panjang karakter n. Proses pencocokan string dimulai dengan menempatkan window string dari 0 sampai m pada awal teks. Kemudian, karakter pada window akan dibandingkan dengan karakter pada teks dari arah kiri ke kanan dengan pergeseran sebanyak 1 karakter string sampai window sesuai dengan teks atau window berada pada akhir teks [9]. Query pada penelitian ini bertindak sebagai string sedangkan teks yang akan dibandingkan adalah cara baca aksara Jawa. _Output_ dari sistem ini adalah gambar aksara Jawa yang sesuai dengan _query_. </br>
**Hasil**: Waktu pencarian dicatat untuk mengetahui waktu yang dibutuhkan untuk proses pencarian setiap query aksara sampai menampilkan hasil yang sesuai. Eksperimen dilakukan dalam tiga percobaan yang berbeda berdasarkan variasi dataset. Percobaan ke-1 menggunakan dataset yang terdiri dari 20 aksara dasar, percobaan ke-2 menggunakan dataset yang terdiri dari 36 data yaitu gabungan 20 aksara dasar dan 16 kata, serta percobaan ke-3 menggunakan dataset yang terdiri dari 51 data yaitu gabungan 20 aksara dasar, 16 kata, dan 15 kalimat. Pada percobaan ke-1, rata-rata waktu pencarian untuk 20 aksara dasar adalah 0.1403924584 detik. Pencarian tercepat yaitu pada aksara ‘da’ dengan waktu selama 0.09719347954 detik. Sedangkan pencarian terlama yaitu pada aksara ‘ka’ dengan waktu selama 0.2369954586 detik. Pada percobaan ini masing-masing aksara terdiri dari 1 data saja. Pada percobaan ke-2, rata-rata waktu pencarian untuk 36 data adalah 0.4636428356 detik. Pencarian tercepat yaitu pada aksara ‘tha’ dengan waktu selama 0.2907538414 detik. Aksara ‘tha’ terdiri dari 3 data, oleh sebab itu memiliki waktu pencarian tercepat. Sedangkan pencarian terlama yaitu pada aksara ‘na’ dengan waktu selama 1.138965368 detik. Aksara ‘na’ terdiri dari 7 data, sehingga memiliki waktu pencarian terlama. Pada percobaan ke-3, rata-rata waktu pencarian untuk 51 data adalah 1.179515135 detik. Pencarian tercepat yaitu pada aksara ‘tha’ dengan waktu selama 0.4946451187 detik. Aksara ‘tha’ terdiri dari 3 data, oleh sebab itu memiliki waktu pencarian tercepat. Sedangkan pencarian terlama yaitu pada aksara ‘na’ dengan waktu selama 2.608828068 detik. Aksara ‘na’ terdiri dari 16 data sehingga memiliki waktu pencarian terlama. Contoh hasil pencarian untuk query ‘ca’ = ca, cacah, cetha, sampun dhahar acar; sistem menampilkan gambar aksara Jawa dari semua hasil pencarian tersebut.</br>
**Pembahasan**: Berdasarkan percobaan yang dilakukan, prapemrosesan berupa lowercase diketahui tidak begitu mempengaruhi kecepatan proses pencarian karena berbagai bentuk variasi input yang telah dicoba memberikan hasil waktu pencarian yang cepat dengan perbedaan waktu di bawah 0.1 detik. Sistem ini memberikan hasil pencarian yang bersifat exactly match, karena hasil yang ditampilkan adalah selalu sesuai dengan query dan dataset yang ada. Sistem sudah mampu menghasilkan output yang sesuai dengan query dengan rata-rata running time 0.59451681 detik pada semua percobaan. Pencarian tercepat yaitu pada aksara dasar ‘da’ pada percobaan ke-1, sedangkan pencarian terlama yaitu aksara ‘na’ pada percobaan ke-3. Waktu pencarian berbanding lurus dengan jumlah data yang ada. Semakin banyak jumlah data yang dimiliki, maka waktu pencarian yang dibutuhkan semakin lama. </br>
**Referensi**: </br>
[1]	Casparis, J..G.. de, 1975, Indonesian Palaeography: A History of Writing in Indonesia from the Beginnings to C A.D. 1500. Leiden/Koln: Brill. Handbuch der Orientalistik. Dritte Abteilung. Vierter Band, erste Lieferung </br>
[2]	Ekowati, Venny Indria, 2007, Perubahan Sistem Pembelajaran Aksara Jawa, Anjasmara UNY, Yogyakarta </br>
[3]	Danuri, D. (2016). Pencarian File Teks Berbasis Content dengan Pencocokan String Menggunakan Algoritma Brute force. Scientific Journal of Informatics, 3(1), 68-75. doi:https://doi.org/10.15294/sji.v3i1.6515</br>
[4]	Amin, F., & Nurraharjo, E. (2017). REKAYASA SISTEM TEMU KEMBALI INFORMASI DOKUMEN TEKS BERBAHASA JAWA METODE COSINE SIMILARITY DAN RULE BASE STEMMING BAHASA JAWA. SINTAK, 1. Retrieved from https://unisbank.ac.id/ojs/index.php/sintak/article/view/5499 </br>
[5]	Aribowo, Eric. (2018). Digitalisasi Aksara Jawa dan Pemanfaatannya sebagai Media Pembelajaran bagi Musyawarah Guru Mata Pelajaran Bahasa Jawa SMP Kabupaten Klaten. Warta LPM. 21. 10.23917/warta.v21i2.5620 </br>
[6]	Roffiq, A., Qiram, I., & Rubiono, G. (2017a). Implementasi Algoritma Brute Force Dalam Pencocokan String Pada Aplikasi Pencarian Musik. JPDI (Jurnal Pendidikan Dasar Indonesia), 2(2), 35. https://doi.org/10.26737/jpdi.v2i2.330 </br>
[7]	Fandi Nainggolan, G. H., Andryana, S., Aris Gunaryati, dan, Teknologi Komunikasi dan Informatika, F., Nasional Ps Minggu, U., Jakarta Selatan, K., & Khusus Ibukota Jakarta, D. (n.d.). PENCARIAN BERITA PADA WEB PORTAL MENGGUNAKAN ALGORITMA BRUTE FORCE STRING MATCHING.</br>
[8]	Irawan, C., & Pratama, M. R. (2020). Perbandingan Algoritma Boyer-Moore dan Brute Force pada Pencarian Kamus Besar Bahasa Indonesia Berbasis Android. BIOS: Jurnal Teknologi Informasi dan Rekayasa Komputer, 1(2), 54-60.</br>
[9]	Mukaromah, I. A., Jamil, A., Saputro, M. W., Farikha, N., Studi, P., Informatika, T., Muhammadiyah, S., Brebes, P., & Informasi, S. (2021). ANALISIS PENCOCOKAN STRING MENGGUNAKAN ALGORITMA BRUTE FORCE. In Jurnal Teknik Informatika dan Sistem Informasi (JURTISI) (Vol. 1, Issue 1).</br>
[10]	Azis, M. R., Fitri, I., & Rahman, B. (2021). PENGGUNAAN ALGORITMA BRUTE FORCE STRING MATCHING DALAM PENCARIAN ORANG HILANG PADA WEBSITE TEMUKANDIA. COM. JIPI (Jurnal Ilmiah Penelitian dan Pembelajaran Informatika), 6(2), 205-212.</br>
[11]	Setiawan, C. B. (2018). Penerapan dan Perbandingan Algoritma String Matching pada Aplikasi UUD 1945 dan UU di Indonesia
</br></br>
Proyek STBI Kelompok 4 yaitu “Aksara Jawa” merupakan _multimedia information retrieval system_ karena sistem ini melakukan ekstraksi informasi semantik dari sumber data multimedia dalam bentuk gambar, yaitu berupa _label_.
</br>
Rangkuman dalam bentuk paper dapat dilihat di: https://docs.google.com/document/d/1tmFKtXr9QkoUrM6n0OSlNiRQ5zSodkGjRUMTac4Co5c/edit#heading=h.exgrom2ge51o
