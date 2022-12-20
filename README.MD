**PENGENALAN DATABASES MANAGEMENT SYSTEM**

- DBMS dalah aplikasi yang digunakan untuk me-manege data
- Tanapa menggunkan DBMS , unruk me-manege data , seperti data produk , data cunstomer , data penjualan , kita harus simpan dalam bentuk file ( misal seperti kita mengunakan exile )
- DBMS biasa nya berjalan sebagai aplikasi server yang di gunakan untuk memanage data , kita hanya tingal memberi perintah ke DMBS untuk melakukan proses managemen data nya ,seperti menambah mengubah , menghapus dan mengambil data
- Contoh DBMS yang populer seperti MySQL , PosgreSQL , MongoDB , Oracle , dan lain-lain

**PENGENALAN RELASIONAL DATABASES**

- Ada banyak sekali jenis-jenis DBMS , seperti Relasional Databases , Document Databases, Key-Value Databases , dan lain-lain
  -Namun yang masih populer dan kebanyakan orang gunakan adalah relasional databases
- Relasionala databases cukup mudah di mengerti dan di pelajari karena kit aterbisa menyimpan data dalam bentuk dalam bentuk tabular (table) seperti di Exel dll
- selain itu relasional databases memiliki perintah standar mengunkan SQL sehinga kita mudah ketika ingin berganti-ganti aplikasi databses ( DBMS yang populer seperti MySQL , PosgreSQL , MongoDB , Oracle )

**CARA KERJA DBMS**

- `[Database client]->SQL->[database managemen system]->[data file]`

**DATABASES CLIENT**

- Database Client adalah aplikasi yang di gunakan untuk bercomunikasi dengan DBMS
- Biasa nya DBMS sudah menyediakan databases client sederhana yang bisa kita gunakan untuk berkomunikasi dengan DBMS agar lebih mudah
- Atau kita bisa membuat aplikasi untuk berkomunikasi dengan DBMS , misal membuat aplikasi databases client menggunakan JAVA,PHP atau bahasa pemrograman lain nya

**DATABASE FILE**

- Mayoritas DBMS menyimpan datanya di file , walaupun ada beberapa databases yang lain hanya menyimpan datanya di memory (RAM)
- Namun jangan berfikir file databases yang di simpan berupa file seperti Exel atau CSV (Comma Separated Value), tapi jauh lebih kompleks dari pada itu
  -Database akan di optimasi oleh DBMS agar mempermudah DBMS dalam manajemen data nya , seperti insert , update , delete dan select
- Tiap DBMS biasanya memiliki caranya masing masing untuk mengelolah database file nya, dan kita tidak perlu harus tau, karena yang kita perlu tau hanya cara berkomunikasi ke DBMS

**SQL**

- SQL (Stucktur Query Language)
- Merupakan bahasa yang digunkan untuk berkomunikasi ke DBMS
- SQL adalah bahasa yang muda karena hanya berisi intruksi untuk menyimpan , mengubah , menghapus , atau mengambil data ke di DBMS
- Secara garis besar , semua perintah SQL di Relasional databses itu hampir sama , namun yang membedakan nya adalah improvment pada setip DBMS nya

**MySQL**
-MySQL adalah DBMS Relasional Database OpenSource

**PERINTAH DASAR**

- Menanpilkan nama database yang tersedia di server database anda
  - `show databases`
- Memilih databases
  - `use nama_databases`
  - comand `use` juga bisa di gunakan untuk table
- Menghapus databases
  - `drop database nama_databases`
- Menanpilkan nama Table yang tersedia di database anda
  - `show tables`
- Memilih tabel
  - `use nama_table`
- Menghapus tabel
  - `drop tabels nama_databases`

**TIPE DATA**

- sebelum kita mengisi data pada table database kita harus menentukan tipe data dan nama colum nya
- pada colum tabel satu colum harus memiliki satu tipe data
  - ```
    INT() VARCHAR() VARCHAR() ENUM() VARCHAR() NUMBER() DECIMAL()
    +------------+-----------+--------------+--------------+----------------------------+---------+---------+
    | NomorInduk | NamaDepan | NamaBelakang | JenisKelamin | Alamat | KodePos | Nilai |
    +------------+-----------+--------------+--------------+----------------------------+---------+---------+
    | 1 | reki | desmahaldi | Laki-laki | jalan muaro tanjungampalu | 27511 | 77.00 |
    | 0 | budi | santoso | Laki-laki | jalan gajamada nor 4 | 22233 | 72.80 |
    | 2 | budi | nugroho | Laki-laki | jalan kayaan no gaya | 22111 | 77.00 |
    | 3 | achan | ghui | Perempuan | jalan jompo nomor 5 | 27511 | 71.00 |
    | 4 | mail | ahmad | Perempuan | jalan joko nomor 80 | | 73.00 |
    +------------+-----------+--------------+--------------+----------------------------+---------+---------+
    ```

````
- Biasanya kita mengunagakan tipe data sesuai dengan kebutuhan


**TYPE DATA YANG UMUM DI GUNAKAN DI MYSQL**

- TYPE DATA INTEGER
  - ```
    +------------+-----------+--------------+--------------+-------------------+
    | Type       |length  | Minimum value| Max Value   |Min Value | Max Value  |
    |            |in byte |(Signed)      |  (Signed)   |(Unsigned)| (Unsigned) |
    +------------+--------+--------------+-------------+----------+------------+
    | TINYINT    | 1      | -128         | 127         |  0       | 255        |
    | SMALLINT   | 2      | -32768       | 32767       |  0       | 65535      |
    | MEDIUMINT  | 3      | -8388608     | 8388607     |  0       | 1677215    |
    | INT        | 4      | -2147483648  | 2147483647  |  0       | 4294967295 |
    | BIGINT     | 5      | -922337203685| 922337203685|  0       | 18446744073|
    |            |        |  4775808     | 4775807     |          |  709551615 |
    +------------+--------+--------------+-------------+----------+------------+
    ```
- TYPE DATA FOLOTING POINT
  - ```
    +------------+--------+-----------------+----------------+
    | Type       |length  | Minimum value   | Max Value      |
    |            |in byte |(Signed)         |  (Signed)      |
    +------------+--------+-----------------+----------------+
    | FLOAT      | 4      | -3.402823466E+38|-1.175494351E-38|
    | DOUBLE     | 8      | -1.797693134    |-2.225073855    |
    |            |        |   8623157E+308  |   072014E-308  |
    +------------+--------+--------------+-------------+------
    ```
- TYPE DATA DECIMAL
  - ```
    +-------------+--------+---------+
    | Type        | Minimum| Maximal |
    | Decimal     |        |         |
    +-------------+--------+---------+
    | DECIMAL(5,2)|-999.99 |999.99   |      ( 5 <=jumlah angka dalam digit , 2 <=jumlah angka diblakang koma)
    | DECIMAL(5,0)|-99999  |99999    |
    | DECIMAL(3,1)|-99.9   |999      |
    | DECIMAL(3)  |-999    |999      |
    +------------+--------+-----------
    ```
````
