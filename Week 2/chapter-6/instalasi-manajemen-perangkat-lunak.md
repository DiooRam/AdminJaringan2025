<div align="center">
  <h1 style="text-align: center;font-weight: bold">Laporan Week 2<br>ADMINISTRASI JARINGAN</h1>
</div>
<br />
<div align="center">
  <img src="https://upload.wikimedia.org/wikipedia/id/4/44/Logo_PENS.png" alt="Logo PENS">
  <h4 style="text-align: center;">Dosen Pengampu : Dr. Ferry Astika Saputra, S.T., M.Sc.</h4>
  <h3 style="text-align: center;">Disusun Oleh : </h3>
  <p style="text-align: center;">
    <strong>Nama : Dio Ramadhan Widya Pamungkas</strong><br>
    <strong>Kelas : 2 D3 IT A</strong><br>
    <strong>NRP : 3123500011</strong>
  </p>

<h3 style="text-align: center;line-height: 1.5">Politeknik Elektronika Negeri Surabaya<br>Departemen Teknik Informatika Dan Komputer<br>Program Studi Teknik Informatika<br>2024/2025</h3>
  <hr><hr>
</div>

# **Chapter 6 Instalasi dan Manajemen Perangkat Lunak**

### Instalasi Sistem Operasi

Distribusi Linux dan FreeBSD memiliki prosedur instalasi dasar yang cukup sederhana.

- **Instalasi Fisik vs. Virtual:**
    Jika menggunakan perangkat fisik, sistem bisa di-boot melalui CD, DVD, atau USB. Sementara itu, pada mesin virtual, booting dilakukan menggunakan file ISO. Instalasi dari media lokal menjadi lebih sederhana berkat antarmuka grafis yang memandu pengguna selama proses berlangsung.
    
- **Instalasi Melalui Jaringan:**
    
Untuk instalasi di banyak perangkat, metode tradisional menggunakan CD/DVD/USB bisa kurang praktis karena memakan waktu dan rentan terhadap kesalahan. Alternatif yang lebih efisien adalah instalasi melalui jaringan.
Proses ini biasanya menggunakan protokol seperti DHCP dan TFTP, memungkinkan sistem untuk mengunduh file instalasi langsung dari server melalui HTTP, FTP, atau NFS. Salah satu metode populer adalah PXE (Preboot eXecution Environment), yang memungkinkan perangkat booting langsung dari jaringan tanpa memerlukan media fisik.

Sistem Manajemen Paket di Linux
Format Paket:

Linux memiliki beberapa format paket, tetapi yang paling umum adalah:

RPM – Digunakan oleh distribusi seperti Red Hat, CentOS, SUSE, dan Amazon Linux.
DEB – Digunakan oleh sistem berbasis Debian seperti Ubuntu.
Kedua format ini berfungsi serupa dalam mengelola perangkat lunak pada sistem.

Alat Manajemen Paket Dasar:

Setiap sistem memiliki alat bawaan untuk menangani paket perangkat lunak, seperti:

rpm untuk paket berbasis RPM.
dpkg untuk paket berbasis .deb.
Manajemen Paket Tingkat Lanjut
Alat manajemen paket tingkat lanjut mempermudah instalasi, pembaruan, dan penghapusan perangkat lunak. Selain itu, mereka juga memungkinkan pencarian paket serta melihat daftar perangkat lunak yang telah terinstal.

Repositori Paket:

Alat manajemen paket tingkat lanjut mempermudah instalasi, pembaruan, dan penghapusan perangkat lunak. Selain itu, mereka juga memungkinkan pencarian paket serta melihat daftar perangkat lunak yang telah terinstal.

Release – Kumpulan paket dalam satu versi stabil.
Component – Subset perangkat lunak dalam suatu release.
Architecture – Jenis perangkat keras yang didukung, misalnya i386 untuk Fedora.
yum (Yellowdog Updater, Modified):

Alat ini digunakan pada sistem berbasis RPM untuk menangani instalasi, pembaruan, dan penghapusan paket dengan otomatis menyelesaikan dependensi.

APT (Advanced Package Tool):

APT digunakan dalam sistem berbasis Debian untuk mengelola paket perangkat lunak dengan lebih efisien. Beberapa perintah yang umum digunakan:

