## Python-Project-Pacmann---Super-Cashier
## Oleh : Yendri Kilauan Purnama
## Student : #pacmann-peduli-awardee   (Thank You Pacmann)
## Batch 1. (Tgl. 24 Oktober 2023)
&nbsp;
## Background Project

Andi adalah seorang pemilik supermarket besar di salah satu kota di Indonesia. Andi memiliki rencana untuk melakukan perbaikan proses bisnis, yaitu Andi akan membuat sistem kasir yang self-service di supermarket miliknya. Sehingga customer bisa langsung memasukkan item yang dibeli, jumlah item yang dibeli, dan harga item yang dibeli dan fitur yang lain. Sehingga customer yang tidak berada di kota tersebut bisa membeli barang dari supermarket tersebut. Setelah Andi melakukan riset, ternyata Andi memiliki masalah, yaitu Andi membutuhkan Programmer untuk membuatkan fitur - fitur agar bisa sistem kasir self-service di supermarket itu bisa berjalan dengan lancar.

## Deskripsi Task

Akhirnya Andi meminta tolong kepada teman-teman selaku programmer Python untuk membuat program yang menyelesaikan problem tersebut.
Jika ada yang berbelanja, begini journey customer dalam membantu orang yang berbelanja tersebut.
1. Customer membuat ID transaksi customer berikut:

   •	Dengan membuat objek dari class transct_123 = Transaction()
2. Kemudian customer memasukkan nama item, jumlah item, dan harga barang

   •	Masukkan item yang ingin dibeli. add_item([<nama item>, <jumlah item>, <harga per item>])
3. Jika terjadi kesalahan dalam memasukkan nama item atau jumlah item atau harga item tetapi tidak ingin menghapus itemnya, Customer bisa melakukan:
   
    a. Update nama item dengan method: update_item_name(<nama item>, <update nama item>)

    b. Update jumlah item dengan method: update_item_qty(<nama item>, <update jumlah item>)

    c. Update harga item dengan method: update_item_price(<nama item>, <update harga item>)

4. Jika batal membeli item belanja, customer bisa melakukan:

   a. menghapus salah satu item dari nama item dengan method: delet_item(<nama_item>)

   <img width="401" alt="image" src="https://github.com/Yendri-Kilauan/Python-Project-Pacmann---Super-Cashier/assets/134827728/6ede2575-fc9b-4d83-b6b3-44b22300f353">
    
   Ketika menghapus salah satu nama item, maka jumlah item dan harga per item pada baris/list tersebut akan ikut terhapus
   b. Langsung menghapus semua transaksi atau reset transaksi dengan method: reset_transaction()
   
5. Customer sudah selesai dengan berbelanja online nya, tetapi Customer masih ragu apakah harga barang dan nama barang yang diinput sudah benar. Bisa saja customer melakukan kesalahan dalam melakukan input, semisal sudah melakukan input harga barang tetapi lupa untuk input nama barangnya.
Bisa menggunakan method: check_order().
Dengan ketentuan:

   a. Akan mengeluarkan pesan "Pemesanan Sudah Benar"

   b. Akan mengeluarkan pesan "Terdapat kesalahan input data"

   c. Keluarkan output berikut:

   <img width="346" alt="image" src="https://github.com/Yendri-Kilauan/Python-Project-Pacmann---Super-Cashier/assets/134827728/80775edf-4ad4-456a-8ff3-f4115992920d">  
 
6. Setelah melakukan pengecekan, customer bisa menghiting total belanja yang sudah dibeli menggunakan method total_price() dengan ketentuan:

   •	Jika total belanja diatas 200.000 akan mendapat diskon 5%

   •	Jika total belanja diatas 300.000 akan mendapat diskon 8%

   •	Jika total belanja diatas 500.000 akan mendapat diskon 10%

   
   Andi juga memberikan pesan kepada teman-teman kalau diberi kebebasan untuk menambahkan fitur yang lain apabila masih terdapat fitur yang belum tercover dalam sistem 
   tersebut.

&nbsp;
 ## Flowchart

 <img width="454" alt="image" src="https://github.com/Yendri-Kilauan/Python-Project-Pacmann---Super-Cashier/assets/134827728/b16ec01e-8677-4e8f-b069-efb7c7efd402">

