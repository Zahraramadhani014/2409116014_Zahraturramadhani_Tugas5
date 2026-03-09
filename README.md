# 📱 TUGAS_PAB 📱

---

<h1 align="center">
📝 Registration Form Hands-On 🚀
</h1>

<p align="center">
  <b>Form Registrasi Event Kampus</b>
</p>

---

## 👩‍🎓 Identitas Mahasiswa

| Nama | NIM | Mata Kuliah | Dosen |
|------|------|--------------|--------|
| Zahraturramadhani | 2409116014 | Pemrograman Aplikasi Bergerak | Anton Prafanto, S.Kom., M.T. |

---

## 📌 Deskripsi Project

Project ini merupakan pembuatan aplikasi **Form Registrasi Event Kampus** menggunakan Flutter dengan bantuan state management **Provider**. Aplikasi ini dibuat untuk mensimulasikan proses pendaftaran peserta pada sebuah event, di mana pengguna diminta untuk mengisi beberapa data seperti nama lengkap, email, password, jenis kelamin, program studi, tanggal lahir, serta persetujuan terhadap syarat dan ketentuan yang berlaku.

Data yang dimasukkan oleh pengguna tidak hanya ditampilkan di halaman form saja, tetapi juga disimpan menggunakan **Provider (ChangeNotifier)** sehingga dapat digunakan kembali pada halaman lain di dalam aplikasi. Dengan cara ini, data pendaftar bisa dikelola secara lebih terstruktur dan dapat langsung diperbarui pada tampilan ketika terjadi perubahan.

Selain halaman form registrasi, aplikasi ini juga memiliki halaman **daftar pendaftar** yang menampilkan seluruh data peserta yang telah terdaftar. Dari halaman tersebut pengguna juga dapat membuka **halaman detail pendaftar** untuk melihat informasi lengkap dari setiap peserta yang telah melakukan registrasi.

Melalui project ini, diharapkan dapat memahami bagaimana cara membuat form interaktif di Flutter dengan berbagai jenis input, menerapkan validasi data secara langsung saat pengguna mengisi form, serta memanfaatkan Provider sebagai solusi pengelolaan state agar data dapat digunakan bersama oleh beberapa halaman dalam aplikasi.

---

## ✏️ Ketentuan Project

**Features:**

- ✅ Multi-field form (nama, email, password, dll)
- ✅ Real-time validation
- ✅ Berbagai input widgets (TextFormField, Radio, Dropdown, DatePicker, Checkbox)
- ✅ Provider untuk menyimpan daftar pendaftar
- ✅ Halaman list pendaftar
- ✅ Halaman detail pendaftar

**App Structure:**

```
┌──────────────────┐     ┌──────────────────┐     ┌──────────────────┐
│  Registration    │────→│  Registrant      │────→│  Registrant      │
│  Form Page       │     │  List Page       │     │  Detail Page     │
│                  │     │                  │     │                  │
│ • Name           │     │ • ListView       │     │ • Full info      │
│ • Email          │     │ • Badge count    │     │ • All fields     │
│ • Password       │     │ • Delete action  │     │                  │
│ • Gender (Radio) │     │                  │     │                  │
│ • Prodi (Drop)   │     │                  │     │                  │
│ • DoB (Date)     │     │                  │     │                  │
│ • Agree (Check)  │     │                  │     │                  │
└──────────────────┘     └──────────────────┘     └──────────────────┘
       ↑                          ↑                        ↑
       └──────────────────────────┴────────────────────────┘
                    Provider (RegistrationProvider)
                  Shared state: List<Registrant>
```

## ⚙️ Struktur Program

<img width="247" height="771" alt="image" src="https://github.com/user-attachments/assets/d069150a-e65e-458b-bccb-3931e5f22862" />

Struktur project pada aplikasi ini mengikuti struktur standar yang biasanya digunakan pada project Flutter. Secara umum, folder seperti **android**, **ios**, **web**, **windows**, **linux**, dan **macos** merupakan folder bawaan dari Flutter yang digunakan untuk mendukung aplikasi agar dapat dijalankan di berbagai platform.

Bagian utama dari aplikasi yang dikembangkan berada di dalam folder **lib**, karena pada folder inilah seluruh kode program yang dibuat berada. Di dalam folder **lib** terdapat beberapa bagian yang dipisahkan berdasarkan fungsinya agar kode lebih rapi dan mudah dipahami.

