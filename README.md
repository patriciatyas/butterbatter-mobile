# 🧈 Butter & Batter Mobile App 🧈

Patricia Herningtyas (2306152241)
PBP - A

# TUGAS INDIVIDU 7

## Jelaskan apa yang dimaksud dengan stateless widget dan stateful widget, dan jelaskan perbedaan dari keduanya.
- **Stateless widget** adalah widget yang tidak memiliki "state" yang dapat berubah saat aplikasi berjalan. Artinya, setelah widget ini dibangun, ia tidak akan dirender ulang dengan perubahan data. Contoh: Text, Icon, atau Container, yang hanya menampilkan data statis.
- **Stateful widget** adalah widget yang memiliki "state" yang dapat berubah selama aplikasi berjalan. Stateful widget akan dirender ulang setiap kali state berubah. Ini cocok untuk elemen interaktif, seperti form input, animasi, atau elemen yang menampilkan data yang berubah seiring waktu.
- **Perbedaan** antara keduanya adalah pada kemampuannya untuk berubah. Stateless widget tidak berubah setelah dibuat, sedangkan stateful widget dapat berubah sesuai dengan statenya. Dalam stateful widget, perubahan pada state menyebabkan widget dirender ulang untuk mencerminkan perubahan tersebut.

## Sebutkan widget apa saja yang kamu gunakan pada proyek ini dan jelaskan fungsinya.
- MaterialApp: Widget utama yang menyediakan struktur dasar untuk aplikasi dengan tema Material Design
- Scaffold: Menyediakan struktur dasar halaman, termasuk AppBar dan body, yang mempermudah membuat tata letak.
- AppBar: Menyediakan area untuk menampilkan judul atau tombol navigasi di bagian atas halaman.
- ElevatedButton: Widget tombol yang terangkat dengan efek bayangan. Dalam proyek ini, tombol ini digunakan untuk berbagai tindakan (melihat daftar produk, menambah produk, dan logout).
- SnackBar: Menampilkan pesan sementara di bagian bawah layar sebagai notifikasi atau informasi singkat untuk pengguna.
- Icon: Menampilkan ikon pada tombol untuk memperjelas fungsi dari tombol tersebut.
- Column: Menyusun widget di dalamnya dalam bentuk kolom secara vertikal.
- Text: Digunakan untuk menampilkan teks, seperti label pada tombol dan konten pada SnackBar.

## Apa fungsi dari `setState()`? Jelaskan variabel apa saja yang dapat terdampak dengan fungsi tersebut.

Fungsi `setState()` digunakan dalam stateful widget adalah untuk memberi tahu Flutter bahwa state dari widget telah berubah, sehingga widget tersebut perlu dirender ulang. Ketika `setState()` dipanggil, Flutter akan menjalankan ulang build method untuk memperbarui tampilan sesuai perubahan data.

Semua variabel yang terdefinisi dalam state widget dapat terdampak oleh `setState()`. Hanya variabel yang mengalami perubahan di dalam `setState()` yang akan diperbarui pada tampilan.

## Jelaskan perbedaan antara const dengan final.
`const` digunakan untuk nilai yang bersifat konstan pada waktu kompilasi. Artinya, nilai tersebut harus sudah diketahui dan tidak boleh berubah selama eksekusi aplikasi. Contoh, const digunakan untuk widget atau nilai yang tidak akan pernah berubah.

`final` digunakan untuk nilai yang tetap setelah diberikan, tetapi nilainya dapat diketahui saat runtime, bukan hanya saat kompilasi. Contoh, objek yang diambil dari API bisa menggunakan final karena nilai tersebut akan tetap setelah diinisialisasi, namun diperoleh saat runtime.

## Jelaskan bagaimana cara kamu mengimplementasikan checklist-checklist di atas.
1. Membuat program Flutter baru dengan tema E-Commerce. Dalam direktori pbp-flutter yang telah saya buat, saya menjalankan command `flutter create butter_and_batter` untuk membuat program Flutter baru, dan menjalankan `flutter doctor` untuk memeriksa error.
2. Membuat tiga tombol -> Saya menggunakan widget ElevatedButton.icon untuk membuat tombol-tombol dengan ikon dan teks. Setiap tombol dikonfigurasi dengan warna yang berbeda menggunakan `backgroundColor` untuk membedakan tiap fungsinya.
3. Membuat SnackBar -> Pada setiap tombol, saya menambahkan onPressed yang memanggil fungsi `_showSnackbar()`. Fungsi ini menampilkan SnackBar dengan pesan yang berbeda sesuai dengan tombol yang ditekan. Tanda underscore pada fungsi `_showSnackbar()` menunjukkan bahwa fungsi tersebut hanya dapat dipanggil dari dalam kelas `SnackBarPage` untuk mengurangi kemungkinan konflik nama dalam proyek yang lebih besar nantinya.
4. Pada setiap tombol, saya menggunakan `ElevatedButton.styleFrom` untuk mengatur warna latar (backgroundColor) dan warna teks (foregroundColor) menjadi putih.

