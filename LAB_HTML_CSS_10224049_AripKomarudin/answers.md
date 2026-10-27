
# Jawaban Praktikum: Arip Komarudin (10224049)

## Bagian 1: Pemanasan

### 1. Selector dan deklarasi CSS

Pada aturan `nav a.active:hover { color: red; }`:

- Selector: `nav a.active:hover`
- Deklarasi: `color: red;`
- Property: `color`
- Value: `red`
- Pseudo-class: `:hover`

### 2. Jenis elemen HTML

- Inline: `span`, `a`, `strong`
- Block: `p`, `h2`
- `li`: secara default ditampilkan sebagai item daftar (`list-item`).

### 3. Selector descendant

Paragraf A dan B menjadi hijau karena keduanya merupakan elemen `p` yang berada di dalam elemen dengan class `box`.

### 4. CSS specificity

Warna teks menjadi merah karena selector `#title` memiliki specificity lebih tinggi daripada `.heading` dan `h1`.

### 5. Memperbaiki struktur HTML

Kesalahan terdapat pada urutan penutupan tag. Tag `<strong>` harus ditutup sebelum tag `<p>`.

Perbaikan:

`<p>Hello <strong>world</strong></p>`

---

## Bagian 3: Selector Golf

### P1. Prediksi warna teks

a. "Weekly hack nights." — Hijau karena cocok dengan selector `section p`.

b. "Bring your own laptop." — Oranye karena cocok dengan selector `.note`.

c. "© 2026 Student Affairs" — Biru karena cocok dengan selector `p`, jika tidak ada aturan lain yang lebih spesifik.

### P2. Urutan specificity

Urutan dari tertinggi ke terendah:

1. `#tech p`
2. `.club p`
3. `main section p`
4. `p`

### Hasil pengujian

Hasil warna harus dicatat berdasarkan CSS pengujian P1 yang diberikan dalam instruksi praktikum. Aturan 11 tantangan pada `selector-golf.css` merupakan pengujian terpisah.

---

## Bagian 4: Styling Profil dan Box Model

### Q1. Lebar elemen dengan content-box

Jika width = 300px, padding kiri dan kanan masing-masing 16px, serta border kiri dan kanan masing-masing 1px:

Lebar total = 300px + 32px + 2px = **334px**.

### Q2. Lebar elemen dengan border-box

Jika menggunakan `box-sizing: border-box` dan width = 300px, lebar total dari tepi border ke tepi border tetap **300px**.

Padding dan border sudah termasuk dalam ukuran width.

### Q3. Pemeriksaan melalui DevTools

Pemeriksaan dilakukan melalui browser DevTools pada bagian Computed atau Box Model untuk melihat content, padding, border, dan margin.

---

## Bagian 5: Tabel Debug

| # | Baris | Bug | Perbaikan | Cara menemukannya |
|---|---|---|---|---|
| 1 | 8 | Properti `colour` tidak valid dalam CSS | Mengganti `colour` menjadi `color` | Membaca kode CSS dan memeriksa properti |
| 2 | 11 | Deklarasi `background` tidak diakhiri titik koma | Menambahkan `;` setelah `#dbe7f3` | Membaca aturan CSS dan memeriksa tampilan |
| 3 | 14 | Selector `.Card` tidak cocok dengan class `card` | Mengganti `.Card` menjadi `.card` | Membandingkan selector CSS dengan class HTML |
| 4 | 19 | Penulisan ukuran `18 px` tidak valid | Mengganti menjadi `18px` | Memeriksa nilai properti CSS |
| 5 | 23 | Nilai `centre` tidak valid untuk `text-align` | Mengganti menjadi `center` | Memeriksa properti CSS |
| 6 | 29 | Tag `<h1>` ditutup menggunakan `</h2>` | Mengganti menjadi `</h1>` | Membaca pasangan tag HTML |
| 7 | 32 | Tanda kutip atribut `href` tidak lengkap | Memperbaiki menjadi `href="about.html"` | Memeriksa atribut tautan |
| 8 | 38 | ID `newsList` tidak cocok dengan selector `#news-list` | Mengganti ID menjadi `news-list` | Membandingkan ID HTML dengan selector CSS |
| 9 | 37 | Gambar tidak memiliki atribut `alt` | Menambahkan `alt="Berita kampus"` | Memeriksa atribut elemen gambar |

### Kesimpulan Debugging

Saya belajar bahwa kesalahan kecil dalam penulisan HTML dan CSS dapat memengaruhi tampilan dan fungsi halaman web. Membaca kode secara teliti, menggunakan validator, dan memeriksa hasil melalui browser membantu menemukan serta memperbaiki kesalahan tersebut.


---

## Bagian 6: Review HTML dan CSS