apt-get – Menginstal, menghapus, dan memperbarui paket.
apt-cache – Mencari informasi dalam cache paket.
apt-file – Menelusuri file dalam paket.
apt-show-versions – Menampilkan versi paket yang telah terinstal.
aptitude – Alat yang lebih canggih dibandingkan apt-get dengan fitur tambahan.
apt-mirror – Digunakan untuk membuat salinan repositori.
APT adalah salah satu sistem manajemen paket paling populer di Linux berbasis Debian, dapat menangani paket DEB maupun RPM.

Lokalisasi dan Konfigurasi Sistem
Menyesuaikan sistem agar sesuai dengan kebutuhan lokal atau lingkungan berbasis cloud adalah bagian penting dari administrasi jaringan. Menggunakan pendekatan yang terstruktur dan dapat direplikasi membantu memastikan sistem tetap mudah dipelihara serta dapat dipulihkan dengan cepat jika terjadi masalah.

Keseluruhan pembahasan ini bertujuan untuk memberikan pemahaman dasar mengenai cara menginstal sistem operasi serta mengelola perangkat lunak secara efisien, terutama dalam lingkungan yang membutuhkan otomatisasi dan skalabilitas tinggi.









    

### Sistem Manajemen Paket Linux

- **Format Paket:**
    
    Linux menggunakan berbagai format paket, dengan dua yang paling umum adalah:
    
    - **RPM:** Digunakan oleh distribusi seperti Red Hat, CentOS, SUSE, dan Amazon Linux.
    - **.deb:** Digunakan oleh sistem berbasis Debian seperti Ubuntu.
    
    Kedua format ini memiliki fungsi yang hampir serupa.
    
- **Alat Manajemen Paket Dasar:**
    
    Setiap sistem memiliki alat bawaan untuk mengelola paket:
    
    - **rpm** untuk paket RPM.
    - **dpkg** untuk paket .deb.

### Manajemen Paket Tingkat Tinggi

Alat manajemen paket tingkat tinggi memungkinkan instalasi, penghapusan, dan pembaruan paket dengan lebih mudah. Selain itu, alat ini juga memungkinkan pencarian paket serta melihat daftar paket yang sudah terinstal.

- **Repositori Paket:**
    
    Konfigurasi default sistem manajemen paket umumnya terhubung ke satu atau beberapa server yang dikelola oleh distributor.
    
    - *Release* merupakan snapshot konsisten dari semua paket.
    - *Component* adalah subset perangkat lunak dalam sebuah release.
    - *Architecture* mengacu pada jenis perangkat keras yang kompatibel dengan binary paket, seperti i386 untuk Fedora 20.
- **yum (Yellowdog Updater, Modified):**
    
    Manajer paket berbasis RPM ini menangani resolusi dependensi saat menginstal, memperbarui, dan menghapus paket. yum dapat mengelola paket dari repositori yang sudah terdaftar serta menjalankan operasi baris perintah untuk paket tertentu.
    
- **APT (Advanced Package Tool):**
    
    APT adalah kumpulan alat yang menyediakan sistem manajemen paket lengkap untuk sistem berbasis Debian (.deb). Beberapa alat dalam APT meliputi:
    
    - **apt-get:** Mengelola instalasi, penghapusan, dan pembaruan paket.
    - **apt-cache:** Mencari dan menampilkan informasi dari cache paket APT.
    - **apt-file:** Mencari file di dalam paket.
    - **apt-show-versions:** Menampilkan versi paket yang terinstal.
    - **aptitude:** Antarmuka tingkat tinggi untuk manajemen paket, dengan fungsionalitas tambahan dibandingkan apt-get.
    - **apt-mirror:** Menyediakan fitur pencerminan repositori paket.
    
    APT merupakan sistem yang paling banyak digunakan pada distribusi berbasis Debian dan dapat menangani paket .deb maupun RPM.
    

### Lokalisasi dan Konfigurasi Perangkat Lunak

Menyesuaikan sistem agar sesuai dengan lingkungan kerja lokal atau berbasis cloud adalah bagian penting dari administrasi sistem. Pendekatan yang terstruktur dan dapat direproduksi sangat penting untuk menghindari sistem unik yang sulit dipulihkan jika terjadi masalah besar.

Keseluruhan pembahasan ini bertujuan untuk memberikan pemahaman praktis tentang cara menginstal sistem operasi serta mengelola paket perangkat lunak secara efisien, terutama dalam lingkungan yang membutuhkan otomatisasi dan skalabilitas.
