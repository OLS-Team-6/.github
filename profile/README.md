# 💻 PENGEMBANGAN WEB SERVER DAN APLIKASI SEDERHANA

**Proyek:** [PROYEK WEB SERVER OLS]

Proyek ini dibuat untuk memenuhi tugas mata pelajaran **Administrasi Sistem Jaringan (ASJ)**, yang merupakan salah satu elemen Capaian Pembelajaran Konsentrasi Keahlian Teknik Komputer dan Jaringan (**CP KKTKJ**) pada program TJKT. Proyek ini berfokus pada implementasi layanan Web Server, konfigurasi PHP, dan pengamanan koneksi menggunakan SSL/HTTPS.

---

### 1. 👥 Informasi Kelompok dan Spesifikasi Lingkungan Praktik

#### 1.1. Informasi Kelompok

| Peran | Nama Lengkap | Kelas |
| :--- | :--- | :--- |
| **Ketua Kelompok** | [Bagus Fajri Giri Hidayat] | [XI TJKT 2] |
| Anggota 1 | [Rafi Khazin Nugraha] | [XI TJKT 2] |
| Anggota 2 | [Farish Syam Fairus] | [XI TJKT 2] |
| Anggota 3 | [Tiara Srimaya] | [XI TJKT 2] |
| **Nama Sekolah/Institusi** | [SMKN 1 SOREANG] | | [XI TJKT 2]

#### 1.2. Spesifikasi Alat dan Bahan (Host) 🛠️

| Komponen | Deskripsi / Versi |
| :--- | :--- |
| **Virtualisasi** | [Versi VMware Workstation yang Digunakan, VMware Workstation 17 Pro] |
| **Sistem Operasi Host** | [OS yang digunakan di laptop, contoh: Windows 11] |
| **RAM Host (Minimal)** | [RAM Minimal yang digunakan di Host, contoh: 8 GB] |
| **CPU Host** | [Tuliskan jenis/seri CPU, contoh: Intel Core i5 Generasi ke-10] |

#### 1.3. Spesifikasi Server Virtual (VM) 🖥️

| Spesifikasi | Detail |
| :--- | :--- |
| **Sistem Operasi Tamu (Guest OS)** | Debian Trixie (12.x) |
| **Alamat IP Server** | `[192.168.1.209]` |
| **RAM VM** | [Jumlah RAM yang dialokasikan untuk VM, contoh: 2 GB] |
| **vCPU** | [Jumlah Core CPU yang dialokasikan untuk VM, 2 Core] |
| **Web Server yang Dipilih** | **[OpenLiteSpeed]** |
| **Versi PHP yang Dipakai** | **[lsphp]** |

---

### 2. 📝 Dokumentasi Teknis dan Langkah-Langkah Pengerjaan

#### 2.1. Persiapan Dasar (Debian Trixie di VMware)

1.  Melakukan *update* dan *upgrade* sistem.
    ```bash
    Update sistem: apt update && apt upgrade
    ```
2.  Memastikan konfigurasi jaringan (Bridge/NAT/Host-Only) sudah benar.

#### 2.2. Instalasi dan Konfigurasi Web Server 🌐

Kami menggunakan **[OpenLiteSpeed]**. Berikut langkah-langkah utamanya:

* **Instalasi:**
    ```bash
    # [ Update sistem: apt install openlitespeed]
    ```
* **Konfigurasi Virtual Host/Server Block:**
    [Jelaskan secara singkat penyesuaian konfigurasi yang Kalian lakukan pada file utama, misalnya penentuan Document Root dan port.]

#### 2.3. Konfigurasi PHP 🐘

Kami menggunakan **[JENIS PHP:lsphp]** untuk mengintegrasikan PHP dengan *Web Server*.

* **Instalasi PHP:**
    ```bash
    # [ apt install lsphp84 lsphp84-mysql ]
    ```
* **Integrasi:**
    [Jelaskan langkah-langkah integrasi antara PHP dengan Web Server yang Kalian pilih.]

#### 2.4. Implementasi SSL (HTTPS) 🔒

Untuk mengaktifkan akses HTTPS, kami membuat *self-signed certificate*.