Folder **models** digunakan untuk menyimpan struktur data yang digunakan dalam aplikasi. Pada project ini terdapat file `registrant_model.dart` yang berisi model data pendaftar, seperti nama, email, gender, program studi, tanggal lahir, dan waktu registrasi.

Folder **providers** digunakan untuk mengelola state aplikasi menggunakan Provider. File `registration_provider.dart` berfungsi untuk menyimpan daftar pendaftar, menambahkan data baru, menghapus data pendaftar, serta mengambil data berdasarkan ID.

Selanjutnya terdapat folder **pages** yang berisi tampilan dari setiap halaman aplikasi. Pada folder ini terdapat tiga halaman utama, yaitu `registration_page.dart` sebagai halaman form pendaftaran, `registrant_list_page.dart` untuk menampilkan daftar peserta yang sudah terdaftar, serta `registrant_detail_page.dart` untuk menampilkan informasi lengkap dari peserta yang dipilih.

Selain itu terdapat juga file **main.dart** yang merupakan titik awal ketika aplikasi dijalankan. Pada file ini dilakukan konfigurasi aplikasi seperti pengaturan tema, routing halaman, serta penyediaan Provider agar data pendaftar dapat diakses oleh seluruh halaman yang ada di dalam aplikasi.

---

## 📸 Screenshoot Aplikasi

### Form Registrasi

<img width="1919" height="1140" alt="image" src="https://github.com/user-attachments/assets/3f075f4d-a38c-4b25-af12-2271e6772535" />

---

### Validasi Form

<img width="1919" height="1140" alt="image" src="https://github.com/user-attachments/assets/d09d9a66-d835-4374-9913-5d8482619c46" />

---

### List Pendaftar

<img width="1919" height="1142" alt="image" src="https://github.com/user-attachments/assets/ad8f2a64-ca60-4f61-959c-fb2658e6e4df" />

---

### Detail Pendaftar

<img width="1919" height="1140" alt="image" src="https://github.com/user-attachments/assets/f0d7950d-7000-42b4-8c99-1ff5f1e0ea9b" />

---

## 🔄 Alur Program

### 1️⃣ Aplikasi dijalankan

Ketika aplikasi dijalankan, Flutter akan mulai mengeksekusi file **main.dart** sebagai titik awal program. Pada file ini dilakukan konfigurasi utama aplikasi, seperti pengaturan tema, routing halaman, serta penyediaan state management menggunakan **Provider**.

Di dalam `main.dart`, aplikasi dibungkus dengan **ChangeNotifierProvider** yang berfungsi untuk menyediakan `RegistrationProvider` ke seluruh bagian aplikasi. Provider ini nantinya digunakan untuk menyimpan dan mengelola data pendaftar yang dimasukkan melalui form registrasi.

Setelah itu, aplikasi akan membangun widget utama yaitu **MaterialApp**. Pada bagian ini juga ditentukan beberapa route yang digunakan untuk berpindah antar halaman, seperti halaman form registrasi, halaman daftar pendaftar, dan halaman detail pendaftar.

Dengan adanya konfigurasi ini, setiap halaman dalam aplikasi dapat mengakses data pendaftar yang sama melalui Provider tanpa perlu mengirim data secara manual antar halaman.

><img width="1917" height="1140" alt="image" src="https://github.com/user-attachments/assets/9244ed2f-5792-4fde-abb3-79835b8aa2b1" />

---

### 2️⃣ Halaman Registrasi

Setelah aplikasi berhasil dijalankan, halaman pertama yang muncul adalah **halaman registrasi**. Pada halaman ini pengguna diminta untuk mengisi beberapa data yang diperlukan untuk melakukan pendaftaran event.

Form registrasi ini terdiri dari beberapa field input, seperti **nama lengkap, email, password, jenis kelamin, program studi, tanggal lahir**, serta **persetujuan terhadap syarat dan ketentuan**. Beberapa field menggunakan jenis input yang berbeda, misalnya radio button untuk memilih jenis kelamin, dropdown untuk memilih program studi, serta date picker untuk memilih tanggal lahir.

