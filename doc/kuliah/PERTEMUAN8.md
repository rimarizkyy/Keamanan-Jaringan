**SNORT**

<p align="center">
  <img src="../../img/8.JPG" width="400px">
</p>

LATAR BELAKANG

Berikut akan dijelaskan mengenai software Snort. Apa saja yang akan dibahas? Antara lain definisi Snort, fitur – fitur dalam Snort, dan cara penginstall-an Snort dalam CentOS.

PEMBAHASAN

Definisi Snort

Snort adalah sebuah software atau aplikasi yang bersifat opensource. Snort berguna sebagai NIDS yaitu Network Intrusion Detection System yang ringan dan menggunakan rules system yang termasuk mudah untuk dipelajari.

Snort sendiri dikembangkan oleh Marty Roesch yang dikembangkan awal tahun 1998 sebagai sniffer dengan konsistensi outputnya. Snort masih berbasis command-line. Snort juga masih GNU atau General Public License maka dari itu Snort masuh bisa digunakan secara gratis.

Fitur – Fitur Snort

- --Penggunaan Snort yang bebas menjadikan Snort bisa dipergunakan secara gratis. Snort jugapilihan terbaik untuk NIDS yang lainnya.
- --Penggunaan yang sangat bebas menjadikan Snort dapat digunakan di lingkungan mana saja.
- --Snort mempunyai bahasa dalam rules yang relative mudah sehingga mudah dan fleksibel untuk dipelajari.
- --Di dalam snort sendiri sudah terdapat database yangs ecara aktif dapat terus dikembangkan jika ada tipe – tipe serangan baru.
- --Snort sendiri tidak memerlukan banyak resources, tetapi cukup fleksibel dan canggih.
- --Snort juga dapat melakukan logging ke sistem database seperti S SQL, MySQL, dll.
- --Sebagai NIDS, snort tidak terlihat di jaringan komputer, yang disebut dengan Stealth Mode.

Cara Install Snort dalam CentOS

- -- **Instalasi dengan yum**
Snort memberikan paket rpm nyaman untuk CentOS 7, yang dapat diinstal hanya dengan perintah di bawah ini. Snort sendiri menggunakan sesuatu yang disebut Data Acquisition perpustakaan (DAQ) untuk melakukan panggilan abstrak untuk packet capture perpustakaan. Periksa nomor versi terbaru dari website Snort, jika versi yang lebih baru dari DAQ atau Snort tersedia cukup mengganti nomor versi di perintah berikut dengan opsi terbaru.

- -- **Instalasi dari Source**
Menyiapkan Snort dari kode sumber terdiri dari beberapa langkah: download kode, mengkonfigurasi, kompilasi kode dan terakhir menginstal itu. Pertama membuat folder download sementara untuk direktori home Anda dan kemudian bergerak ke dalamnya dengan perintah ini

_mkdir ~/snort\_src_
_cd ~/snort\_src_

Download paket terbaru sumber DAQ dari website Snort dengan perintah wget bawah, ganti nomor versi jika ada sumber yang lebih baru yang tersedia

_wget https://www.snort.org/downloads/snort/daq-2.0.6.tar.gz_

Download hanya akan memakan waktu beberapa detik, ekstrak setelah selesai kode sumber dan melompat ke dalam direktori baru dengan perintah berikut

_tar -xvzf daq-2.0.6.tar.gz_
_cd daq-2.0.6_

Jalankan script konfigurasi dengan default, kemudian gunakan membuat untuk mengkompilasi program dan kemudian akhirnya memasang DAQ

_./configure_
_make_
_sudo make install_

Dengan DAQ yang diinstal Anda bisa memulai dengan Snort, mengubah kembali ke folder download

_cd ~/snort\_src_

Kemudian download kode sumber Snort dengan wget, memeriksa nomor versi terbaru dari situs Snort dan menggantinya di perintah berikut jika diperlukan.

_wget https://www.snort.org/downloads/snort/snort-2.9.8.0.tar.gz_

Setelah download selesai, ekstrak sumber dan mengubah ke dalam direktori baru dengan perintah ini

_tar -xvzf snort-2.9.8.0.tar.gz_
_cd snort-2.9.8.0_

Kemudian mengkonfigurasi instalasi dengan modus Sourcefire diaktifkan, jalankan make dan make install.

._/configure --enable-sourcefire_
_make_
_sudo make install_

PENUTUP

1. Kesimpulan : Snort merupakan aplikasi opensource yang sangat ringan dan gratis dan menyediakan fitur – fitur yang cukup fleksibel dan sangat menguntungkan bagi banyak user.
2. Saran : disarankan agar mencari referensi lain dari luar blog ini yang lebih lengkap.
