# Aplikasi PPDB (Penerimaan Peserta Didik Baru) Online

Aplikasi **PPDB Online** adalah sebuah platform berbasis web yang dirancang untuk memfasilitasi proses pendaftaran siswa baru di sekolah secara digital. Aplikasi ini mempermudah calon siswa dalam melakukan pendaftaran, mengunggah dokumen persyaratan, dan memantau status kelulusan, serta membantu panitia/admin sekolah dalam mengelola data pendaftar dengan lebih efisien.

---

## 🌟 Fitur Utama

Aplikasi ini dibagi menjadi dua hak akses utama: **Siswa/Pendaftar** dan **Admin**.

**Fitur untuk Siswa:**
*   **Registrasi & Login Akun:** Pendaftaran akun baru dan akses masuk yang aman.
*   **Formulir Pendaftaran:** Pengisian data diri lengkap calon siswa.
*   **Upload Dokumen:** Mengunggah berkas persyaratan (Kartu Keluarga, Ijazah, Foto, dll) ke direktori `uploads/`.
*   **Dashboard Siswa:** Memantau status pendaftaran dan pengumuman dari sekolah.
*   **Profil:** Melihat dan memperbarui data profil pendaftar.

**Fitur untuk Admin:**
*   **Dashboard Admin:** Ringkasan statistik pendaftar (jumlah pendaftar, status verifikasi).
*   **Manajemen Siswa (`students.php`):** Melihat daftar seluruh pendaftar, memverifikasi data, dan mengubah status pendaftaran (Lulus/Tidak Lulus).
*   **Manajemen Dokumen (`documents_admin.php`):** Mengecek dan mengunduh berkas yang telah diunggah oleh pendaftar.
*   **Manajemen Pengumuman (`announcements_admin.php`):** Membuat dan mempublikasikan pengumuman terkait proses PPDB.
*   **Pengaturan Sistem (`settings.php`):** Konfigurasi periode pendaftaran dan pengaturan aplikasi lainnya.

---

## 🛠️ Teknologi yang Digunakan

Aplikasi ini dibangun menggunakan arsitektur *native* dengan teknologi berikut:
*   **Bahasa Pemrograman:** PHP (Native)
*   **Database:** MySQL / MariaDB (via `mysqli` atau `PDO`)
*   **Frontend Framework:** Tailwind CSS (untuk styling modern pada beberapa komponen UI) & CSS Kustom (`style.css`).
*   **Struktur Frontend:** HTML5 & JavaScript Vanilla (`app.js`).

---

## 📋 Prasyarat Instalasi

Pastikan lingkungan server lokal (seperti XAMPP, Laragon, atau MAMP) Anda memenuhi prasyarat berikut:
*   **Web Server:** Apache atau Nginx
*   **PHP:** Versi 7.4 atau lebih baru (disarankan 8.x)
*   **Database:** MySQL atau MariaDB

---

## 🚀 Panduan Instalasi & Penggunaan

Ikuti langkah-langkah berikut untuk menjalankan project ini di komputer Anda:

1.  **Clone Repository**
    Buka terminal dan *clone* repositori ini ke dalam direktori web server Anda (misal: `htdocs` untuk XAMPP).
    ```bash
    git clone [https://github.com/username/ppdb-app.git](https://github.com/username/ppdb-app.git)
    cd ppdb-app
    ```

2.  **Konfigurasi Database**
    *   Buat database baru di phpMyAdmin (misal: `db_ppdb`).
    *   Impor file `config/database.sql` ke dalam database yang baru saja Anda buat untuk membangun struktur tabel.

3.  **Sesuaikan Koneksi Database**
    Buka file `config/database.php` dan sesuaikan detail koneksi database (username, password, dan nama database) dengan pengaturan server lokal Anda.

4.  **Uji Koneksi**
    Anda dapat membuka file `test_db.php` di browser (`http://localhost/ppdb-app/test_db.php`) untuk memastikan bahwa aplikasi sudah berhasil terhubung ke database.

5.  **Jalankan Aplikasi**
    Buka browser dan akses URL utama aplikasi:
    ```
    http://localhost/ppdb-app/index.php
    ```

---

## 📂 Susunan Project

Berikut adalah struktur file dan folder utama dalam aplikasi ini:
```text
ppdb-app/
├── assets/                 # Aset frontend (CSS, Gambar, JavaScript)
│   ├── css/style.css
│   ├── img/
│   └── js/app.js
├── config/                 # Konfigurasi sistem
│   ├── database.php        # Konfigurasi koneksi database
│   └── database.sql        # File dump SQL untuk struktur tabel
├── lib/                    # Kumpulan fungsi PHP pembantu (Helper)
│   └── functions.php
├── templates/              # Komponen UI yang dapat digunakan kembali (Header, Footer, Sidebar)
│   └── partials/
├── uploads/                # Direktori penyimpanan file yang diunggah oleh siswa
├── index.php               # Halaman utama (Landing Page)
├── login.php               # Halaman Login
├── register.php            # Halaman Pendaftaran Akun
├── dashboard_siswa.php     # Halaman Dashboard khusus Siswa
├── dashboard_admin.php     # Halaman Dashboard khusus Admin
├── alur_pendaftaran.php    # Halaman informasi alur
└── ...                     # File PHP operasional lainnya
```
MIT License

Copyright (c) 2026

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