Setiap field yang memiliki tanda (*) berarti wajib diisi oleh pengguna. Jika ada field yang belum diisi atau format data tidak sesuai, maka sistem akan menampilkan pesan validasi agar pengguna dapat memperbaiki input tersebut sebelum melanjutkan proses pendaftaran.

Dengan adanya form ini, pengguna dapat memasukkan data pendaftaran secara lengkap sebelum data tersebut diproses dan disimpan oleh sistem.

><img width="1916" height="1142" alt="image" src="https://github.com/user-attachments/assets/99a51f5f-ce4f-401c-b3a0-6265007e6a77" />

Sebagai contoh, pada gambar di bawah ditampilkan salah satu contoh pengisian form registrasi oleh pengguna. Pada contoh tersebut, pengguna telah mengisi beberapa data yang diminta oleh sistem seperti nama lengkap, email, password, jenis kelamin, program studi, serta tanggal lahir. Selain itu, pengguna juga mencentang bagian persetujuan syarat dan ketentuan sebagai tanda bahwa pengguna menyetujui aturan yang berlaku pada proses pendaftaran. Contoh ini menunjukkan bagaimana form registrasi dapat diisi secara lengkap sebelum data dikirim ke sistem. 

><img width="1919" height="1141" alt="image" src="https://github.com/user-attachments/assets/143e1004-fb8e-4ca8-8bb4-9719cb2804d7" />

##### Validasi Form

Jika data yang dimasukkan oleh pengguna tidak sesuai dengan ketentuan yang ada, maka sistem akan menampilkan pesan kesalahan pada field yang bermasalah. Pada gambar di bawah dapat dilihat beberapa contoh validasi yang muncul, seperti nama yang kurang dari jumlah karakter minimal, format email yang tidak valid, password yang belum memenuhi syarat, program studi yang belum dipilih, serta tanggal lahir yang belum diisi.

Validasi ini bertujuan untuk membantu pengguna agar dapat memperbaiki data yang dimasukkan sebelum melanjutkan proses pendaftaran. Dengan adanya validasi ini, sistem dapat memastikan bahwa data yang dikirim sudah lengkap dan sesuai dengan format yang diharapkan.

><img width="1919" height="1142" alt="image" src="https://github.com/user-attachments/assets/f9f1ec08-bf3b-4e05-a6ff-110c9caab4b4" />

Pada gambar di bawah ditunjukkan kondisi ketika pengguna mencoba melakukan pendaftaran menggunakan email yang sudah pernah digunakan sebelumnya. Sistem akan mendeteksi bahwa email tersebut sudah terdaftar di dalam data pendaftar.

Ketika hal ini terjadi, aplikasi akan menampilkan pesan pemberitahuan di bagian bawah layar yang menyatakan bahwa **email sudah terdaftar**. Dengan adanya pengecekan ini, sistem dapat mencegah terjadinya data pendaftar yang duplikat sehingga setiap peserta hanya dapat menggunakan satu email untuk melakukan registrasi.

><img width="1919" height="1139" alt="image" src="https://github.com/user-attachments/assets/63eee277-3c72-4646-aa96-9adb09876e0d" />

Pada gambar ini ditunjukkan kondisi ketika pengguna mencoba melakukan pendaftaran tanpa mencentang bagian persetujuan **syarat dan ketentuan**. Meskipun seluruh data pada form sudah diisi, proses registrasi tidak dapat dilanjutkan jika bagian ini belum dicentang.

Ketika pengguna menekan tombol **Daftar Sekarang**, sistem akan menampilkan pesan peringatan yang meminta pengguna untuk terlebih dahulu menyetujui syarat dan ketentuan yang berlaku. Hal ini bertujuan untuk memastikan bahwa pengguna memahami dan menyetujui aturan yang ada sebelum proses pendaftaran dilakukan.

><img width="1919" height="1141" alt="image" src="https://github.com/user-attachments/assets/c043c7eb-4181-4162-8089-a9cdfd401202" />

Pada gambar di bawah ditunjukkan fungsi dari tombol **Reset Form** yang terdapat di bawah tombol Daftar Sekarang. Tombol ini digunakan untuk menghapus seluruh data yang sudah diisi pada form pendaftaran.

Ketika tombol reset ditekan, semua field input seperti nama, email, password, pilihan jenis kelamin, program studi, serta tanggal lahir akan kembali ke kondisi awal seperti saat halaman pertama kali dibuka. Dengan adanya fitur ini, pengguna dapat dengan mudah mengosongkan form jika ingin mengisi ulang data dari awal.

