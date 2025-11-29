
💻 LAPORAN PROYEK: PENGEMBANGAN WEB SERVER DAN APLIKASI SEDERHANA
Proyek: [WEB SERVER OLS]

Proyek ini dibuat untuk memenuhi tugas mata pelajaran Administrasi Sistem Jaringan (ASJ) , yang merupakan salah satu elemen Capaian Pembelajaran Konsentrasi Keahlian Teknik Komputer dan Jaringan ( CP KKTKJ ) pada program TJKT. Proyek ini fokus pada implementasi layanan Web Server, konfigurasi PHP, dan pengamanan koneksi menggunakan SSL/HTTPS.

1. 👥 Informasi Kelompok dan Spesifikasi Lingkungan Praktik
1.1. Informasi Kelompok
Peran	Nama Lengkap	Kelas
Ketua Kelompok	[Bagus Fajri Giri Hidayat]	[XI TJKT 2]
Anggota 1	[Rafi Khazin Nugraha]	[XI TJKT 2]
Anggota 2	[Faris Syam Fairus]	[XI TJKT 2]
Anggota 3	[Tiara Sri Maya]	[XI TJKT 2]
Nama Sekolah/Institusi	[SMKN 1 SOREANG ]	
1.2. Spesifikasi Alat dan Bahan (Host) 🛠️
Komponen	Deskripsi / Versi
Virtualisasi	[Versi VMware Workstation yang Digunakan, contoh: VMware Workstation 17 Pro]
Sistem Operasi Host	[OS yang digunakan di laptop/PC utama, contoh: Windows 11 / macOS Sonoma]
RAM Host (Minimal)	[RAM Minimal yang digunakan di Host, contoh: 8 GB]
Host CPU	[Tuliskan jenis/seri CPU, contoh: Intel Core i5 Generasi ke-10]
1.3. Spesifikasi Server Virtual (VM) 🖥️
Spesifikasi	Detil
Sistem Operasi Tamu (OS Tamu)	Debian Trixie (12.x)
Alamat IP Server	[Tuliskan Alamat IP Lokal Server]
Mesin Virtual RAM	[Jumlah RAM yang dikhususkan untuk VM, contoh: 2 GB]
vCPU	[Jumlah Core CPU yang dikhususkan untuk VM, contoh: 2 Core]
Web Server yang Dipilih	[Apache2 / Nginx / OpenLiteSpeed]
Versi PHP yang Dipakai	[mod_php / php-fpm / lsphp]
3. 📝 Dokumentasi Teknis dan Langkah-Langkah Pengerjaan
2.1. Persiapan Dasar (Debian Trixie di VMware)
Melakukan update dan upgrade sistem.
sudo apt update && sudo apt upgrade -y
Konversi konfigurasi jaringan (Bridge/NAT/Host-Only) sudah benar.
2.2. Instalasi dan Konfigurasi Web Server 🌐
Kami menggunakan [NAMA WEB SERVER] . Berikut langkah-langkah utamanya:

Instalasi:
# [Tuliskan perintah instalasi Web Server Kalian, contoh: sudo apt install nginx -y]
Konfigurasi Virtual Host/Server Block: [Jelaskan secara singkat penyesuaian konfigurasi yang Kalian lakukan pada file utama, misalnya penentuan Document Root dan port.]
2.3. Konfigurasi PHP 🐘
Kami menggunakan [JENIS PHP: mod_php / php-fpm / lsphp] untuk mengintegrasikan PHP dengan Web Server .

Instalasi PHP:
# [Tuliskan perintah instalasi PHP dan modul yang dibutuhkan]
sudo apt install php-fpm php-mysql
Integrasi: [Jelaskan langkah-langkah integrasi antara PHP dengan Web Server yang Kalian pilih.]
2.4. Implementasi SSL (HTTPS) 🔒
Untuk mengaktifkan akses HTTPS, kami membuat sertifikat yang ditandatangani sendiri .

Membuat direktori untuk sertifikat .
Membuat Kunci dan Sertifikat menggunakan OpenSSL.
Memodifikasi konfigurasi Web Server untuk menggunakan port 443 dan menunjuk ke sertifikat yang telah dibuat, serta memastikan akses dapat dilakukan melalui https://[IP_SERVER].
3. 📊 Analisis Web Server
Berdasarkan pengalaman kami dalam proyek ini, berikut adalah analisis kelebihan dan kekurangan dari Web Server yang kami gunakan:

Aspek	Kelebihan ([NAMA WEB SERVER]) 👍	Kekurangan ([NAMA WEB SERVER]) 👎
Performa & Kecepatan	[Tuliskan kelebihannya.]	[Tuliskan kekurangannya.]
Kemudahan Konfigurasi	[Tuliskan kelebihannya.]	[Tuliskan kekurangannya.]
Fitur & Modularitas	[Tuliskan kelebihannya.]	[Tuliskan kekurangannya.]
4. 🧠 Re Proyekfleksi: Kesan dan Kendala
4.1. Kesan Selama Proses Pengerjaan ✨
[Tuliskan kesan anggota kelompok, misalnya: "Kami merasa mendapatkan banyak ilmu baru, terutama dalam praktik Version Control menggunakan Git dan GitHub yang belum pernah kami lakukan sebelumnya."]

4.2. Kendala dan Solusi yang Diterapkan 💡
Kendala yang Kalian Hadapi 🚧	Solusi yang Ditemukan ✅
[Tuliskan kendala teknis atau kolaborasi lain yang Kalian hadapi.]	[Jelaskan solusi spesifik Kalian.]
5. 📂 Website Dokumentasi Konten
Seluruh kode sumber (Halaman Utama dan Halaman Profil) yang berada di server root dokumen telah diverifikasi dan di- commit ke dalam folder /htmldi repositori GitHub ini.

6. 🎬 Dokumentasi Video Pengerjaan
Seluruh proses pengerjaan telah direkam dan diunggah ke YouTube.

Tautan Video YouTube:

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
