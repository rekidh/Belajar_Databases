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
-

```
   INT()        VARCHAR()   VARCHAR()      ENUM()          VARCHAR()                 NUMBER()  DECIMAL()
+------------+-----------+--------------+--------------+----------------------------+---------+---------+
| NomorInduk | NamaDepan | NamaBelakang | JenisKelamin | Alamat                     | KodePos | Nilai   |
+------------+-----------+--------------+--------------+----------------------------+---------+---------+
|          1 | reki      | desmahaldi   | Laki-laki    | jalan muaro tanjungampalu  | 27511   | 77.00   |
|          0 | budi      | santoso      | Laki-laki    | jalan gajamada nor 4       | 22233   | 72.80   |
|          2 | budi      | nugroho      | Laki-laki    | jalan kayaan no gaya       | 22111   | 77.00   |
|          3 | achan     | ghui         | Perempuan    | jalan jompo nomor 5        | 27511   | 71.00   |
|          4 | mail      | ahmad        | Perempuan    | jalan joko nomor 80        |         | 73.00   |
+------------+-----------+--------------+--------------+----------------------------+---------+---------+
```

- Biasanya kita mengunagakan tipe data sesusi dengan kebutuhan
