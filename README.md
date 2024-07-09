# Proyek Akhir APBO Kelompok 4 ServiceAC

## Nama Anggota Kelompok 
- Ramadhani Prasetyo - 4522210009
- Daffa Abraar Sajuti - 4522210040
- Farah Tri Mahardini - 4522210042
- Salwa Khairu Mista - 4522210066
- Nadia Ayu Rahmawati - 4522210077
  
---

### Actor
**Actor yang menggunakan**
1. Customer
2. Admin
3. Teknisi

---

### Use Case
![UseCaseNew](https://github.com/ramadhaniprasety0/Proyek_Akhir_APBO_Kelompok4_ServiceAC/assets/109285562/19761565-7cb5-4226-8079-7b5f30129179)

Pada use case beberapa fungsi yang bisa digunakan tiap actor

1. Customer
- Customer dapat login ke akun customer 
- Customer dapat memilih jasa layanan 
- Customer dapat reservasi layanan
- Customer dapat melihat status layanan 
- Customer dapat melihat laporan perbaikan
- Lalu customer akan melakukan pembayaran
2. Admin 
- Admin dapat login ke akun admin 
- Admin dapat menambah layanan jasa  
- Admin dapat menghapus layanan jasa 
- Admin dapat mengupdate layanan jasa 
- Admin dapat melihat pesanan 
- Admin juga dapat melihat laporan perbaikan 
3. Teknisi 
- Teknisi dapat login ke akun teknisi 
- Teknisi juga dapat melihat pesanan 
- Teknisi dapat menambah status layanan
- Teknisi dapat menghapus status layanan
- Teknisi dapat mengupdate status layanan
- Teknisi akan membuat laporan perbaikan

---

### ERD (Entity Relationship Diagram)
![ERD JASA SERVICE AC](https://github.com/ramadhaniprasety0/Proyek_Akhir_APBO_Kelompok4_ServiceAC/assets/109285562/bae7df77-6c4f-4df5-9a00-43d12ccfa78a)
Terdapat 6 entitas pada ERD Jasa Service MJS seperti:
- Customer
- Admin
- Teknisi
- Order
- Service
- StatusService

Tiap entitas memiliki atribut
- Customer --> (IDcustomer, Nmcustomer, NoTelp, Alamat, Password)
- Admin --> (IDadmin, Nmadmin, NoTelp_admin, Password, IDcustomer)
- Teknisis --> (IDteknisi, Nmteknisi, NoTelpteknisi, Password, IDcustomer)
- Order --> (IDorder, Tglorder, IDcustomer, IDstatus, IDteknisi, IDservice)
- Service --> (IDservice, Nmservice, Harga)
- StatusService --> (IDstatus, keterangan)

Adapun relationship antar entitas seperti:
1. dilayani --> pada entitas customer dan admin
2. ditangani --> pada entitas customer dan teknisi
3. Memesan --> pada entitas customer dan order
4. Mencakup --> pada entitas order dan Admin
5. Mencakup --> pada entitas order dan teknisi
6. Mencakup --> pada entitas order dan service
7. Berstatus --> pada entitas order dan StatusService

Terdapat kardinalitas juga seperti many to one

---

### Sequence Diagram

Aktor
- Customer: Pelanggan yang menggunakan aplikasi untuk memesan layanan perbaikan.
- Teknisi: Teknisi yang melakukan perbaikan.
- Admin: Administrator yang mengelola aplikasi dan sistem.

---

1. Sequence Diagram Customer
![sequenceCust](https://github.com/ramadhaniprasety0/Proyek_Akhir_APBO_Kelompok4_ServiceAC/assets/109285562/17855a11-8f12-4c73-8797-20bfbfa6cf1b)

2. Sequence Diagram Admin
![sequenceAdmin](https://github.com/ramadhaniprasety0/Proyek_Akhir_APBO_Kelompok4_ServiceAC/assets/109285562/9526a5da-e9f8-4cf1-a1c0-c4bde01d7583)

4. Sequence Diagram Teknisi
![sequenceTeknisi](https://github.com/ramadhaniprasety0/Proyek_Akhir_APBO_Kelompok4_ServiceAC/assets/109285562/4828e3e9-599f-4858-a86d-e21f758d1ca0)

Penjelasan:
1. Login
- Customer melakukan login ke aplikasi.
- Aplikasi memverifikasi identitas Customer.
- Customer berhasil login dan masuk ke halaman utama aplikasi.
2. Memilih Jenis Layanan
- Customer memilih jenis layanan perbaikan yang diinginkan.
- Aplikasi menampilkan daftar jenis layanan yang tersedia.
- Customer memilih jenis layanan yang sesuai dengan kebutuhannya.
3. Mengisi Detail Pesanan
- Customer mengisi detail pesanan, seperti nama, alamat, dan deskripsi masalah.
- Aplikasi menampilkan formulir untuk mengisi detail pesanan.
- Customer mengisi formulir dengan lengkap dan benar.
- Customer menekan tombol submit untuk mengirimkan detail pesanan.
4. Konfirmasi Pesanan
- Aplikasi mengirimkan konfirmasi pesanan kepada Customer.
- Customer menerima konfirmasi pesanan melalui email atau SMS.
- Customer dapat memilih untuk melanjutkan pesanan atau membatalkannya.
5. Menangani Pesanan
- Jika Customer memilih untuk melanjutkan pesanan, aplikasi mengirimkan data pesanan kepada Admin.
- Admin meninjau pesanan dan menunjuk Teknisi untuk menangani pesanan tersebut.
- Teknisi menerima notifikasi tentang pesanan yang ditugaskan kepadanya.
6. Melakukan Service
- Teknisi mendatangi lokasi Customer untuk melakukan perbaikan.
- Teknisi melakukan diagnosa dan perbaikan terhadap masalah yang dihadapi Customer.
- Teknisi membuat laporan perbaikan dan mengirimkan laporan tersebut kepada Customer dan Admin.
7. Melihat Laporan Perbaikan
- Customer dapat melihat laporan perbaikan melalui aplikasi.
- Laporan perbaikan berisi informasi tentang masalah yang dihadapi, tindakan yang dilakukan, dan biaya perbaikan.
8. Konfirmasi Pembayaran
- Customer mengkonfirmasi pembayaran atas biaya perbaikan melalui aplikasi.
- Aplikasi menampilkan metode pembayaran yang tersedia.
- Customer memilih metode pembayaran yang sesuai dan menyelesaikan pembayaran.
9. Melakukan Pembayaran
- Customer melakukan pembayaran kepada Teknisi.
- Teknisi menerima pembayaran dari Customer.
- Admin mengkonfirmasi pembayaran

--- 

### Activity Diagram
![ActivityDiagram](https://github.com/ramadhaniprasety0/Proyek_Akhir_APBO_Kelompok4_ServiceAC/assets/109285562/0a6331af-ef80-4816-8bcb-77ac8a9f5038)

Alur Aktivitas:
- Customer Login: Customer melakukan login ke aplikasi MJS.
- Memilih Jenis Layanan: Customer memilih jenis layanan servis AC.
- Mengisi Detail Pemesanan: Customer mengisi detail pemesanan, seperti nama, alamat, dan deskripsi masalah AC.
- Konfirmasi Pesanan: Customer mengkonfirmasi pesanan.
- Admin Menerima Pesanan: Admin menerima pesanan dari Customer.
- Admin Meneruskan Ke Teknisi: Admin menunjuk Teknisi yang sesuai untuk menangani servis AC di lokasi Customer.
- Teknisi Menerima Pesanan: Teknisi menerima notifikasi tentang pesanan yang ditugaskan kepadanya.
- Teknisi Berangkat ke Lokasi: Teknisi berangkat ke lokasi Customer untuk melakukan servis AC.
- Teknisi Melakukan Diagnosa: Teknisi melakukan diagnosa untuk mengetahui penyebab masalah AC.
- Teknisi Melakukan Servis: Teknisi melakukan servis AC sesuai dengan diagnosa.
- Teknisi Membuat Laporan Servis: Teknisi membuat laporan servis yang berisi informasi tentang masalah AC, tindakan yang dilakukan, dan biaya servis.
- Teknisi Mengirim Laporan Servis: Teknisi mengirimkan laporan servis kepada Customer dan Admin.
- Customer Melakukan Pembayaran: Customer melakukan pembayaran atas biaya servis melalui aplikasi.
- Admin Mengkonfirmasi Pembayaran: Admin mengkonfirmasi pembayaran dari Customer.
- Customer Menerima Notifikasi Pembayaran: Customer menerima notifikasi tentang status pembayarannya.
- Customer Melihat Laporan Servis: Customer dapat melihat laporan servis melalui aplikasi.

--- 

### User Interface

#### Interface Customer
**Tampilan Login Customer**
![Page (3)](https://github.com/ramadhaniprasety0/Proyek_Akhir_APBO_Kelompok4_ServiceAC/assets/109285562/0f8a04f8-6f17-43e9-bee0-67c060efb16d)

**Tampilan Daftar Customer**
![Page (4)](https://github.com/ramadhaniprasety0/Proyek_Akhir_APBO_Kelompok4_ServiceAC/assets/109285562/9e9a1812-b704-4198-9ffb-db0dfd139c91)

**Home Page Customer**
![Page (5)](https://github.com/ramadhaniprasety0/Proyek_Akhir_APBO_Kelompok4_ServiceAC/assets/109285562/c4159b0e-70b9-4aed-bf10-533a53e85725)

**Memesan Layanan**
![Page (6)](https://github.com/ramadhaniprasety0/Proyek_Akhir_APBO_Kelompok4_ServiceAC/assets/109285562/e2088b74-454b-415c-9ccf-7bb5e18fbc17)

**Riwayat Pemesanan**
![Page (7)](https://github.com/ramadhaniprasety0/Proyek_Akhir_APBO_Kelompok4_ServiceAC/assets/109285562/b875daaf-c1d2-4923-a372-4fc3bc7ea4cb)

---

#### Interface Admin
**Tampilan Dashboard Admin**
![Page (8)](https://github.com/ramadhaniprasety0/Proyek_Akhir_APBO_Kelompok4_ServiceAC/assets/109285562/70d6a76b-2836-4fdd-bd4e-4d4f9ae260d7)

**Konfirmasi Pesanan**
![Page (9)](https://github.com/ramadhaniprasety0/Proyek_Akhir_APBO_Kelompok4_ServiceAC/assets/109285562/5e112f49-9d5d-4775-9a73-14e24ffd3ad2)

**Pengaturan**
![Page (10)](https://github.com/ramadhaniprasety0/Proyek_Akhir_APBO_Kelompok4_ServiceAC/assets/109285562/63cbb803-dd31-4fc4-a74a-44f9b453edd8)

**Pengaturan Layanan**
![Page (11)](https://github.com/ramadhaniprasety0/Proyek_Akhir_APBO_Kelompok4_ServiceAC/assets/109285562/f65b3ba1-8fd1-494a-963d-622fa2af3f29)

**Pengaturan Staff/Teknisi**
![Page (12)](https://github.com/ramadhaniprasety0/Proyek_Akhir_APBO_Kelompok4_ServiceAC/assets/109285562/81718cf2-ff2f-47b8-b416-d8857245f624)

---

### Interface Teknisi
**Tampilan Dashboard Teknisi**
![Page (13)](https://github.com/ramadhaniprasety0/Proyek_Akhir_APBO_Kelompok4_ServiceAC/assets/109285562/0263d2c7-1338-4fea-9560-21d49f30edf0)

**Mengupdate Status Pesanan**
![Page (14)](https://github.com/ramadhaniprasety0/Proyek_Akhir_APBO_Kelompok4_ServiceAC/assets/109285562/97c89a3b-2c52-408a-81ac-d86c3cefa273)

**Pembayaran**
![Page (15)](https://github.com/ramadhaniprasety0/Proyek_Akhir_APBO_Kelompok4_ServiceAC/assets/109285562/006d785a-e903-4ff3-936c-cda6a2dd2eda)
