&nbsp;
## Code (penjelasan tentang fungsinya)

•	class Transaction: Kelas digunakan untuk menampung method-method yang berisi feature requirements yang dibutuhkan.

•	def __init__(self): fungsi untuk menginisialisasi sebuah atribut data pada class Transaction. Pada fungsi ini terdapat satu parameter self.data_transaksi (dict) yang 
   merupakan variabel untuk menampung data transaksi customer yang masuk.

•	def add_item(self, nama, jumlah, harga): Fungsi untuk memasukkan item yang ingin dibeli. Dengan input nama, jumlah, dan harga peritem.

•	print_item(self): Fungsi untuk mencetak item-item yang masuk dengan memberikan input berupa tabulate.

•	update_item_name(self, nama, nama_baru): Fungsi untuk mengupdate nama item.

•	update_item_qyt(self, nama, jumlah_baru): Fungsi untuk mengupdate jumlah item.

•	def update_item_price(self, nama, harga_baru): Fungsi untuk mengupdate harga per item.

•	def delete_item(self, nama): Fungsi untuk menghapus salah satu item.

•	def reset_transaction(self): Fungsi untuk mereset atau menghapus semua data transaksi yang ada.

•	def check_order(self):Fungsi untuk mengecek apakah data transaksi yang diinput sudah benar atau belum. Pengecekan dilakukan dengan mengecek apakah nama yang diinput 
   bukan string kosong " " dan jumlah serta harga per item harus dalam tipe data integer.

•	def total_price(self): Fungsi untuk menghitung total belanja yang harus dibayar. Dengan memberikan diskon dengan ketentuan:

     o	Jika totalbelanja di atas Rp200.000 maka akan mendapatkan diskon 5%.
     o	Jika totalbelanja di atas Rp300.000 maka akan mendapatkan diskon 8%.
     o	Jika totalbelanja di atas Rp500.000 maka akan mendapatkan diskon 10%.

## Test Code

### Test 1:
Customer ingin menambahkan dua item dengan method add_item() kemudian mencetak list data yang sudah masuk dengan print_item()

<img width="560" alt="image" src="https://github.com/Yendri-Kilauan/Python-Project-Pacmann---Super-Cashier/assets/134827728/6ea55e2e-e498-441c-8e56-b5df3d403771">

<img width="458" alt="image" src="https://github.com/Yendri-Kilauan/Python-Project-Pacmann---Super-Cashier/assets/134827728/2942c6f1-b4c4-4443-b49a-e43dc92b8028">


### Test 2:
Customer salah membeli barang, sehingga ingin menghapus item "Pasta Gigi" dengan method delete_item()

<img width="456" alt="image" src="https://github.com/Yendri-Kilauan/Python-Project-Pacmann---Super-Cashier/assets/134827728/799c5558-545f-486f-8708-be07d11219d2">

### Test 3:
Ternyata customer salah memasukkan semua item yang ingin dibelanjakan, sehingga customer ingin menghapus semua data transaksi yang masuk dengan method reset_transaction()

<img width="453" alt="image" src="https://github.com/Yendri-Kilauan/Python-Project-Pacmann---Super-Cashier/assets/134827728/502b5e08-ef0f-498a-8e6f-9f7ec93f9b9a">

### Test 4:
Customer menginput kembali item-item yang ingin dibeli, kemudian akan menghitung semua total belanja yang harus dibayar dengan method total_price()

<img width="453" alt="image" src="https://github.com/Yendri-Kilauan/Python-Project-Pacmann---Super-Cashier/assets/134827728/9800ac1f-c5e0-4691-8a7a-79d9a40c0f05">

## Conclusion
Sistem kasir self-service ini dibuat untuk mengelola proses transaksi di supermarket agar lebih mudah, efektif dan efisien. Dalam project ini telah dibuat sitem kasir yang dengan beberapa fitur dapat membantu proses transaksi jarak jauh diantaranya dapat menginput item yang ingin dibeli, memperbarui item, menghapus item, membatalkan transaksi dan mengecheck total harga keseluruhan di daftar belanja. Sehingga hal ini membuat customer dapat dengan mudah belanja di supermarket Andi tanpa harus datang langsung ke supermarket.






 

       
 

   


