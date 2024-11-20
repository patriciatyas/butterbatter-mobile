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

## Jelaskan perbedaan antara `const` dengan final.
``const`` digunakan untuk nilai yang bersifat konstan pada waktu kompilasi. Artinya, nilai tersebut harus sudah diketahui dan tidak boleh berubah selama eksekusi aplikasi. Contoh, `const` digunakan untuk widget atau nilai yang tidak akan pernah berubah.

`final` digunakan untuk nilai yang tetap setelah diberikan, tetapi nilainya dapat diketahui saat runtime, bukan hanya saat kompilasi. Contoh, objek yang diambil dari API bisa menggunakan final karena nilai tersebut akan tetap setelah diinisialisasi, namun diperoleh saat runtime.

## Jelaskan bagaimana cara kamu mengimplementasikan checklist-checklist di atas.
1. Membuat program Flutter baru dengan tema E-Commerce. Dalam direktori pbp-flutter yang telah saya buat, saya menjalankan command `flutter create butter_and_batter` untuk membuat program Flutter baru, dan menjalankan `flutter doctor` untuk memeriksa error.
2. Membuat tiga tombol -> Saya menggunakan widget ElevatedButton.icon untuk membuat tombol-tombol dengan ikon dan teks. Setiap tombol dikonfigurasi dengan warna yang berbeda menggunakan `backgroundColor` untuk membedakan tiap fungsinya.
3. Membuat SnackBar -> Pada setiap tombol, saya menambahkan onPressed yang memanggil fungsi `_showSnackbar()`. Fungsi ini menampilkan SnackBar dengan pesan yang berbeda sesuai dengan tombol yang ditekan. Tanda underscore pada fungsi `_showSnackbar()` menunjukkan bahwa fungsi tersebut hanya dapat dipanggil dari dalam kelas `SnackBarPage` untuk mengurangi kemungkinan konflik nama dalam proyek yang lebih besar nantinya.
4. Pada setiap tombol, saya menggunakan `ElevatedButton.styleFrom` untuk mengatur warna latar (backgroundColor) dan warna teks (foregroundColor) menjadi putih.

# TUGAS INDIVIDU 8
## Apa kegunaan `const` di Flutter? Jelaskan apa keuntungan ketika menggunakan `const` pada kode Flutter. Kapan sebaiknya kita menggunakan const, dan kapan sebaiknya tidak digunakan?
`const` digunakan pada Flutter untuk mendeklarasikan konstanta yang nilainya tetap sepanjang waktu. Manfaat utama `const` adalah meningkatkan efisiensi performa karena objek yang dideklarasikan dengan `const` dibuat hanya sekali dan dapat digunakan kembali. `const` lebih baik digunakan ketika kita yakin bahwa nilai atau widget tersebut tidak akan berubah selama aplikasi berjalan (statis). Namun, pengunaan `const` sebaiknya dihindari jika nilai tersebut dinamis atau bergantung pada input pengguna, karena dapat menyebabkan error ketika kode dijalankan.

## Jelaskan dan bandingkan penggunaan Column dan Row pada Flutter. Berikan contoh implementasi dari masing-masing layout widget ini!
Di Flutter, Column dan Row adalah widget tata letak yang digunakan untuk menyusun widget secara vertikal dan horizontal.
1. Column: menyusun widget anak secara vertikal. Cocok untuk menampilkan konten bertingkat seperti formulir atau daftar.
2. Row: menyusun widget anak secara horizontal. Cocok untuk membuat toolbar, menu, atau menampilkan elemen dalam satu baris.

## Sebutkan apa saja elemen input yang kamu gunakan pada halaman form yang kamu buat pada tugas kali ini. Apakah terdapat elemen input Flutter lain yang tidak kamu gunakan pada tugas ini? Jelaskan!
Element input yang saya gunakan:

TextFormField digunakan untuk menerima input dari pengguna berupa teks. Terdapat beberapa TextFormField pada form ini, masing-masing untuk mengisi data seperti nama produk, harga produk, deskripsi produk, dan jumlah produk yang juga dilengkapi dengan atribut validator = ElevatedButton digunakan untuk menyimpan data yang dimasukkan pada form ketika tombol Save ditekan. Button ini juga digunakan untuk memicu validasi form dan menampilkan hasil input pengguna dalam bentuk dialog.