| # | Baris | Masalah | Mengapa penting | Perbaikan saya |
|---|---|---|---|---|
| 1 | 1 | Tidak ada deklarasi `<!DOCTYPE html>` | Browser dapat menampilkan halaman dalam mode yang tidak diharapkan | Menambahkan `<!DOCTYPE html>` |
| 2 | 1 | Tag `<html>` tidak memiliki atribut `lang` | Membantu browser dan teknologi pembaca layar mengenali bahasa halaman | Menggunakan `<html lang="id">` |
| 3 | 2 | Tidak ada deklarasi charset dan viewport | Karakter dan tampilan halaman pada perangkat berbeda dapat bermasalah | Menambahkan `meta charset="UTF-8"` dan pengaturan viewport |
| 4 | 5 | Header menggunakan lebar tetap `1200px` | Halaman dapat melebar dan sulit dibaca pada layar kecil | Menggunakan `width: 100%` atau lebar responsif |
| 5 | 6 | Menggunakan `!important` pada warna tautan | Membuat aturan CSS lebih sulit diatur dan ditimpa | Menghapus `!important` dan mengatur selector dengan tepat |
| 6 | 7 | Warna teks `#bbbbbb` kurang kontras dengan latar putih | Teks lebih sulit dibaca | Menggunakan warna teks yang lebih gelap |
| 7 | 8 | Selector `.sidebar` tidak digunakan pada HTML | Aturan CSS menjadi tidak diperlukan | Menghapus aturan yang tidak digunakan atau menambahkan elemen yang sesuai |
| 8 | 14 | Nama kampus hanya menggunakan tag `<b>`, bukan heading | Struktur judul halaman kurang semantik | Menggunakan tag `<h1>` |
| 9 | 20 dan 26 | Judul bagian menggunakan inline style | Gaya sulit dipelihara jika digunakan berulang kali | Membuat class CSS khusus, misalnya `.section-title` |
| 10 | 21 dan 25 | Menggunakan `<br>` berulang kali untuk membuat jarak | Tag `<br>` seharusnya digunakan untuk pemisah baris, bukan mengatur tata letak | Mengatur jarak menggunakan `margin` atau `padding` |
| 11 | 24 | Gambar tidak memiliki atribut `alt` | Pengguna pembaca layar tidak mendapat deskripsi gambar | Menambahkan atribut `alt` yang menjelaskan gambar |
| 12 | 27–28 | Input tidak memiliki label | Pengguna mungkin kesulitan mengetahui fungsi setiap kolom | Menambahkan `<label>` yang terhubung dengan input |
| 13 | 28 | Kolom email menggunakan `type="text"` | Browser tidak membantu memvalidasi format email | Mengubah menjadi `type="email"` |
| 14 | 29 | Tombol menggunakan `onclick` untuk menampilkan alert | Belum ada proses pengiriman formulir yang sebenarnya | Menggunakan elemen `<form>` dan menangani pengiriman formulir |
| 15 | 16 | Tautan menggunakan `href="#"` | Tautan belum mengarah ke halaman atau bagian yang dituju | Mengganti dengan URL atau ID tujuan yang benar |
| 16 | 31 | Footer menggunakan `<div>` biasa | Struktur halaman kurang semantik | Menggunakan tag `<footer>` |

### Refleksi

**1. Masalah yang paling mudah ditemukan**

Masalah yang paling mudah saya temukan adalah atribut gambar `alt` yang belum tersedia dan penggunaan inline style. Keduanya dapat ditemukan dengan membaca kode HTML secara langsung.

**2. Masalah yang paling sulit ditemukan**

Masalah yang lebih sulit adalah menentukan apakah warna teks sudah memiliki kontras yang cukup dan apakah tata letak responsif. Saya perlu memeriksa tampilan halaman dan menguji halaman pada ukuran layar yang berbeda.

**3. Pelajaran yang saya dapatkan**

Saya belajar bahwa HTML bukan hanya untuk menampilkan konten, tetapi juga harus memiliki struktur semantik yang baik. CSS perlu ditulis secara teratur, responsif, dan mudah dipelihara agar halaman web nyaman digunakan.


---

## Bagian 7: Exit Ticket

### 1. Jelaskan struktur dasar sebuah aturan CSS.

Sebuah aturan CSS terdiri dari selector dan blok deklarasi. Di dalam blok deklarasi terdapat property dan value, misalnya `p { color: blue; }`, yang berarti teks pada elemen paragraf ditampilkan dengan warna biru.

### 2. Selector atau konsep CSS apa yang masih membingungkan?

Saya masih perlu berlatih memahami specificity ketika beberapa selector mengatur elemen yang sama. Saya perlu memastikan selector mana yang memiliki prioritas lebih tinggi dan bagaimana browser menentukan aturan yang digunakan.

### 3. Apa satu hal yang sekarang bisa dilakukan tanpa melihat panduan?

Saya sekarang dapat membuat struktur halaman HTML sederhana dan menghubungkannya dengan file CSS eksternal. Saya juga dapat menggunakan selector dasar untuk mengatur warna, ukuran teks, dan tampilan elemen pada halaman web.