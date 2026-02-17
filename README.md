# Penyelesaian Permainan Queens Linkedin

# a. Penjelasan Singkat Program

Program ini adalah solver untuk permainan **Queens Puzzle** menggunakan algoritma **Brute Force (Exhaustive Search)**.

Tujuan permainan:
- Tempatkan tepat **1 queen** di setiap baris, kolom, dan region warna
- Queen **tidak boleh bersentuhan** satu sama lain (termasuk diagonal)

Program membaca board dari file `.txt`, memvalidasi input, lalu mencari solusi dengan mencoba **semua kemungkinan penempatan** . Selama proses pencarian, program menampilkan **live update** progress di terminal dengan menunjukan output iterasi tertentu, yang disesuakin dengan ukuran Board.

# b. Requirement & Instalasi

## Requirement
- **Java Development Kit (JDK)** versi 8 atau lebih baru

## Cek Instalasi Java
```bash
java -version
javac -version
```
## Format File Input

File `.txt` berisi board N×N dengan huruf kapital (A-Z), satu baris per baris board:

AAAB
ACBB
CCDB
DDDD

## c. Cara Kompilasi

Jalankan perintah berikut dari **root folder project**:
```bash
javac -d bin src/queen.java
```

Jika berhasil, folder `bin/` akan berisi:
```
bin/
├── queen.class
└── Point.class
```

---

## d. Cara Menjalankan Program

### Menjalankan
Dari **root folder project**, jalankan:
```bash
java -cp bin queen
```

### Alur Penggunaan

**1. Masukkan path file test case:**
```
Masukkan path file: test/"Nama test file".txt
```

**2. Program memvalidasi board:**
```
Memvalidasi Board...
Board Valid! Menunjukan Board

Board:
A A A B
A C B B
C C D B
C D D D
```

**3. Program mencari solusi (dengan live update):**
```
Live Update:
A A A #
A C B B
C C D B
C D D D

Iterasi : 1000
Waktu   : 5 ms
```

**4. Program menampilkan solusi:**
```
Solusi:
A A A #
A # B B
C C D B
C D # D

Waktu   : 8 ms
Iterasi : 1250 kasus
```

**5. Opsi simpan solusi:**
```
Apakah anda ingin Save Jawaban? (Y/n): Y
Nama file output: test/solusi.txt
Solusi disimpan ke: test/solusi.txt
```

### Catatan
- Path file relatif dari **root folder project**
- Untuk board 9×9, waktu pencarian bisa mencapai beberapa menit karena exhaustive search murni (387 juta kombinasi)
- File output berisi board solusi beserta statistik waktu dan iterasi

---

# e. Author

Muhammad Rafi Akbar / 13524125