Element input yang tidak saya gunakan:
- Checkbox: Digunakan untuk memilih satu atau lebih opsi dalam bentuk kotak centang, ya/tidak.
- Radio : Digunakan untuk memilih satu opsi dari beberapa pilihan yang ada
- Switch : Digunakan untuk memilih antara dua keadaan
- DropdownButton : Digunakan untuk memilih satu nilai dari daftar pilihan yang tersedia.
- DatePicker dan TimePicker : Digunakan untuk memilih tanggal atau waktu.
- Slider : Digunakan untuk memilih nilai dalam rentang tertentu menggunakan penggeser, seperti volume atau tingkat pencahayaan.

## Bagaimana cara kamu mengatur tema (theme) dalam aplikasi Flutter agar aplikasi yang dibuat konsisten? Apakah kamu mengimplementasikan tema pada aplikasi yang kamu buat?
Untuk menjaga konsistensi tema dalam aplikasi Flutter yang saya buat, saya menerapkan ThemeData secara global di root aplikasi saya, yaitu pada MaterialApp. Dalam aplikasi Butter and Batter, saya memilih warna dominan coklat agar sesuai dengan tema bakery.

Langkah-langkah yang saya lakukan antara lain:
1. Mengatur Color Scheme: Saya menggunakan ColorScheme.fromSeed dengan warna coklat sebagai warna utama. Warna ini digunakan di berbagai elemen aplikasi, seperti tombol dan latar belakang.
2. Menyesuaikan AppBar: Saya mengatur warna AppBar agar selalu menggunakan warna coklat yang seragam, dengan teks putih untuk kontras yang jelas.
3. Menerapkan Tema untuk Widget Lain: Saya juga menerapkan warna coklat muda untuk komponen seperti Card agar tampilannya menyatu dan terlihat harmonis.
Dengan pendekatan ini, aplikasi saya memiliki nuansa warna yang konsisten, sesuai dengan tema bakery.


## Bagaimana cara kamu menangani navigasi dalam aplikasi dengan banyak halaman pada Flutter?
Navigasi antar halaman (screens) dapat ditangani menggunakan beberapa pendekatan, tergantung pada kompleksitas aplikasi dan kebutuhan navigasi yang kita inginkan. Flutter sendiri menyediakan sistem Navigator yang memungkinkan peralihan antar halaman secara mudah. Kita dapat menggunakan Navigator.push() untuk membuka halaman baru (ditambahin gitu ke stack) dan Navigator.pop() untuk kembali ke halaman sebelumnya (menghapus halaman baru ke stack).

Navigasi dari left drawer:

```
ListTile(
    leading: const Icon(Icons.home_outlined),
    title: const Text('Halaman Utama'),
    // Bagian redirection ke MyHomePage
    onTap: () {
        Navigator.pushReplacement(
            context,
            MaterialPageRoute(
            builder: (context) => MyHomePage(),
            ));
        },
    ),
ListTile(
    leading: const Icon(Icons.cake),
    title: const Text('Tambah Pastry'),
    // Bagian redirection ke MoodEntryFormPage
    onTap: () {
        Navigator.pushReplacement(
            context,
            MaterialPageRoute(
            builder: (context) => const ProductEntryFormPage(),
            ));
        },
    ),
```

Navigasi dari item card:
```
child: InkWell(
    // Aksi ketika kartu ditekan.
    onTap: () {
        // Menampilkan pesan SnackBar saat kartu ditekan.
        ScaffoldMessenger.of(context)
        ..hideCurrentSnackBar()
        ..showSnackBar(
            SnackBar(content: Text("Kamu telah menekan tombol ${item.name}!"))
        );

        if (item.name == "Tambah Mood") {
            Navigator.push(context, MaterialPageRoute(builder: (context) => const ProductEntryFormPage()));
        } 
    },
)
```

Untuk aplikasi dengan banyak bagian, penggunaan Drawer sendiri sangat membantu dalam mengelola navigasi antar halaman. LeftDrawer disini digunakan sebagai menu samping yang memungkinkan pengguna untuk berpindah antara halaman-halaman yang berbeda. Masing-masing ListTile mewakili item menu di Drawer, dan setiap itemnya dapat digunakan untuk menavigasi ke halaman yang berbeda.

