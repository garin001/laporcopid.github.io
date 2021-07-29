# Desa Lapor Covid

[![N|Solid](https://desalaporcovid.online/desalaporcovid-logo.png)](https://desalaporcovid.online/)

Aplikasi Desa Lapor Covid-19 merupakan sebuah sistem berbasis web yang berfungsi untuk melakukan pencatatan dan pemantauan data warga yang memiliki gejala covid19 ataupun warga yang datang atau pergi dari wilayah terjangkit covid19.

Aplikasi Desa Lapor Covid-19 dirancang untuk dapat digunakan dari level Desa dan nantinya datanya dapat diakses dan dipantau di level kecamatan, kabupaten / kota, dan bahkan bisa sampai level Provinsi.

Penjelasan singkat aplikasi ini sebagai berikut :
  - Warga dapat melaporkan diri sendiri atau warga lain (tetangga) yang mengalami gejala covid19 atau melapor jika anda atau warga lain baru saja datang / akan pergi dari daerah terdampak covid19 (pemudik / perantau).
  - Data laporan warga kemudian akan di verifikasi dan divalidasi oleh posko yang didirikan di setiap wilayah (misal: RT / RW / Puskesmas).
  - Admin di level Desa, Kecamatan, Kab / Kota, dan Provinsi dapat memantau data laporan warga dan memantau kondisi warga terlapor secara cepat.




# Fitur Desa Lapor Covid!

    Tipe Pengguna : Warga 
- [x] Pendaftaran Pengguna Baru
  
- [x] Login Pengguna
  
- [x] Laporan Warga
  
- [x] Notifikasi Status Perkembangan Laporan Warga
  
- [x] Halaman Daftar Laporan Saya
  
- [x] Mengganti Password/ Kata Sandi Sendiri
  
- [x] Logs Semua Aktifitas Pengguna  
  
  
    Tipe Pengguna : POSKO
    
     
- [x] Login Petugas Posko
  
- [x] Mengganti Password/ Kata Sandi Sendiri
  
- [x] Notifikasi Laporan Warga
  
- [x] Validasi Laporan Warga
  
- [x] Merubah Status Laporan Warga
  
- [x] Notifikasi Laporan Warga  
  
- [x] Import/Pindah/Copy Data Dari Laporan Warga Ke Data Posko
  
- [x] Membuat Data Posko (Data Pantauan Warga Pendatang/Pemudik)
  
- [x] Merubah Status Data Posko (Data Posko)
  
- [x] Menambah/ Merubah Data Pantauan Harian
  
- [x] Mencetak PDF Data Posko Per Desa Petugas Posko
  
- [x] Mencetak PDF Detail Data Posko Per Warga Desa Petugas Posko
  
- [x] Logs Semua Aktifitas Pengguna  
  
- [ ] Statistik Data Posko 1 Desa
  
- [ ] Statistik Laporan Warga 1 Desa
  
  
      Tipe Pengguna : ADMIN DESA 
- [x] Login ADMIN DESA
  
- [x] Mengganti Password/ Kata Sandi Sendiri
  
- [x] Notifikasi Laporan Warga
  
- [x] Validasi Laporan Warga
  
- [x] Merubah Status Laporan Warga
  
- [x] Notifikasi Laporan Warga  
  
- [x] Import/Pindah/Copy Data Dari Laporan Warga Ke Data Posko
  
- [x] Membuat Data Posko (Data Pantauan Warga Pendatang/Pemudik)
  
- [x] Merubah Status Data Posko (Data Posko)
  
- [x] Menambah/ Merubah Data Pantauan Harian
  
- [x] Mencetak PDF Data Posko Per Desa Petugas Posko
  
- [x] Mencetak PDF Detail Data Posko Per Warga Desa Petugas Posko
  
- [x] Merubah Status Pengguna dari Desa Yang Sama Menjadi Tipe Posko Atau Admin
  Desa
  
- [x] Merubah Kata Sandi Pengguna dari Desa Yang Sama
  
- [x] Merubah Status Pengguna Dari Desa Yang Sama (AKTIF/DITANGGUHKAN)
  
- [x] Menghapus Data Posko
  
- [x] Menghapus Laporan Warga
  
- [x] Logs Semua Aktifitas Pengguna  
  
- [ ] Statistik Data Posko 1 Desa
  
- [ ] Statistik Laporan Warga 1 Desa
  
  
      Tipe Pengguna : PETUGAS PUSKESMAS 
- [ ] Login PETUGAS PUSKESMAS
  
- [ ] Mengganti Password/ Kata Sandi Sendiri
  
- [ ] Melihat Data Posko 1 Kecamatan
  
- [ ] Menambahkan/ Merubah Data Pantauan Harian Warga 
  

### Tech

Desa Lapor Covid uses a number of open source projects to work properly:

* [PHP](https://www.php.net/) - PHP is a popular general-purpose scripting language that is especially suited to web!
* [Twitter Bootstrap](https://getbootstrap.com/) - The most popular HTML, CSS, and JS library in the world.
* [Yii2 Framework](https://www.yiiframework.com/) - Yii is a fast, secure, and efficient PHP framework.
* [MySQL](https://www.mysql.com/) - MySQL is an open-source relational database management system (RDBMS)


# Petunjuk Instalasi 
## Docker Compose

- `git clone git@github.com:cekdiri/desalaporcovid.git`
- `cd desalaporcovid`
- `docker-compose up`
- Buka shell baru & buat database di mysql container. `docker exec -t desalaporcovid_mysql_1 mysql -uroot -proot -e "create database desalaporcovid"`
- Install dependency `docker exec -t desalaporcovid_php_1 composer install --ignore-platform-reqs` 
- Ubah konfigurai di `config/db-local.php`, sesuaikan nama database dan parameter lainnya. Untuk database hostname gunakan `mysql`.
- Jalankan migrasi & masukan data awal `docker exec -it desalaporcovid_php_1 php yii desalapor/install`. Jawab yes untuk melanjutkan proses.
- Di langkah terakhir, proses install akan membuatkan user baru untuk anda dengan username `superadmin` dan password sesuai tertera di console.
- Aplikasi dapat di akses di http://localhost:8000/

### 




## Manual Installation

Desa Lapor Covid requires The minimum required [PHP](https://www.php.net/) version is PHP 5.4. to run.

Install the dependencies and start the server.

```sh
$ git clone https://github.com/teknosuper/desalaporcovid.git
$ composer install --ignore-platform-reqs
$ php yii migrate
$ php yii import/dependency # or if you like do manually, import sql in data.
```

###Settings

Change `YII_DEBUG` to `true` if you want to enable debug toolbar. default `false`.
Change `YII_ENV` to `dev` if you want to develop on local machine, otherwise set it `prod` when on production mode.

```sh
$ nano web/index.php 
defined('YII_DEBUG') or define('YII_DEBUG', true);
defined('YII_ENV') or define('YII_ENV', 'dev')
```
duplicate `db.php` in config folder to `db-local.php`

```sh
$ nano config/db-local.php
return [
    'class' => 'yii\db\Connection',
    'dsn' => 'mysql:host=localhost;dbname=desalaporcovid',
    'username' => 'root',
    'password' => '',
    'charset' => 'utf8',

    // Schema cache options (for production environment)
    // 'enableSchemaCache' => true,
    // 'schemaCacheDuration' => 3600*24,
    // 'schemaCache' => 'cache',
];

```

### Development

Want to contribute? Great! 

### Todos

 - Write MORE Tests
 - Bug Testing

