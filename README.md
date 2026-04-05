# ⚙️ Backend API - Sarana Pengaduan Sekolah

Ini adalah *repository* untuk bagian *backend* dari sistem Sarana Pengaduan Sekolah. Backend ini dibangun menggunakan **Strapi (Headless CMS)** dan menggunakan **MySQL** sebagai *database* utamanya. 

Backend ini bertugas untuk menyediakan REST API yang akan dikonsumsi oleh aplikasi *frontend* React, serta menyediakan panel admin yang mudah digunakan untuk mengelola data pengaduan.

## 🚀 Teknologi yang Digunakan

* **Framework/CMS:** Strapi
* **Database:** MySQL
* **Environment:** Node.js

## 🗂️ Struktur Data (Collection Types)

Sistem ini memiliki beberapa *Collection Types* utama yang sudah dikonfigurasi:
* **Pengaduan:** Menyimpan data laporan dari siswa (lokasi, keterangan, kategori, foto bukti, status).
* **Siswa:** Data profil siswa (NIS, Nama, Kelas, dll).
* **Kategori:** Jenis-jenis kategori pengaduan.
* **User & Roles:** Sistem autentikasi untuk membedakan akses antara akun **Siswa** dan **Admin Sekolah**.

## 🛠️ Cara Menjalankan Project Secara Lokal

Ikuti panduan ini agar project dapat berjalan dengan lancar menggunakan *database* MySQL di komputermu.

### 1. Persyaratan Sistem
Pastikan kamu sudah menginstal perangkat lunak berikut:
* [Node.js](https://nodejs.org/) (Versi 18 atau lebih baru disarankan)
* MySQL Server (Bisa menggunakan [XAMPP](https://www.apachefriends.org/) atau sejenisnya)
* Git

### 2. Persiapan Database
1. Buka MySQL kamu (misal: aktifkan MySQL di XAMPP).
2. Buka phpMyAdmin (atau *database client* lain).
3. Buat *database* baru yang kosong. Ingat nama *database* tersebut (contoh: `db_pengaduan_sekolah`).

### 3. Instalasi dan Konfigurasi

1.  **Clone repository ini:**
    ```bash
    git clone [https://github.com/username-kamu/nama-repo-backend-kamu.git](https://github.com/username-kamu/nama-repo-backend-kamu.git)
    cd nama-repo-backend-kamu
    ```
    *(Jangan lupa ganti link di atas dengan URL GitHub kamu yang asli!)*

2.  **Instal dependensi (termasuk MySQL driver):**
    ```bash
    npm install
    ```

3.  **Atur Environment Variables:**
    * Project ini menggunakan file `.env` untuk menyimpan konfigurasi *database* dan rahasia lainnya.
    * *Duplikat* atau *copy* file `.env.example` dan ubah namanya menjadi `.env`.
    * Buka file `.env` tersebut dan sesuaikan bagian *database* dengan konfigurasi MySQL lokal kamu:
        ```env
        DATABASE_CLIENT=mysql
        DATABASE_HOST=127.0.0.1
        DATABASE_PORT=3306
        DATABASE_NAME=nama_database_yang_kamu_buat_tadi
        DATABASE_USERNAME=root
        DATABASE_PASSWORD= # Isi jika ada password, biarkan kosong jika default XAMPP
        ```

### 4. Jalankan Aplikasi
Setelah *database* siap dan file `.env` sudah diatur, jalankan perintah berikut:

```bash
npm run develop
