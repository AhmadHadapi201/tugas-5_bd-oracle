TUGAS 5 BASIS DATA ORACLE


# 1. Membuat Koneksi Oracle Menggunakan PHP
Hal yang pertama dilakukan untuk membuat program Oracle menggunakan PHP 
adalah dengan mengkoneksikan Oracle ke PHP.

    <?php   $user="dapi_201";   $pass="201";   $database="LOCALHOST/XE";   $con = oci_connect($user, $pass, $database);   if($con){    echo "Koneksi Sukses";  }   else{    $err = oci_error();    echo "Gagal". $err['text'];   } ?>

Jika Koneksi Berhasil, silahkan buka Browser web kalian dengan memasukkan 
link 'Localhost/Oracle/koneksi.php'.
**Catatan : Link Sesuai dengan folder dan Nama file yang sudah kalian simpah**
    
![Screenshot (12)](https://user-images.githubusercontent.com/95658885/144950848-8339b7de-4e4e-47e5-a73f-0c10a22931b8.png)

    
# 2. Membuat view
Selanjutnya adalah untuk membuat view. Sebenarnya saya membuat view lebih dari 5, Namun agar lebih mudah
disini hanya saya tampilkan 2 dari view yang sudah saya buat

    CREATE OR REPLACE view toko_jaksel as SELECT * FROM toko_1001 WHERE alamat = 'Jakarta Selatan'; 
    CREATE OR REPLACE view kap_gudang as SELECT * FROM gudang_1001 WHERE kapasitas = '70.000 pcs';   
    
Jika sudah dibuat maka akan coba kita tampilkan Hasil dari
view yang sudah kita buat dengan Query View tersebut
   
![Screenshot (17) - Copy](https://user-images.githubusercontent.com/95658885/144948726-01453bb6-c2b9-4581-bf0f-980a80ad4ec6.png)
![Screenshot (16)](https://user-images.githubusercontent.com/95658885/144948960-3e3f00ab-4893-4cf4-8c21-faa8bd72d96b.png)

# 3. Membuat Halaman Home/Beranda
Selanjutnya kita akan coba menampilkan view yang sudah dibuat kedalam project PHP
menggunakan sublime Text 3. Berikut tampilannya!
        
![Screenshot (7)](https://user-images.githubusercontent.com/95658885/144949190-a223e65e-a4ee-4f8a-8888-a2a3c4320c81.png)

# 4. Membuat Tabel Master
Setelah sukses koneksi, membuat view dan menjalankan di PHP maka kali ini kita 
akan membuat Tabel Master / Data Tabel dari Database yang sudah kita buat di Oracle.

![Screenshot (8)](https://user-images.githubusercontent.com/95658885/144949510-33a7d498-9fe1-4bbf-8dec-ab42f168118c.png)

![Screenshot (9)](https://user-images.githubusercontent.com/95658885/144949541-7036fc77-4194-4b77-a795-74ee11edc425.png)

![Screenshot (10)](https://user-images.githubusercontent.com/95658885/144949544-b90f5f02-d332-412a-b20d-20ce94c8d991.png)

![Screenshot (11)](https://user-images.githubusercontent.com/95658885/144949546-abe583dc-48a1-4a26-b4d8-18aa6a5bbe59.png)

