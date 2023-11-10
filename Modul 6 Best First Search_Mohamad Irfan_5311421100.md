#### Mohamad Irfan 5311421100

<center><h1>MODUL 6 PERMAINAN TIC TAC TOE</h1></center>

Pada modul 6 tentang Permaian TIC TAC TOE ini memiliki tujuan untuk Meningkatkan pemahaman mahasiswa terhadap code permainan tic tac toe. Selain itu, modul 6 
memberikan pengetahuan tentang Object Oriented Programming menggunakan bahasa pemrograman Java terutama Java Swing dan Japplet. Dalam praktikum Best First Search ini, mahasiswa diminta untuk membuat implementasi permainan Tic-Tac-Toe menggunakan bahasa pemrograman Java. Untuk melaksanakan praktikum ini, buatlah sebuah folder dengan nama "Tic Tac Toe". Pada folder tersebut, kita buat enam file dengan nama State.Java, Seed.Java, GameState.Java, Cell.Java, Board.Java, dan GameMain.Java seperti yang tercantum di bawah ini:

##### Enumaration State (GameState.Java)

![alt text](https://github.com/mhdirfan17/ARTIFICIAL-INTELLIGENCE-AND-APPLICATION/blob/main/6%20GameState.png)

Kode tersebut mendefinisikan sebuah enumerasi (enum) dalam bahasa pemrograman Java untuk merepresentasikan berbagai kondisi atau status dalam permainan Tic Tac Toe. Enumerasi ini disebut GameState, dan memiliki empat nilai yang mungkin:

1. `PLAYING`: Menunjukkan bahwa permainan masih berlangsung, dan belum ada pemenang atau seri (draw).

2. `DRAW`: Menunjukkan bahwa permainan berakhir dengan hasil seri, artinya tidak ada pemenang.

3. `CROSS_WON`: Menunjukkan bahwa pemain yang menggunakan simbol "CROSS" (X) telah memenangkan permainan.

4. `NOUGHT_WON`: Menunjukkan bahwa pemain yang menggunakan simbol "NOUGHT" (O) telah memenangkan permainan.

Dengan menggunakan enum ini, kode permainan Tic Tac Toe dapat dengan mudah merujuk dan memeriksa status permainan saat ini.

##### Enumaration State (Seed.Java)

![alt text](https://github.com/mhdirfan17/ARTIFICIAL-INTELLIGENCE-AND-APPLICATION/blob/main/6%20Seed.png)

Kode tersebut mendefinisikan sebuah enumerasi (enum) dalam bahasa pemrograman Java untuk merepresentasikan berbagai "seed" atau isi sel dalam permainan Tic Tac Toe. Enumerasi ini disebut Seed, dan memiliki tiga nilai yang mungkin:

1. `EMPTY`: Menunjukkan bahwa sebuah sel dalam papan permainan Tic Tac Toe masih kosong atau belum diisi oleh simbol apapun.

2. `CROSS`: Menunjukkan bahwa sebuah sel dalam papan permainan diisi dengan simbol "CROSS" (X).

3. `NOUGHT`: Menunjukkan bahwa sebuah sel dalam papan permainan diisi dengan simbol "NOUGHT" (O).

Dengan menggunakan enum Seed ini, kode permainan dapat dengan mudah mengidentifikasi dan memanipulasi isi sel pada papan permainan berdasarkan simbol-simbol yang didefinisikan.

##### Enumaration State (State.Java)

![alt text](https://github.com/mhdirfan17/ARTIFICIAL-INTELLIGENCE-AND-APPLICATION/blob/main/6%20State.png)

Kode tersebut mendefinisikan sebuah enumerasi (enum) dalam bahasa pemrograman Java untuk merepresentasikan berbagai kondisi atau status dalam permainan Tic Tac Toe. Enumerasi ini disebut State, dan memiliki empat nilai yang mungkin:

1. `PLAYING`: Menunjukkan bahwa permainan masih berlangsung, dan belum ada pemenang atau seri (draw).

2. `DRAW`: Menunjukkan bahwa permainan berakhir dengan hasil seri, artinya tidak ada pemenang.

3. `CROSS_WON`: Menunjukkan bahwa pemain yang menggunakan simbol "CROSS" (X) telah memenangkan permainan.

4. `NOUGHT_WON`: Menunjukkan bahwa pemain yang menggunakan simbol "NOUGHT" (O) telah memenangkan permainan.

Dengan menggunakan enum ini, kode permainan Tic Tac Toe dapat dengan mudah merujuk dan memeriksa status permainan saat ini. Ini memungkinkan programmer untuk dengan jelas mengidentifikasi dan memanipulasi kondisi permainan tanpa perlu menggunakan angka atau string yang sulit dipahami.

##### Class Cell.java

![alt text](https://github.com/mhdirfan17/ARTIFICIAL-INTELLIGENCE-AND-APPLICATION/blob/main/6%20Class%20Cell%201.png)

![alt text](https://github.com/mhdirfan17/ARTIFICIAL-INTELLIGENCE-AND-APPLICATION/blob/main/6%20Class%20Cell%202.png)

Kode tersebut merupakan implementasi kelas `Cell` dalam konteks permainan Tic Tac Toe. Kelas ini merepresentasikan sebuah sel atau kotak pada papan permainan dan menyimpan informasi tentang isi sel tersebut.

Berikut adalah penjelasan singkat dari beberapa bagian kode tersebut:

1. **Variabel dan Konstruktor:**
   - `Seed content`: Merepresentasikan isi dari sel tersebut, yang dapat berupa `Seed.EMPTY` (kosong), `Seed.CROSS` (X), atau `Seed.NOUGHT` (O).
   - `int row, col`: Menyimpan posisi baris dan kolom dari sel ini.
   - Konstruktor `public Cell(int row, int col)`: Inisialisasi sel dengan baris dan kolom yang ditentukan, dan kemudian memanggil metode `clear()` untuk mengosongkan isi sel.

2. **Metode `clear()`:**
   - Mengosongkan isi sel dengan mengatur `content` menjadi `Seed.EMPTY`.

3. **Metode `paint(Graphics g)`:**
   - Digunakan untuk menggambar sel pada canvas grafis menggunakan objek `Graphics`.
   - Jika isi sel adalah `Seed.CROSS`, garis diagonal merah digambar.
   - Jika isi sel adalah `Seed.NOUGHT`, lingkaran biru digambar.
   - Pengaturan warna dan ukuran simbol (X atau O) ditentukan oleh konstanta yang mungkin didefinisikan di kelas `GameMain` seperti `SYMBOL_STROKE_WIDTH`, `CELL_SIZE`, `CELL_PADDING`, dan `SYMBOL_SIZE`.

Ini adalah bagian dari implementasi dari permainan Tic Tac Toe yang menggunakan representasi grafis untuk menampilkan papan permainan dan simbol-simbolnya.

##### Class Board.java

![alt text](https://github.com/mhdirfan17/ARTIFICIAL-INTELLIGENCE-AND-APPLICATION/blob/main/6%20Class%20Board%201.png)

![alt text](https://github.com/mhdirfan17/ARTIFICIAL-INTELLIGENCE-AND-APPLICATION/blob/main/6%20Class%20Board%202.png)

![alt text](https://github.com/mhdirfan17/ARTIFICIAL-INTELLIGENCE-AND-APPLICATION/blob/main/6%20Class%20Board%203.png)

![alt text](https://github.com/mhdirfan17/ARTIFICIAL-INTELLIGENCE-AND-APPLICATION/blob/main/6%20Class%20Board%204.png)

Kode tersebut adalah implementasi kelas `Board` dalam konteks permainan Tic Tac Toe. Kelas ini bertanggung jawab untuk merepresentasikan papan permainan, mengelola sel-sel di dalamnya, serta menyediakan metode untuk menginisialisasi, memeriksa kemenangan, dan menggambar papan permainan.

Berikut adalah penjelasan singkat dari beberapa bagian kode tersebut:

1. **Variabel:**
   - `Cell[][] cells`: Matriks dua dimensi dari objek `Cell` yang merepresentasikan sel-sel pada papan permainan.

2. **Konstruktor:**
   - `public Board()`: Inisialisasi papan permainan dengan membuat seluruh sel dan menyimpannya dalam matriks `cells`.

3. **Metode `init()`:**
   - Menginisialisasi ulang papan permainan dengan mengosongkan isi semua sel menggunakan metode `clear()` dari kelas `Cell`.

4. **Metode `isDraw()`:**
   - Memeriksa apakah permainan berakhir seri (draw), yaitu ketika tidak ada sel kosong di papan.

5. **Metode `hasWon(Seed seed, int seedRow, int seedCol)`:**
   - Memeriksa apakah pemain dengan simbol tertentu (`seed`) telah memenangkan permainan setelah menempatkan simbolnya di koordinat `(seedRow, seedCol)`. Ini dilakukan dengan memeriksa apakah ada baris, kolom, atau diagonal yang terdiri dari tiga simbol yang sama.

6. **Metode `paint(Graphics g)`:**
   - Menggambar papan permainan dan seluruh selnya menggunakan objek `Graphics`.
   - Menggunakan warna abu-abu untuk menggambar garis-garis grid pada papan permainan.
   - Memanggil metode `paint(g)` pada setiap sel untuk menggambar simbol (X atau O) di atasnya.

Kelas ini berperan penting dalam mengatur logika dan tampilan papan permainan Tic Tac Toe.

##### Class GameMain.java

![alt text](https://github.com/mhdirfan17/ARTIFICIAL-INTELLIGENCE-AND-APPLICATION/blob/main/C%20GameMain%20(11).png)

![alt text](https://github.com/mhdirfan17/ARTIFICIAL-INTELLIGENCE-AND-APPLICATION/blob/main/C%20GameMain%20(10).png)

![alt text](https://github.com/mhdirfan17/ARTIFICIAL-INTELLIGENCE-AND-APPLICATION/blob/main/C%20GameMain%20(9).png)

![alt text](https://github.com/mhdirfan17/ARTIFICIAL-INTELLIGENCE-AND-APPLICATION/blob/main/C%20GameMain%20(8).png)

![alt text](https://github.com/mhdirfan17/ARTIFICIAL-INTELLIGENCE-AND-APPLICATION/blob/main/C%20GameMain%20(7).png)

![alt text](https://github.com/mhdirfan17/ARTIFICIAL-INTELLIGENCE-AND-APPLICATION/blob/main/C%20GameMain%20(6).png)

Kode yang diberikan adalah implementasi utama dari permainan Tic Tac Toe menggunakan Java dan Swing untuk antarmuka grafis. Berikut adalah penjelasan singkat untuk beberapa bagian utama dari kode tersebut:

1. **Variabel dan Konstanta:**
   - `ROWS` dan `COLS`: Konstanta yang menentukan ukuran papan permainan Tic Tac Toe.
   - `CELL_SIZE`, `CANVAS_WIDTH`, dan `CANVAS_HEIGHT`: Konstanta yang menentukan ukuran sel dan dimensi papan permainan.
   - `GRID_WIDTH` dan `GRID_WIDTH_HALF`: Konstanta yang menentukan lebar grid di papan permainan.
   - `CELL_PADDING`, `SYMBOL_SIZE`, dan `SYMBOL_STROKE_WIDTH`: Konstanta yang menentukan padding sel, ukuran simbol, dan lebar stroke untuk menggambar simbol.

2. **Variabel Kelas:**
   - `board`: Objek dari kelas `Board` yang merepresentasikan papan permainan.
   - `currentState`: Enum dari kelas `GameState` yang menyimpan status permainan saat ini (PLAYING, DRAW, CROSS_WON, NOUGHT_WON).
   - `currentPlayer`: Enum dari kelas `Seed` yang menunjukkan pemain saat ini (CROSS atau NOUGHT).
   - `statusBar`: JLabel untuk menampilkan pesan status di bagian bawah antarmuka grafis.

3. **Metode Konstruktor (`GameMain()`):**
   - Membuat objek `MouseAdapter` untuk menangani klik mouse dan melakukan tindakan yang sesuai berdasarkan koordinat klik.
   - Menyiapkan status bar (JLabel) untuk menampilkan pesan status.
   - Mengatur layout dan ukuran panel.
   - Membuat objek `Board` untuk merepresentasikan papan permainan.
   - Memanggil metode `initGame()` untuk menginisialisasi permainan.

4. **Metode `initGame()`:**
   - Mengosongkan seluruh sel di papan permainan dan menginisialisasi variabel-variabel permainan.

5. **Metode `updateGame(Seed theSeed, int row, int col)`:**
   - Memperbarui status permainan berdasarkan langkah terakhir yang diambil oleh pemain.
   - Memeriksa apakah pemain yang mengambil langkah tersebut telah memenangkan permainan atau apakah permainan berakhir seri.

6. **Metode `paintComponent(Graphics g)`:**
   - Menggambar papan permainan dan elemen-elemen grafis lainnya.
   - Memanggil metode `paint()` pada objek `Board` untuk menggambar sel-sel pada papan permainan.
   - Menampilkan pesan status di status bar berdasarkan status permainan saat ini.

7. **Metode `main(String[] args)`:**
   - Metode utama yang memulai aplikasi.
   - Membuat objek `JFrame` untuk menampilkan antarmuka grafis.
   - Menetapkan panel utama (`GameMain`) sebagai konten frame.
   - Mengatur atribut frame dan menampilkan frame.

Kode tersebut merupakan implementasi lengkap dari permainan Tic Tac Toe dengan antarmuka grafis menggunakan Java dan Swing.

Hasil Output dari code program diatas sebagai berikut :

![alt text](https://github.com/mhdirfan17/ARTIFICIAL-INTELLIGENCE-AND-APPLICATION/blob/main/6%20Output%20TicTacToe.png)
