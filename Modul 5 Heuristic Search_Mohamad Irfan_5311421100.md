#### MOHAMAD IRFAN 53114211000

<center><h1>MODUL 5 TEKNIK HEURISTIC SEARCH</h1></center>
Teknik pencarian heuristik adalah metode pencarian dalam kecerdasan buatan di mana agen atau program mencari solusi untuk masalah dengan menggunakan informasi tambahan yang disebut heuristik. Heuristik adalah aturan atau pedoman yang mengarahkan pencarian menuju solusi yang mungkin tanpa mengeksplorasi semua kemungkinan. Dalam konteks teknik heuristic search, agen menggunakan heuristik untuk mengambil keputusan tentang langkah apa yang harus diambil selanjutnya. Konsep ini berlawanan dengan pencarian "blind" atau "uninformed search," di mana agen tidak memiliki pengetahuan khusus tentang lingkungan atau masalah yang sedang dihadapinya.

#### TUGAS

1.	Pelajari class EightPuzzleSearch, EightPuzzleSpace, dan Node.

#### Kelas Eight Puzzle Search

- EightPuzzleSearch class memiliki tanggung jawab dalam melakukan pencarian solusi untuk permasalahan 8-puzzle.
- Open vector digunakan untuk menampung simpul-simpul yang masih harus dieksplorasi, sedangkan closed vector digunakan untuk menyimpan simpul-simpul yang telah dieksplorasi.
- Kelas ini dilengkapi dengan dua metode heuristik, yaitu h1Cost() dan h2Cost(), yang digunakan untuk menghitung biaya simpul berdasarkan heuristik yang berbeda.
- Metode hCost(Node node) digunakan untuk memilih heuristik yang akan digunakan, baik itu h1 atau h2.

Metode

- Fungsi `getBestNode(Vector nodes)` menghasilkan simpul dengan biaya terendah dari kumpulan simpul yang diberikan.
- Fungsi `getPreviousCost(Node node)` mengembalikan biaya simpul jika simpul tersebut ada dalam daftar open atau closed.
- Fungsi `printPath(Vector path)` mencetak jalur dari akar ke tujuan.
- Fungsi `run()` adalah fungsi utama yang mengeksekusi algoritma pencarian.

#### Kelas Eight Puzzle Space

- Kelas ini menentukan keadaan awal dan tujuan dalam permasalahan 8-puzzle, serta menghasilkan simpul-simpul yang akan digunakan selanjutnya.
- Fungsi `getRoot()` mengembalikan keadaan awal dalam bentuk simpul.
- Fungsi `getGoal()` mengembalikan keadaan tujuan sebagai simpul.
- Fungsi `getSuccessors(Node parent)` menghasilkan simpul-simpul penerus dengan mempertimbangkan perpindahan ubin kosong.
- Fungsi `transformState()` digunakan untuk menciptakan simpul baru dengan pertukaran posisi dua ubin dalam keadaan.

#### Kelas Node

- Kelas Node merupakan representasi dari suatu simpul atau kondisi di dalam ruang pencarian, terutama dalam konteks penyelesaian permasalahan 8-puzzle.
- Bidang `state` mengandung sebuah larik yang terdiri dari 9 bilangan bulat yang memvisualisasikan kondisi atau letak ubin-ubin dalam papan permainan.
- Bidang `cost` merupakan nilai biaya yang terkait dengan mencapai simpul ini.
- Bidang `parent` berupa referensi yang mengarah ke simpul induk dalam struktur pohon pencarian.
- Bidang `successors` adalah vektor yang memuat simpul-simpul anak yang terhubung dengan simpul ini.

Metode

- Konstruktor `Node(int s[], Node parent)` digunakan untuk memulai simpul dengan suatu keadaan tertentu dan simpul induk.
- Metode `toString()` menghasilkan representasi string dari keadaan dalam simpul.
- Metode `equals(Object node)` membandingkan dua simpul untuk memeriksa apakah keadaan mereka sama.
- Metode `getPath(Vector<Node> v)` mengembalikan jalur dari simpul akar hingga simpul saat ini dalam bentuk vektor.
- Metode `getPath()` menghasilkan jalur tersebut dalam bentuk vektor yang baru.

#### Hasil Praktikum

