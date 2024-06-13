## Materi: Menganalisis Perancangan dengan Activity Diagram, Sequence Diagram, dan Class Diagram

### Matakuliah: Perancangan Sistem Informasi

#### Pendahuluan
Perancangan sistem informasi merupakan tahap penting dalam pengembangan sistem informasi yang efektif dan efisien. Pada tahap ini, kita akan menggunakan tiga diagram utama: Activity Diagram, Sequence Diagram, dan Class Diagram. Ketiga diagram ini membantu kita memahami alur kerja, interaksi antar komponen, dan struktur data dari sistem yang akan dikembangkan.

#### Tujuan
1. Memahami konsep dasar Activity Diagram, Sequence Diagram, dan Class Diagram.
2. Mampu membuat dan menganalisis ketiga diagram tersebut.
3. Menerapkan konsep perancangan ini dalam studi kasus toko online PT Aneka Busa.

### 1. Activity Diagram
Activity Diagram menggambarkan alur kerja atau aktivitas dari sebuah sistem. Diagram ini membantu dalam memodelkan proses bisnis dan alur kerja dalam sistem.

#### Elemen Activity Diagram:
- **Aktivitas (Activity):** Menunjukkan tindakan atau langkah dalam proses.
- **Transisi (Transition):** Menunjukkan perpindahan dari satu aktivitas ke aktivitas lainnya.
- **Start Point:** Menandakan awal dari alur aktivitas.
- **End Point:** Menandakan akhir dari alur aktivitas.
- **Fork dan Join:** Menandakan aktivitas paralel.

#### Contoh Activity Diagram untuk PT Aneka Busa
Misalkan kita ingin memodelkan proses pemesanan produk di toko online PT Aneka Busa.

![Activity Diagram](https://www.visual-paradigm.com/servlet/vp/template/diagram/vp_diagram_thumbnail.jsp?tpv=22_1_6_1_2_activity-diagram-thumbnail&style=b.png)

1. **Start**: Pelanggan mengakses situs web toko online.
2. **Browse Products**: Pelanggan mencari produk (busa, sofa, alas gosok, karpet busa).
3. **Select Product**: Pelanggan memilih produk yang ingin dibeli.
4. **Add to Cart**: Pelanggan menambahkan produk ke keranjang belanja.
5. **View Cart**: Pelanggan melihat isi keranjang belanja.
6. **Checkout**: Pelanggan memulai proses checkout.
7. **Enter Shipping Information**: Pelanggan memasukkan informasi pengiriman.
8. **Make Payment**: Pelanggan melakukan pembayaran.
9. **Order Confirmation**: Sistem mengonfirmasi pesanan.
10. **End**

### 2. Sequence Diagram
Sequence Diagram menggambarkan interaksi antara objek dalam sistem dalam urutan kronologis. Diagram ini menunjukkan pesan yang dikirim antar objek dalam suatu skenario tertentu.

#### Elemen Sequence Diagram:
- **Lifeline:** Representasi partisipan dalam interaksi.
- **Message:** Komunikasi antara lifeline.
- **Activation:** Periode ketika sebuah objek sedang melakukan atau menunggu tindakan.

#### Contoh Sequence Diagram untuk Proses Pemesanan
Misalkan kita ingin memodelkan interaksi saat pelanggan melakukan pemesanan.

![Sequence Diagram](https://www.visual-paradigm.com/servlet/vp/template/diagram/vp_diagram_thumbnail.jsp?tpv=22_1_7_1_1_sequence-diagram-thumbnail&style=b.png)

1. **Pelanggan -> Web Toko**: Memilih produk dan menambahkannya ke keranjang belanja.
2. **Web Toko -> Pelanggan**: Menampilkan isi keranjang belanja.
3. **Pelanggan -> Web Toko**: Memulai proses checkout.
4. **Web Toko -> Pelanggan**: Mengirim formulir informasi pengiriman.
5. **Pelanggan -> Web Toko**: Mengirim informasi pengiriman.
6. **Web Toko -> Pelanggan**: Menampilkan opsi pembayaran.
7. **Pelanggan -> Web Toko**: Memilih metode pembayaran dan mengirim detail pembayaran.
8. **Web Toko -> Sistem Pembayaran**: Mengirim informasi pembayaran.
9. **Sistem Pembayaran -> Web Toko**: Mengonfirmasi pembayaran.
10. **Web Toko -> Pelanggan**: Mengirim konfirmasi pesanan.

### 3. Class Diagram
Class Diagram menggambarkan struktur statis dari sistem dengan menunjukkan kelas, atribut, metode, dan hubungan antar kelas.

#### Elemen Class Diagram:
- **Class:** Menunjukkan entitas dalam sistem.
- **Attribute:** Menunjukkan data yang dimiliki oleh sebuah kelas.
- **Operation:** Menunjukkan fungsi atau metode yang dimiliki oleh kelas.
- **Association:** Menunjukkan hubungan antara kelas.

#### Contoh Class Diagram untuk Toko Online
Berikut adalah contoh Class Diagram untuk sistem toko online PT Aneka Busa:

![Class Diagram](https://www.visual-paradigm.com/servlet/vp/template/diagram/vp_diagram_thumbnail.jsp?tpv=22_1_5_1_1_class-diagram-thumbnail&style=b.png)

- **Class Pelanggan**
  - Attributes: idPelanggan, nama, alamat, email, telepon
  - Methods: tambahPelanggan(), updatePelanggan(), deletePelanggan()

- **Class Produk**
  - Attributes: idProduk, namaProduk, kategori, harga, stok
  - Methods: tambahProduk(), updateProduk(), deleteProduk()

- **Class Pesanan**
  - Attributes: idPesanan, tanggalPesanan, statusPesanan, idPelanggan
  - Methods: buatPesanan(), updatePesanan(), batalkanPesanan()

- **Class Pembayaran**
  - Attributes: idPembayaran, idPesanan, metodePembayaran, tanggalPembayaran, jumlah
  - Methods: prosesPembayaran(), konfirmasiPembayaran()

- **Class Keranjang**
  - Attributes: idKeranjang, idPelanggan, idProduk, jumlah
  - Methods: tambahKeKeranjang(), hapusDariKeranjang(), updateJumlah()

### Kesimpulan
Dalam perancangan sistem informasi, Activity Diagram, Sequence Diagram, dan Class Diagram sangat penting untuk memodelkan alur kerja, interaksi antar komponen, dan struktur data sistem. Melalui studi kasus toko online PT Aneka Busa, kita telah mempelajari bagaimana menerapkan ketiga diagram ini untuk memodelkan proses pemesanan produk di toko online. Dengan memahami dan menerapkan diagram-diagram ini, kita dapat merancang sistem yang lebih terstruktur, efisien, dan mudah dipahami.