# TUGAS INDIVIDU 9
## Jelaskan mengapa kita perlu membuat model untuk melakukan pengambilan ataupun pengiriman data JSON? Apakah akan terjadi error jika kita tidak membuat model terlebih dahulu?
Model diperlukan untuk mengatur struktur data JSON agar lebih terorganisir dan mudah diproses
- Model memetakan data JSON dari server ke objek di aplikasi. Ini memudahkan pengelolaan data.
- Dengan model, kita dapat memvalidasi data yang diterima atau dikirim untuk memastikan kesesuaiannya.
- Model membuat kode lebih modular dan mudah dipahami, sehingga mempermudah debugging dan pengembangan di masa depan.
J
ika tidak menggunakan model, apa yang terjadi?
- Tanpa model, data JSON mungkin tidak terstruktur dengan baik, sehingga sulit diproses. Misalnya, tipe data yang tidak sesuai dapat memicu error saat memproses data.
- Parsing data JSON secara manual menyebabkan kode menjadi panjang dan sulit dipelihara.
## Jelaskan fungsi dari library http yang sudah kamu implementasikan pada tugas ini
Library `http` digunakan untuk:
- Memungkinkan aplikasi Flutter untuk melakukan `GET`, `POST`, `PUT`, dan `DELETE` ke API server.
- Library ini membantu mengelola respons dari server, seperti membaca body, status kode, atau header.
- Memanfaatkan fitur `Future` untuk menangani permintaan dan respons secara asynchronous, sehingga UI tetap responsif.
## Jelaskan fungsi dari CookieRequest dan jelaskan mengapa instance CookieRequest perlu untuk dibagikan ke semua komponen di aplikasi Flutter.
`CookieRequest` adalah kelas untuk menangani komunikasi HTTP yang membutuhkan mekanisme sesi (cookies). Fungsi CookieRequest adalah:
- Memastikan cookies disimpan dan dikirim bersama setiap permintaan ke server, memungkinkan sesi pengguna dipertahankan.
- Digunakan untuk mengirim data otentikasi seperti login, sehingga server dapat mengenali pengguna.
- Karena cookies menyimpan data sesi, CookieRequest memastikan status pengguna seperti login tetap konsisten di seluruh aplikasi.

Mengapa perlu dibagikan ke semua komponen?
Agar setiap komponen di aplikasi memiliki akses ke sesi yang sama. Ini penting untuk fitur seperti login, sehingga setiap bagian aplikasi dapat mengakses data yang sama tanpa harus login ulang.

## Jelaskan mekanisme pengiriman data mulai dari input hingga dapat ditampilkan pada Flutter.
1. Pengguna memasukkan data melalui antarmuka Flutter (form atau input field).
2. Data input dikirim melalui permintaan HTTP menggunakan library seperti http atau CookieRequest. Jika pengiriman menggunakan POST, data dikirim dalam body permintaan.
3. Server (misalnya Django) menerima permintaan, memproses data, dan mengirimkan respons dalam format JSON.
4. Aplikasi Flutter menerima data JSON dari server dan mem-parsing-nya menggunakan model atau langsung membaca data mentah.
5. Data yang sudah diproses diubah menjadi widget Flutter, seperti ListView atau Text, untuk ditampilkan kepada pengguna.

## Jelaskan mekanisme autentikasi dari login, register, hingga logout. Mulai dari input data akun pada Flutter ke Django hingga selesainya proses autentikasi oleh Django dan tampilnya menu pada Flutter.
a. Login
1. Pengguna memasukkan username dan password di aplikasi Flutter.
2. Aplikasi mengirim data ke endpoint login Django menggunakan permintaan POST.
3. Django memvalidasi kredensial:
- Jika valid, Django membuat sesi dan mengembalikan respons dengan cookies sesi.
- Jika tidak valid, Django mengembalikan error.
4. Flutter menyimpan cookies sesi menggunakan CookieRequest untuk digunakan dalam permintaan berikutnya.
5. Setelah berhasil login, Flutter menampilkan menu utama sesuai status pengguna.

b. Register
1. Pengguna memasukkan detail akun baru di aplikasi Flutter.
2. Aplikasi mengirim data ke endpoint register Django menggunakan permintaan POST.
3. Django memvalidasi data:
- Jika valid, Django menyimpan akun baru ke database.
- Jika tidak valid, Django mengembalikan pesan error.
4. Setelah berhasil register, pengguna dapat login menggunakan akun baru.

c. Logout
1. Flutter mengirim permintaan logout ke endpoint Django menggunakan POST.
2. Django menghapus sesi pengguna dan cookies yang terkait.
3. Flutter menghapus cookies lokal di aplikasi menggunakan CookieRequest.
4. Aplikasi mengarahkan pengguna kembali ke halaman login.
Dengan mekanisme ini, autentikasi dilakukan dengan aman menggunakan sesi yang dikelola oleh Django, dan Flutter bertanggung jawab untuk menyimpan serta menggunakan cookies sesi tersebut.
## Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step! (bukan hanya sekadar mengikuti tutorial).