![alt text](https://github.com/MFikriHidayat/Fikri/blob/main/Jobsheet%205%20Nomor%201.png)

- Keadaan Semula : Puzzle board terdiri dari sembilan ubin yang disusun dalam bentuk matriks 3x3. Ubin dengan angka 0 mewakili ubin kosong yang dapat dipindahkan ke atas, bawah, kiri, atau kanan untuk mencapai keadaan tujuan.
- Langkah 1 : Pada langkah awal, ubin kosong dipindahkan dari koordinat (3,3) ke koordinat (2,3).
- Langkah 2 : Selanjutnya, ubin kosong dipindahkan dari koordinat (2,3) ke koordinat (2,2).
- Langkah 3 : Ubin kosong dipindahkan dari koordinat (2,2) ke koordinat (1,2).
- Langkah 4 : Pada tahap akhir, ubin kosong dipindahkan dari koordinat (1,2) ke koordinat (1,1).

Dengan demikian, masalah 8-puzzle berhasil dipecahkan dari keadaan awal ke keadaan tujuan dalam lima langkah. Setiap pergerakan ubin kosong dalam setiap langkah membawa keadaan lebih dekat ke tujuan, dan akhirnya mencapai keadaan tujuan yang benar.

2.	Ubahlah initial dan goal state dari program di atas sehingga bentuk initial dan goal statenya Gambar 8. Kemudian tentukan langkah-langkah mana saja sehingga puzzlenya mencapai goal state. Analisa dan bedakan dengan solusi pada point 1. 

#### Hasil Praktikum

![alt text](https://github.com/MFikriHidayat/Fikri/blob/main/Jobsheet%205%20Nomor%202.png)

- Langkah 1 : Memindahkan ubin kosong dari (3,3) ke (3,2)
- Langkah 2 : Memindahkan ubin kosong dari (3,2) ke (3,1)
- Langkah 3 : Memindahkan ubin kosong dari (3,1) ke (2,1)
- Langkah 4 : Memindahkan ubin kosong dari (2,1) ke (2,2)
- Langkah 5 : Memindahkan ubin kosong dari (2,2) ke (1,2)
- Langkah 6 : Memindahkan ubin kosong dari (1,2) ke (1,3)
- Langkah 7 : Memindahkan ubin kosong dari (1,3) ke (2,3)
- Langkah 8 : Memindahkan ubin kosong dari (2,3) ke (2,2)
- Langkah 9 : Memindahkan ubin kosong dari (2,2) ke (2,1)
- Langkah 10 : Memindahkan ubin kosong dari (2,1) ke (1,1)
- Langkah 11 : Memindahkan ubin kosong dari (1,1) ke (1,2)
- Langkah 12 : Memindahkan ubin kosong dari (1,2) ke (1,3)
- Langkah 13 : Memindahkan ubin kosong dari (1,3) ke (2,3)
- Langkah 14 : Memindahkan ubin kosong dari (2,3) ke (2,2)
- Langkah 15 : Memindahkan ubin kosong dari (2,2) ke (2,1)
- Langkah 16 : Memindahkan ubin kosong dari (2,1) ke (1,1)
- Langkah 17 : Memindahkan ubin kosong dari (1,1) ke (1,2)
- Langkah 18 : Memindahkan ubin kosong dari (1,2) ke (1,3), sehingga sesuai dengan tujuan yang diinginkan

Perbandingan dengan Cara Pengerjaan Nomor 1

- Jumlah langkah yang digunakan lebih sedikit yaitu hanya membutuhkan 5 langkah untuk mencapai tujuan yag diinginkan, dibandingkan dengan cara pengerjaan nomor 2 dimana membutuhkan 18 langkah untuk mencapai tujuan yang diiginkan.
- Cara penyelesaian atau solusi dari nomor satu juga jauh lebih sederhana dibandingkan cara pengerjaan nomor 2, karena cara pengerjaan nomor 1 yang membutuhkan sedikit langkah untuk mencapai tujuan yang diinginkan

Jadi dapat disimpulkan, kedua solusi berhasil mencapai tujuan, namun terdapat perbedaan dalam tingkat kompleksitas dan jumlah langkah yang diperlukan. Solusi pertama lebih simpel dan efisien, sementara solusi kedua memerlukan langkah lebih banyak dikarenakan perbedaan keadaan awal. Ini menggambarkan dampak dari perbedaan keadaan awal terhadap perjalanan pencarian dalam masalah 8-puzzle.

3.	Ubahlah initial dan goal state dari program di atas sehingga bentuk initial dan goal statenya Gambar 5.9. Kemudian tentukan langkah-langkah mana saja sehingga puzzlenya mencapai goal state. Analisa dan bedakan dengan solusi pada point 1 dan 2.

#### Hasil Praktikum

![alt text](https://github.com/MFikriHidayat/Fikri/blob/main/Jobsheet%205%20Nomor%203.png)

Analisa Perbandingan dengan Cara Pengerjaan Nomor 1 dan 2

- Baik solusi pertama maupun kedua adalah solusi yang paling simpel atau sederhana kareana proses penyelesaian yang dilakukan berjalan dengan sangat cepat, dengan total waktu eksekusi sekitar 1 detik.
- Berbeda ketika menggunakan cara pengerjaan nomor 3 dimana membutuhkan total waktu 52 menit.



4.	Ubahlah initial dan goal state dari program di atas sehingga bentuk initial dan goal statenya Gambar 5.10. Kemudian tentukan langkah-langkah mana saja sehingga puzzlenya mencapai goal state. Analisa dan bedakan dengan solusi pada point 1, 2, dan 3. 

#### Hasil Praktikum

![alt text](https://github.com/MFikriHidayat/Fikri/blob/main/Jobsheet%205%20Nomor%204.png)

Analisa Perbandingan dengan Cara Pengerjaan Nomor 1, 2, dan 3

- Cara pengerjaan nomor 1, membutuhkan 4 langkah, dengan total waktu 0 detik.
- Cara pengerjaan nomor 2, membutuhkan 18 langkah, dengan total waktu 1 detik.
- Cara pengerjaan nomor 3, membutuhkan 20 langkah, dengan total waktu 52 mwnit, 23 detik.
- Cara pengerjaan nomor 4, membutuhkan 16 langkah, dengan total waktu  0 detik

Analisis Perbandingan
- Solusi 1 dan 4 berhasil mencapai tujuan dengan jumlah langkah yang lebih sedikit, dan prosesnya berlangsung sangat cepat, bahkan kurang dari 1 detik.
- Solusi 2 dan 3, memerlukan lebih banyak langkah dan waktu yang signifikan untuk mencapai tujuan.
- Solusi 2 merupakan solusi yang memerlukan jumlah langkah paling banyak di antara semua solusi.
- Solusi 3 memerlukan waktu yang sangat lama, yakni sekitar 52 menit, untuk menyelesaikan masalah, meskipun jumlah langkahnya hampir sama dengan Solusi 2.

Dari praktikum ini, dapat disimpulkan bahwa Solusi 1 dan Solusi 4 menunjukkan efisiensi yang tertinggi, sementara Solusi 3 adalah yang paling lambat dengan waktu yang sangat lama. Solusi 2 berada di posisi tengah dalam hal jumlah langkah, namun tetap memerlukan waktu yang cukup signifikan dibandingkan dengan Solusi 1 dan Solusi 4.


5.	Ubahlah initial dan goal state dari program dan class-class di atas sehingga bentuk initial dan goal statenya Gambar 5.11. Kemudian tentukan langkah-langkah mana saja sehingga puzzlenya mencapai goal state.

Berikut adalah langkah-langkah yang dapat diikuti untuk mencapai keadaan tujuan (goal state) "AHGB0FCDE" dari keadaan awal (initial state) "DBEAFGHC0" :

1. Geser ubin C ke atas, mengubah keadaannya menjadi "DBEAF0HCCG".
2. Geser ubin G ke kiri, mengubah keadaannya menjadi "DBEAFGH0CC".
3. Geser ubin H ke kiri, mengubah keadaannya menjadi "DBEAFH0GCC".
4. Geser ubin C ke atas, mengubah keadaannya menjadi "DBEAF0HCFC".
5. Geser ubin F ke kanan, mengubah keadaannya menjadi "DBEAFHF0CC".
6. Geser ubin E ke kanan, mengubah keadaannya menjadi "DBEAF0EFCH".
7. Geser ubin C ke atas, mengubah keadaannya menjadi "DBEAFCE0FH".
8. Geser ubin D ke kiri, mengubah keadaannya menjadi "DBEAF0CDEF".
9. Geser ubin E ke atas, mengubah keadaannya menjadi "DBE0FCEAHF".
10. Geser ubin F ke kanan, mengubah keadaannya menjadi "DBEFCE0AHF".
11. Geser ubin A ke kanan, mengubah keadaannya menjadi "DBEF0CEAHF".
12. Geser ubin H ke kanan, mengubah keadaannya menjadi "DBEFCEAH0F".
13. Geser ubin H ke kanan, mengubah keadaannya menjadi "DBEFCEA0HF".
14. Geser ubin F ke kanan, mengubah keadaannya menjadi "DBEFCE0AHF".
15. Geser ubin C ke atas, mengubah keadaannya menjadi "DBE0CEFAHF".
16. Geser ubin E ke atas, mengubah keadaannya menjadi "DBECE0FAHF".
17. Geser ubin F ke kanan, mengubah keadaannya menjadi "DBECEF0AHF".
18. Geser ubin A ke kanan, mencapai keadaan tujuan "AHGB0FCDE".