><img width="1919" height="1138" alt="image" src="https://github.com/user-attachments/assets/7accf7c7-bc77-4de9-9657-c4070a849191" />

Pada gambar di bawah ditunjukkan halaman registrasi yang juga menyediakan akses untuk melihat daftar peserta yang telah mendaftar. Jika pengguna ingin melihat data peserta yang sudah terdaftar, pengguna dapat menekan ikon yang berada di bagian kanan atas pada AppBar.

Ikon tersebut berfungsi sebagai tombol navigasi yang akan membawa pengguna menuju halaman daftar peserta. Dengan adanya fitur ini, pengguna dapat dengan mudah berpindah dari halaman registrasi ke halaman yang menampilkan seluruh data pendaftar.

><img width="1600" height="952" alt="image" src="https://github.com/user-attachments/assets/660bbf8d-b1c8-4b09-a4aa-c8d3fa646917" />

Setelah ikon tersebut ditekan, aplikasi akan mengarahkan pengguna ke halaman **daftar peserta**. Pada halaman ini ditampilkan seluruh data peserta yang telah berhasil melakukan registrasi.

Setiap peserta ditampilkan dalam bentuk daftar yang berisi informasi seperti nama peserta, program studi, serta email yang digunakan saat mendaftar. Melalui halaman ini pengguna dapat melihat siapa saja yang telah terdaftar dalam event tersebut dan juga dapat melakukan beberapa tindakan lain seperti membuka detail peserta atau menghapus data peserta dari daftar.

<img width="1919" height="1142" alt="image" src="https://github.com/user-attachments/assets/20df40d8-a6c8-4298-8d35-8e50aeef4031" />

---

### 3️⃣ Submit Form

Setelah semua data pada form diisi dengan lengkap dan sesuai dengan ketentuan yang diminta, pengguna dapat menekan tombol **Daftar Sekarang** untuk mengirimkan data pendaftaran. Tombol ini berfungsi untuk memproses seluruh data yang telah dimasukkan pada form.

Ketika tombol tersebut ditekan, sistem akan terlebih dahulu memeriksa kembali apakah semua field yang wajib sudah terisi dengan benar. Jika tidak ada kesalahan pada data yang dimasukkan, maka proses registrasi akan dilanjutkan dan data pendaftar akan disimpan oleh sistem.

Langkah ini merupakan tahap akhir dari proses pengisian form sebelum pengguna mendapatkan konfirmasi bahwa pendaftaran telah berhasil dilakukan.

><img width="1600" height="951" alt="image" src="https://github.com/user-attachments/assets/de7008e5-35ac-4a8d-93db-55208e25bc9d" />

---

### 4️⃣ Registrasi Berhasil

Setelah pengguna menekan tombol **Daftar Sekarang** dan semua data yang dimasukkan sudah sesuai dengan ketentuan, maka sistem akan menampilkan dialog yang menandakan bahwa proses **registrasi telah berhasil**. Pada dialog tersebut terdapat informasi bahwa data pendaftar sudah berhasil disimpan oleh sistem. Dialog ini juga menyediakan dua pilihan tombol yang dapat digunakan oleh pengguna.

><img width="1919" height="1140" alt="image" src="https://github.com/user-attachments/assets/ced5968f-8031-4f30-81ab-065ff328b1e8" />

Tombol pertama adalah **Daftar Lagi**, yang berfungsi untuk mengarahkan pengguna kembali ke halaman form registrasi sehingga pengguna dapat melakukan pendaftaran baru dengan data yang berbeda.

><img width="1919" height="1141" alt="image" src="https://github.com/user-attachments/assets/c87b63c5-d7c8-4452-914f-2f224d839fd7" />

Sedangkan tombol kedua adalah **Lihat Daftar**, yang akan mengarahkan pengguna ke halaman **daftar peserta**. Pada halaman ini pengguna dapat melihat seluruh data pendaftar yang sudah tersimpan di dalam sistem. Setiap peserta akan ditampilkan dalam bentuk daftar yang berisi nama serta informasi program studi dan email yang digunakan saat registrasi. Dengan adanya dua pilihan ini, pengguna dapat dengan mudah memilih apakah ingin melakukan pendaftaran ulang atau langsung melihat daftar peserta yang sudah terdaftar.

