# 📱 TUGAS_PAB 📱

---

<h1 align="center">
📝 Event Registration App dengan Provider 🚀
</h1>

---

## 👩‍🎓 Identitas Mahasiswa

| Nama | NIM | Mata Kuliah | Dosen |
|------|------|--------------|--------|
| Zahraturramadhani | 2409116014 | Pemrograman Aplikasi Bergerak | Anton Prafanto, S.Kom., M.T. |

---

## 📌 Deskripsi Project

Project ini merupakan implementasi **Form Registrasi Event Kampus** menggunakan Flutter dengan konsep **state management Provider**.

Aplikasi ini memungkinkan pengguna untuk melakukan pendaftaran event dengan mengisi berbagai field input seperti nama, email, password, jenis kelamin, program studi, tanggal lahir, serta persetujuan syarat dan ketentuan.

Data pendaftar kemudian disimpan menggunakan **Provider (ChangeNotifier)** sehingga dapat digunakan secara bersama oleh beberapa halaman aplikasi.

Aplikasi ini juga dilengkapi dengan halaman **daftar pendaftar** dan **detail pendaftar**, sehingga data yang telah dimasukkan dapat dilihat kembali oleh pengguna.

Tujuan dari project ini adalah untuk memahami:

- Penggunaan berbagai jenis **Form Widgets di Flutter**
- Implementasi **validasi form secara real-time**
- Penggunaan **Provider sebagai state management**
- Pengelolaan **shared state antar halaman**

---

# 🏗️ PART 5: Registration Form Hands-On (Main Project)

## Project Overview

Aplikasi ini merupakan **Form Registrasi Event Kampus** yang memiliki beberapa fitur utama seperti:

- Form pendaftaran dengan berbagai jenis input
- Validasi form secara real-time
- Penyimpanan data pendaftar menggunakan Provider
- Halaman daftar peserta
- Halaman detail peserta

---

## App Structure


┌──────────────────┐ ┌──────────────────┐ ┌──────────────────┐
│ Registration │────→│ Registrant │────→│ Registrant │
│ Form Page │ │ List Page │ │ Detail Page │
│ │ │ │ │ │
│ • Name │ │ • ListView │ │ • Full info │
│ • Email │ │ • Badge count │ │ • All fields │
│ • Password │ │ • Delete action │ │ │
│ • Gender (Radio) │ │ │ │ │
│ • Prodi (Drop) │ │ │ │ │
│ • DoB (Date) │ │ │ │ │
│ • Agree (Check) │ │ │ │ │
└──────────────────┘ └──────────────────┘ └──────────────────┘
↑ ↑ ↑
└──────────────────────────┴────────────────────────┘
Provider (RegistrationProvider)
Shared state: List<Registrant>


---

# ✅ Features Checklist

### Fitur Wajib

- [x] Minimal **5 field input berbeda jenis**
- [x] **Validasi real-time** menggunakan `autovalidateMode`
- [x] Minimal **2 input selain TextFormField**
  - Radio Button
  - Dropdown
  - Checkbox
  - DatePicker
- [x] Menggunakan **Provider** untuk menyimpan data pendaftar
- [x] Halaman **List Pendaftar**
- [x] **Error handling menggunakan try-catch**
- [x] **Reset form setelah submit berhasil**

---

### ⭐ Bonus Features

- [ ] Multi-step form menggunakan **Stepper**
- [ ] **Edit data pendaftar**
- [ ] **Search / filter pendaftar**

---

# ⚙️ Struktur Program

Struktur project mengikuti standar Flutter.

Folder utama aplikasi berada pada **folder `lib`** yang berisi beberapa bagian penting.

---

## 📂 models

Berisi struktur data aplikasi.


models/
registrant_model.dart


File ini berfungsi untuk menyimpan model data pendaftar seperti:

- Nama
- Email
- Gender
- Program Studi
- Tanggal Lahir
- Waktu Registrasi

---

## 📂 providers

Berisi **state management** menggunakan Provider.


providers/
registration_provider.dart


Provider ini berfungsi untuk:

- Menyimpan daftar pendaftar
- Menambahkan data pendaftar
- Menghapus data pendaftar
- Mengambil data berdasarkan ID

---

## 📂 pages

Berisi tampilan halaman aplikasi.


pages/
registration_page.dart
registrant_list_page.dart
registrant_detail_page.dart


Penjelasan:

**registration_page.dart**

Halaman form untuk melakukan pendaftaran event.

**registrant_list_page.dart**

Halaman yang menampilkan daftar seluruh peserta yang telah mendaftar.

**registrant_detail_page.dart**

Halaman yang menampilkan informasi lengkap dari peserta yang dipilih.

---

## 📄 main.dart

File ini merupakan **entry point aplikasi**.

Di dalam file ini juga terdapat:

- konfigurasi `MaterialApp`
- konfigurasi `routes`
- penyediaan `ChangeNotifierProvider`

---

# 📸 Screenshot Aplikasi

### Form Registrasi

Tambahkan screenshot form kosong di sini.

---

### Validasi Form

Tambahkan screenshot validasi error di sini.

---

### List Pendaftar

Tambahkan screenshot halaman daftar peserta.

---

### Detail Pendaftar

Tambahkan screenshot halaman detail peserta.

---

# 🔄 Alur Program

### 1️⃣ Aplikasi dijalankan

Ketika aplikasi dijalankan, Flutter akan mengeksekusi file **main.dart**.

Pada tahap ini aplikasi dibungkus dengan:


ChangeNotifierProvider


yang menyediakan **RegistrationProvider** untuk seluruh aplikasi.

---

### 2️⃣ Halaman Registrasi

Halaman pertama yang muncul adalah **Registration Page**.

Pengguna diminta mengisi beberapa field seperti:

- Nama
- Email
- Password
- Gender
- Program Studi
- Tanggal Lahir
- Persetujuan syarat & ketentuan

---

### 3️⃣ Submit Form

Setelah pengguna menekan tombol **Daftar Sekarang**:

- Sistem melakukan **validasi form**
- Jika valid maka data akan disimpan menggunakan **Provider**

---

### 4️⃣ Registrasi Berhasil

Jika proses registrasi berhasil:

- Akan muncul dialog **Registrasi Berhasil**
- Pengguna dapat memilih:
  - **Daftar Lagi**
  - **Lihat Daftar Peserta**

---

### 5️⃣ Halaman List Pendaftar

Halaman ini menampilkan seluruh data peserta yang telah terdaftar.

Pada halaman ini pengguna dapat:

- Melihat daftar peserta
- Menghapus data peserta
- Membuka halaman detail peserta

---

### 6️⃣ Halaman Detail Peserta

Pada halaman ini ditampilkan informasi lengkap peserta seperti:

- Nama
- Email
- Gender
- Program Studi
- Tanggal Lahir
- Umur
- Waktu Registrasi

---

# 📌 Catatan

Project ini dibuat untuk memenuhi tugas praktikum **Pemrograman Aplikasi Bergerak** mengenai implementasi **Form Handling dan State Management menggunakan Provider pada Flutter**.

Source code project tersedia pada repository GitHub.
