# State Management Stream

---

## Soal 3

### Penjelasan fungsi keyword yield\*

- fungsi ini menghasilkan stream warna yang berubah setiap detik dengan urutan yang terulang, dan yield\* memungkinkan stream Stream.periodic untuk mengalirkan hasilnya ke dalam stream yang dihasilkan oleh getColors().

---

## Soal 4

### Caputer Hasil

![Capture Hasil Praktikum Soal 2](./assets/soal4.gif)

---

## Soal 5

### Penjelasan `Listen` dan `Await for`

- `await for` lebih bersifat blocking dalam artian menunggu setiap event secara berurutan, dan lebih cocok untuk situasi di mana Anda perlu menangani setiap event satu per satu secara sinkron.

- `listen` lebih fleksibel dan non-blocking, memungkinkan eksekusi kode lainnya berjalan bersamaan dengan mendengarkan stream.

---

## Soal 6

### Caputer Hasil

![Capture Hasil Praktikum Soal 2](./assets/soal6.gif)

### Penjelasan kode `Langkah 8 dan 10`

- `initState()` dijalankan ketika widget pertama kali dibuat dan berfungsi untuk menginisialisasi stream serta mendaftar listener yang akan mendengarkan data yang diterima dari stream. Di dalam fungsi ini, setiap kali data baru diterima, UI akan diperbarui menggunakan setState(), yang memastikan bahwa tampilan aplikasi selalu menampilkan nilai terbaru.

- `addRandomNumber()` digunakan untuk menghasilkan angka acak antara 0 hingga 9 dan menambahkannya ke dalam stream. Angka yang ditambahkan ke stream ini kemudian diterima oleh listener yang ada di initState(), sehingga tampilan UI akan diperbarui dengan angka yang baru.

---

## Soal 7

### Penjelasan kode `Langkah 13 sampai 15`

- `addError()` berfungsi untuk mengirimkan error ke dalam stream.

- `initState()` menginisialisasi stream dan mendaftarkan listener untuk menangani data yang diterima dari stream. Jika data diterima dengan sukses, UI akan diperbarui dengan nilai tersebut. Namun, jika error terjadi, UI akan menampilkan nilai -1 (sebagai tanda error).

- `addRandomNumber()` (meskipun seharusnya menghasilkan angka acak) justru menambahkan error ke dalam stream, yang kemudian akan diproses oleh handler onError di initState(). Ketika error ditambahkan ke dalam stream, listener akan menangani error tersebut dengan mengubah nilai lastNumber menjadi -1.