><img width="1919" height="1138" alt="image" src="https://github.com/user-attachments/assets/35a3d20f-6305-4d57-9df2-63cd41f73fd6" />

---

### 5️⃣ Halaman List Pendaftar

Halaman ini menampilkan seluruh data peserta yang telah berhasil melakukan registrasi. Data yang sebelumnya dimasukkan melalui form pendaftaran akan disimpan oleh sistem dan kemudian ditampilkan dalam bentuk daftar pada halaman ini.

Pada halaman ini pengguna dapat melihat beberapa informasi dasar dari setiap peserta, seperti **nama, program studi, dan email** yang digunakan saat registrasi. Setiap peserta ditampilkan dalam bentuk card atau list sehingga lebih mudah untuk dibaca.

Selain menampilkan daftar peserta, halaman ini juga menyediakan beberapa fitur tambahan. Pengguna dapat membuka **halaman detail peserta** dengan menekan salah satu data pada daftar. Selain itu, tersedia juga ikon **tong sampah berwarna merah** yang berfungsi untuk menghapus data peserta dari daftar, dan juga ikon tambah (+) yang berfungsi untuk menambah peserta lagi yang nantinya akan diarahkan ke halaman registrasi.

><img width="1919" height="1138" alt="image" src="https://github.com/user-attachments/assets/c4e25279-16b2-43c2-b544-3d8a4329f67b" />

Jika pengguna menekan ikon hapus tersebut, maka sistem akan menampilkan dialog konfirmasi untuk memastikan apakah pengguna benar-benar ingin menghapus data tersebut.

><img width="1919" height="1140" alt="image" src="https://github.com/user-attachments/assets/0167c030-d4f4-4a39-890b-72068b013280" />

- Jika pengguna memilih tombol **Batal**, maka proses penghapusan akan dibatalkan dan data peserta tetap ada pada daftar.

  ><img width="1917" height="1138" alt="image" src="https://github.com/user-attachments/assets/41d6e3ff-4e17-4a48-b258-d656e9b9aee5" />

- Namun jika pengguna memilih tombol **Hapus**, maka data peserta tersebut akan dihapus dari daftar pendaftar.

  ><img width="1918" height="1141" alt="image" src="https://github.com/user-attachments/assets/ae5877a6-4539-4dd4-94ef-7055aa384713" />

Pada gambar di bawah ditunjukkan halaman yang akan muncul ketika pengguna ingin menambahkan peserta baru. Untuk menambahkan peserta, pengguna cukup menekan ikon **tanda tambah (+)** yang terdapat pada halaman daftar pendaftar.

Setelah ikon tersebut diklik, aplikasi akan langsung mengarahkan pengguna kembali ke **halaman registrasi**. Di halaman ini pengguna dapat mengisi kembali form pendaftaran dengan data peserta yang baru. Dengan adanya fitur ini, pengguna dapat dengan mudah menambahkan beberapa peserta tanpa harus kembali ke halaman utama secara manual.

><img width="1919" height="1141" alt="image" src="https://github.com/user-attachments/assets/a89033bb-a459-4d59-92fc-aea81155e14e" />

---

### 6️⃣ Halaman Detail Peserta

Halaman ini digunakan untuk menampilkan informasi lengkap dari peserta yang telah terdaftar. Halaman detail ini dapat dibuka dengan cara menekan salah satu data peserta yang ada pada halaman daftar pendaftar.

Pada halaman ini ditampilkan beberapa informasi penting mengenai peserta, seperti **nama, email, jenis kelamin, program studi, tanggal lahir, umur**, serta **waktu registrasi** ketika data tersebut pertama kali didaftarkan. Informasi tersebut ditampilkan secara lebih lengkap agar pengguna dapat melihat detail data peserta dengan lebih jelas.

Selain itu, pada bagian atas halaman juga ditampilkan avatar yang berisi huruf pertama dari nama peserta sebagai identitas visual. Dengan adanya halaman detail ini, pengguna dapat melihat informasi peserta secara lebih terperinci tanpa harus kembali ke form registrasi.

><img width="1916" height="1138" alt="image" src="https://github.com/user-attachments/assets/c175be11-270a-4efc-ade3-bf295cf4d458" />

---