1.  Membuat direktori untuk *certificate*.
2.  Membuat *Key* dan *Certificate* menggunakan OpenSSL.
3.  Memodifikasi konfigurasi *Web Server* untuk menggunakan port **443** dan menunjuk ke *certificate* yang telah dibuat, serta memastikan akses dapat dilakukan melalui `https://192.168.1.209`.

---

### 3. 📊 Analisis Web Server

Berdasarkan pengalaman kami dalam proyek ini, berikut adalah analisis kelebihan dan kekurangan dari *Web Server* yang kami gunakan:

| Aspek | Kelebihan ([OpenLiteSpeed]) 👍 | Kekurangan ([OpenLiteSpeed]) 👎 |
| :--- | :--- | :--- |
| **Performa & Kecepatan** | [kelebihan Cepat dan ringan saat menangani banyak pengunjung. <br> - Tidak boros CPU dan RAM. <br> - Ada fitur cache bawaan yang bisa membuat website jauh lebih cepat.] | [kekurangan Kecepatannya baru maksimal kalau pengaturan cache benar. <br> - Bisa lambat kalau ada plugin atau setting yang salah.] |
| **Kemudahan Konfigurasi**| [kelebihan Ada panel admin yang mudah dipakai lewat browser. <br> - Banyak setting siap pakai untuk WordPress, Laravel, dll. <br> - Instalasinya cukup gampang.] | [kekurangan Beberapa pengaturan baru aktif setelah restart. <br> - Dokumentasi kadang kurang jelas untuk pemula. <br> - Beberapa menu konfigurasi bisa membingungkan pengguna baru.] |
| **Fitur & Modularitas** | [kelebihan Sudah mendukung HTTP/3 (lebih cepat untuk website modern). <br> - Cache bawaan sangat bagus untuk WordPress. <br> - Bisa pakai aturan .htaccess seperti di Apache.	] | [kekurangan Tidak sebanyak Nginx dalam pilihan modul. <br> - Fitur terbaik biasanya ada di versi berbayar (LiteSpeed Enterprise). <br> - Untuk aplikasi non-PHP kadang butuh setting tambahan.] |

---

### 4. 🧠 Refleksi Proyek: Kesan dan Kendala

#### 4.1. Kesan Selama Proses Pengerjaan ✨

[kesan anggota kelompok: "kami mendapakan banyak pengetahuan baru dari mulai cara membuat web server dan github sebagai sarana pembelajaran, menemukan solusi dari kegagalan dalam konfigurasi, itu adalah hal yang sangat memuaskan bagi kami."]

#### 4.2. Kendala dan Solusi yang Diterapkan 💡

| Kendala yang Kalian Hadapi 🚧 | Solusi yang Ditemukan ✅ |
| :--- | :--- |
| [kendala yang kami dapat yaitu terdapat pada device yang kami gunakan, cukup menghambat proses pengerjaan karena selalu ngeleg jika terlalu sering pindah pindah software, seperti berpindah dari vmware ke chrome lalu ke winscp] | [Jelaskan solusi spesifik Kalian.] |
solusi yang kami lakukan yaitu dengan bersabar tidak terburu buru untuk berpindah dari software yang satu ke yang lain, dengan itu kami tetap bisa mengerjakan tugas dengan sedikit lancar
---

### 5. 📂 Dokumentasi Konten Website

Seluruh *source code* (Halaman Utama dan Halaman Profil) yang berada di *document root* server telah disalin dan di-*commit* ke dalam folder `/html` di *repository* GitHub ini.

---

### 6. 🎬 Dokumentasi Video Pengerjaan

Seluruh proses pengerjaan telah direkam dan diunggah ke YouTube.

**Link Video YouTube:**

[![Thumbnail Video Pengerjaan](https://img.youtube.com/vi/TValzUfbrZg/maxresdefault.jpg)](https://youtu.be/TValzUfbrZg?si=TUwXVTdGjFV6Ks4x)


(https://img.youtube.com/vi/1-qlNtQS1OA/0.jpg)](https://www.youtube.com/watch?v=1-qlNtQS1OA)
