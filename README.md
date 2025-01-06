# Sistem Transaksi Elektronik Sederhana dengan Python
Kode ini merupakan simulasi sederhana dari sistem transaksi toko elektronik.
Tujuan:
- Mempermudah proses pembelian barang.
- Mengelola stok barang secara otomatis.
- Menyediakan struk pembelian untuk pelanggan.

Program terdiri dari 3 kelas utama dan 1 blok program utama:
Kelas Product: Mengelola data barang.
Kelas Transaction: Mengelola proses transaksi.
Kelas View: Menampilkan antarmuka pengguna (menu).
Blok utama: Menjalankan seluruh logika program.

# 1 Kelas Product
Fungsi:
Mengelola data barang seperti nama, harga, dan stok.
Memiliki metode untuk mengurangi stok barang setelah transaksi.
Penjelasan Atribut dan Metode:

Atribut:
name: Nama produk.
price: Harga produk.
stock: Jumlah stok yang tersedia.

Metode:
_init_(self, name, price, stock): Konstruktor untuk menginisialisasi atribut produk.
reduce_stock(self, quantity):
Mengurangi stok barang berdasarkan jumlah yang dibeli.
Jika stok mencukupi, stok akan dikurangi dan mengembalikan True.
Jika stok tidak mencukupi, mengembalikan False.

# 2 Kelas Transaction
Fungsi:
Mengelola proses transaksi:
Menambahkan barang ke keranjang.
Menghitung total harga.
Menampilkan struk pembelian.
Penjelasan Atribut dan Metode:

Atribut:
cart: Daftar barang yang ditambahkan ke keranjang, beserta jumlahnya.
total_price: Total harga dari semua barang dalam keranjang.

Metode:
_init_(self): Konstruktor untuk menginisialisasi keranjang belanja dan total harga.
add_to_cart(self, product, quantity):
Memeriksa apakah stok mencukupi.
Jika stok cukup, barang ditambahkan ke keranjang dan total harga diperbarui.
Jika stok tidak cukup, akan muncul pesan kesalahan.
print_receipt(self):
Menampilkan daftar barang yang dibeli, jumlah, dan total harga dalam format struk.

# 3 kelas View
Fungsi:
Menampilkan daftar barang yang tersedia di toko.
Menerima input dari pengguna, seperti pilihan barang dan jumlah.
Penjelasan Metode:
display_products(products):
Menampilkan daftar barang beserta harga dan stok yang tersedia.
get_user_input():
Meminta input pengguna untuk memilih barang dan jumlah yang ingin dibeli.
Memastikan input valid, jika tidak valid akan memberikan peringatan.

# 4  Blok Program Utama
Fungsi:
Menjalankan seluruh logika program.
Mengatur daftar barang (data awal), menampilkan menu, dan mengelola transaksi.
Penjelasan Alur Program:
Inisialisasi Data Barang:
Daftar barang (nama, harga, dan stok) diinisialisasi.
Menampilkan Menu:
Memanggil metode display_products() untuk menampilkan barang.
Input Pengguna:
Pengguna memilih barang dan jumlah.
Barang ditambahkan ke keranjang menggunakan metode add_to_cart().
Mengulangi Proses:
Program bertanya apakah pengguna ingin membeli barang lain.
Menampilkan Struk:
Setelah selesai, program menampilkan struk pembelian menggunakan metode print_receipt().

# langkah program
Jalankan program.
- Pilih barang yang diinginkan dan jumlahnya.
- Tambahkan beberapa barang ke keranjang.
- Lihat struk pembelian.

#  Kesimpulan
Keunggulan Program:
Sistem sederhana untuk simulasi transaksi.
Pengelolaan stok secara otomatis.
Pengguna mendapatkan struk pembelian.
Pengembangan Lebih Lanjut:
Menambahkan fitur pembayaran.
Menyimpan data transaksi ke file atau database.
Integrasi dengan antarmuka grafis.
