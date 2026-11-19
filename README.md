# Sistem Informasi Perpustakaan

Aplikasi web Sistem Informasi Perpustakaan merupakan aplikasi untuk membantu petugas perpustakaan dalam mengelola data buku, data anggota, transaksi peminjaman, pengembalian, dan laporan perpustakaan.

## Teknologi yang Digunakan

- PHP 8.2 atau lebih baru
- Laravel 12
- MySQL / MariaDB
- Blade
- Bootstrap
- JavaScript

## Fitur Aplikasi

### 1. Login Admin
- Login dan logout admin.
- Halaman aplikasi dilindungi menggunakan middleware authentication.

### 2. Manajemen Buku
- Menampilkan daftar buku.
- Menambahkan buku.
- Mengubah data buku.
- Menghapus buku.
- Pencarian berdasarkan judul dan penulis.
- Pagination 10 data per halaman.

### 3. Manajemen Anggota
- Menampilkan daftar anggota.
- Menambahkan anggota.
- Mengubah data anggota.
- Menghapus anggota.
- Melihat riwayat peminjaman anggota.

### 4. Transaksi Peminjaman
- Memilih anggota dan buku.
- Tanggal peminjaman otomatis menggunakan tanggal hari ini.
- Memeriksa ketersediaan stok buku.
- Stok buku berkurang ketika peminjaman berhasil.

### 5. Pengembalian Buku
- Mengubah status peminjaman menjadi dikembalikan.
- Mencatat tanggal pengembalian.
- Memperbarui stok berdasarkan kondisi buku.
- Menghitung denda keterlambatan.

### 6. Dashboard
- Menampilkan jumlah buku.
- Menampilkan jumlah anggota.
- Menampilkan jumlah buku yang sedang dipinjam.
- Menampilkan total denda bulan ini.

### 7. Laporan
- Menampilkan laporan peminjaman.
- Filter berdasarkan tanggal dan status.
- Cetak laporan.
- Export laporan ke Excel.

## Persyaratan Instalasi

Pastikan perangkat sudah memiliki:

- PHP
- Composer
- MySQL atau MariaDB
- Node.js dan NPM

## Cara Instalasi

### 1. Clone Repository

```bash
git clone URL_REPOSITORY_KAMU
```

Masuk ke folder project:

```bash
cd peminjaman-buku-perpustakaan
```

### 2. Install Dependency

```bash
composer install
```

### 3. Konfigurasi Environment

Salin file `.env.example` menjadi `.env`.

Kemudian sesuaikan konfigurasi database pada file `.env`:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=peminjaman_buku_perpustakaan
DB_USERNAME=root
DB_PASSWORD=
```

Sesuaikan nama database, username, dan password dengan konfigurasi MySQL di perangkat masing-masing.

### 4. Generate Application Key

```bash
php artisan key:generate
```

### 5. Jalankan Migration dan Seeder

```bash
php artisan migrate --seed
```

Perintah ini akan membuat tabel database dan mengisi data awal berupa akun admin, data buku, serta data anggota.

### 6. Install dan Build Asset

```bash
npm install
npm run build
```

### 7. Jalankan Aplikasi

```bash
php artisan serve
```

Buka aplikasi melalui browser:

```text
http://127.0.0.1:8000
```

## Akun Login Demo

Gunakan akun berikut untuk masuk ke aplikasi:

| Keterangan | Akun |
|---|---|
| Email | admin@gmail.com |
| Password | admin12345 |

Catatan: Akun tersebut merupakan akun demo dari seeder. Ganti password untuk penggunaan di luar keperluan pengujian.

## Database

Database dibuat menggunakan Laravel Migration dan data awal disediakan melalui Seeder.

Tabel utama:

- users
- books
- members
- loans

## Pengembang

**Nama:** [Isi Nama Kamu]

**Project:** Sistem Informasi Perpustakaan

**Tujuan:** Tes Team Programmer Prilude Studio
