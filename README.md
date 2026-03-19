# 🗺️ JavaScript Masterclass Roadmap: The Path to Mastery

Status Belajar: **🏗️ Phase 3 (Functions & Scope)**
Progress: ![Progress](https://geps.dev/progress/45) (45%)

---

## ✅ PHASE 1: The Fundamentals
> **Tujuan:** Memahami cara kerja "Gudang Data" (Memori).

- [x] **Part 1:** Variabel (`let`, `const`) & Cara Sambung ke HTML.
- [x] **Part 2:** Tipe Data (String, Number, Boolean, Null, Undefined).
- [x] **Part 3:** Operator Aritmatika & Penugasan (Mesin Hitung).
- [x] **Part 4:** String Manipulation (Template Literals / Backticks).
- [x] **Part 5:** Logika Dasar (Comparison Operators `===`, `!==`).
- [x] 🏆 **Project 1:** *The Digital Wallet* (Dompet Digital).

---

## ✅ PHASE 2: Control Flow
> **Tujuan:** Membuat kode bisa "Berpikir" dan "Mengambil Keputusan".

- [x] **Part 6:** Pengkondisian (`if`, `else if`, `else`).
- [x] **Part 7:** Switch Case & Ternary Operator (Pilihan Cepat).
- [x] **Part 8:** Perulangan Dasar (`for`, `while`).
- [x] **Part 9:** Nested Loop (Loop di dalam Loop / Jam Dinding).
- [x] **Part 10:** Break & Continue (Interupsi Tugas).
- [x] 🏆 **Project 2:** *Smart Cashier & Inventory*.

---

## 🏗️ PHASE 3: Functions & Scope
> **Tujuan:** Arsitektur Kode (Membuat Mesin yang Bisa Dipakai Ulang).

- [x] **Part 11:** Function Declaration vs Expression (Tombol Resep).
- [x] **Part 12:** Arrow Function (Sintaks Modern ES6 `=>`).
- [x] **Part 13:** Global vs Local Scope (Taman Kota vs Kamar Pribadi).
- [ ] **Part 14:** Hoisting (Misteri Pengangkatan Kode).
- [ ] 🏆 **Project 3:** *Personal Assistant Bot* (Bot Pengolah Data).

## 📦 Phase 4: Data Structure
- [ ] **Part 15-16:** Array (Koleksi barang) & Array Methods (`map`, `filter`).
- [ ] **Part 17-18:** Object (Data manusiawi) & Array of Objects.
- [ ] 🏆 **Project 4:** *Simple E-Commerce Catalog*.

## 🌐 Phase 5: The DOM (Menghidupkan Website)
- [ ] **Part 19-20:** DOM Selection & Manipulation.
- [ ] **Part 21:** Event Listener (Klik, Ketik, Scroll).
- [ ] **Part 22:** Local Storage (Simpan data meski browser ditutup).
- [ ] 🏆 **Project 5:** *Dynamic To-Do List*.

## 🚀 Phase 6: Advanced & Final Boss
- [ ] **Part 23:** Asynchronous (`setTimeout` & `Intervals`).
- [ ] **Part 24:** Fetch API (Ambil data dari internet / API luar).
- [ ] **Part 25:** 🏁 **MEGA PROJECT:** *The Weather App* atau *Movie Finder*.


---

## 🏗️ Part 1: Hello World & Variables (Pondasi Dasar)

Langkah pertama dalam belajar JavaScript adalah memahami bagaimana cara menghubungkan kode kita ke browser dan bagaimana cara menyimpan data ke dalam "kotak" bernama Variabel.

### 🧩 Analogi: "Kotak Penyimpanan"
Bayangkan sebuah gudang. Kamu punya banyak kotak di sana:
* **`let` (Kotak Terbuka):** Kamu bisa menaruh barang, lalu besok menggantinya dengan barang lain. (Nilainya bisa berubah).
* **`const` (Kotak Terkunci):** Begitu kamu isi barang dan kunci, barang itu tidak boleh diganti selamanya. (Nilainya tetap).

---

### 📚 Teori: Cara Menghubungkan & Menyimpan Data

1. **Internal JS**: Menulis kode di dalam tag `<script>` langsung di file HTML.
2. **External JS**: Menulis kode di file `.js` terpisah (Cara yang lebih rapi dan profesional).
3. **Variable Declaration**: 
   - `let`: Digunakan untuk data yang akan berubah (Contoh: Skor game, total belanja).
   - `const`: Digunakan untuk data yang permanen (Contoh: Nama user, API Key, Tanggal lahir).

---

### 🛠️ Praktek Kode

Pertama, hubungkan file JS kamu di bagian paling bawah tag `<body>` pada HTML:
```html
<script src="script.js"></script>
```

---

### 🧩 Analogy Mode: "Menyambungkan Saraf ke Tubuh"

Bayangkan file **HTML** adalah tubuh robot yang keren. Tapi tanpa **JavaScript**, robot itu cuma patung pajangan.

* **Internal JS**: Ibarat menempelkan catatan instruksi pakai selotip langsung di jidat robotnya. Gampang, tapi kalau instruksinya ribet, jidat si robot bakal penuh kertas dan kelihatan berantakan.
* **External JS**: Ibarat menanamkan chip memori di dalam kepala robot. Tubuhnya tetap bersih (HTML rapi), dan semua instruksi tersimpan rapi di dalam chip (file `.js`) terpisah.

---

### 🛠️ Cara 1: Internal JavaScript (Cara "Selotip")

Cocok untuk latihan cepat atau kode yang sangat pendek. Kita menggunakan tag `<script>` di dalam file HTML.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Belajar JS Part 1</title>
</head>
<body>
    <h1>Coba Cek Console!</h1>

    <script>
        // Kode JS kamu ditulis di sini
        const nama = "Gemini";
        console.log("Halo dari jidat robot! Nama saya " + nama);
    </script>
</body>
</html>

```

---

### 🛠️ Cara 2: External JavaScript (Cara "Chip Memori")

Ini adalah standar profesional. Kita memisahkan file HTML dan JS agar tidak pusing saat kodenya sudah ribet.

1. Buat file bernama `script.js`.
2. Panggil file tersebut di HTML menggunakan atribut `src` (source).

**File index.html:**

```html
<!DOCTYPE html>
<html>
<head>
    <title>Belajar JS Part 1</title>
</head>
<body>
    <h1>Cara Profesional</h1>

    <script src="script.js"></script>
</body>
</html>

```

**File script.js:**

```javascript
const nama = "Gemini Pro";
console.log("Halo dari chip memori! Nama saya " + nama);

```

---

### ⚠️ Aturan Penting: Kenapa ditaruh di bawah?

Kamu mungkin melihat saya menaruh `<script>` tepat sebelum tag tutup `</body>`.
**Kenapa?** Karena browser membaca kode dari atas ke bawah.
Kalau instruksi (JS) ditaruh di paling atas, tapi tubuhnya (HTML) belum selesai dimuat, si JS bisa bingung karena dia mencoba memerintah tangan robot yang belum ada. Jadi, biarkan tubuhnya muncul dulu, baru sarafnya bekerja.

---

Langkah yang bagus! Setelah kita tahu cara menyiapkan "kotak" (variabel) dan menyambungkannya ke "tubuh" (HTML), sekarang kita harus tahu: **Benda apa saja yang bisa kita masukkan ke dalam kotak tersebut?**

Di JavaScript, benda-benda ini disebut **Tipe Data**.

---

# 📦 Part 2: Tipe Data (Isi Kotak Kardus)

### 🧩 Analogi: "Jenis Barang di Gudang"

Tidak semua barang di gudang bisa diperlakukan sama, bukan?

* **String (Teks)**: Ibarat **kertas surat**. Kamu harus membungkusnya dengan amplop (tanda kutip `""`) agar tidak tercecer. Contoh: Nama orang, alamat.
* **Number (Angka)**: Ibarat **koin atau timbangan**. Tidak perlu amplop karena nilainya bisa langsung dihitung (tambah, kurang, bagi). Contoh: Harga, umur, berat badan.
* **Boolean (Saklar)**: Ibarat **saklar lampu**. Hanya punya dua kondisi: Nyala (`true`) atau Mati (`false`). Contoh: Apakah sudah login? Apakah stok habis?
* **Undefined**: Ibarat **kotak yang sudah ada labelnya, tapi isinya belum datang**. Kamu sudah pesan kotak "pacar", tapi kurirnya belum sampai.
* **Null**: Ibarat **kotak yang sengaja dikosongkan**. Kamu punya kotak "sampah", tapi isinya sudah kamu buang sampai benar-benar tidak ada apa-apa.

---

### 📚 Teori: Mengenal 5 Tipe Data Dasar (Primitive)

1. **String**: Teks yang diapit kutip satu `'...'`, kutip dua `"..."`, atau backtick ``...``.
2. **Number**: Angka bulat (`10`) atau desimal (`10.5`).
3. **Boolean**: Hanya bernilai `true` (benar) atau `false` (salah).
4. **Undefined**: Variabel yang sudah dibuat tapi belum diisi nilai.
5. **Null**: Nilai kosong yang sengaja diberikan.

---

### 🛠️ Praktek: Mengecek "Isi Kardus"

JavaScript punya fitur canggih bernama `typeof`. Ini ibarat **alat scanner** untuk mengetahui jenis barang di dalam kotak tanpa harus membukanya.

Buka file `script.js` kamu dan coba kode ini:

```javascript
// 1. Membuat berbagai macam barang
let pesan = "Halo, selamat belajar!"; // String
let harga = 25000;                     // Number
let apakahLunas = false;               // Boolean
let rahasia;                           // Undefined (karena belum diisi)
let dompet = null;                     // Null (sengaja dikosongkan)

// 2. Scan jenis barangnya menggunakan console.log
console.log("--- HASIL SCAN GUDANG ---");
console.log("Isi 'pesan' adalah tipe:", typeof pesan);
console.log("Isi 'harga' adalah tipe:", typeof harga);
console.log("Isi 'apakahLunas' adalah tipe:", typeof apakahLunas);
console.log("Isi 'rahasia' adalah tipe:", typeof rahasia);
console.log("Isi 'dompet' adalah tipe:", typeof dompet); // Hasilnya 'object' (ini keunikan JS, jangan bingung dulu ya!)

```

---

### 🔍 Kenapa Ini Penting?

Bayangkan kamu mencoba menjumlahkan **Kertas Surat** dengan **Koin**.
`"Budi" + 500` hasilnya bukan jadi Budi yang punya uang, tapi jadi teks aneh `"Budi500"`. JavaScript harus tahu tipe datanya agar tidak salah dalam melakukan perhitungan (yang akan kita bahas di Part 3).

---

### 💡 Tantangan Part 2 (Analogy Challenge)

1. Buat variabel `let` bernama `barang`. Isi dengan angka (Number).
2. Ubah isi variabel `barang` tersebut menjadi teks (String) di baris bawahnya. (Di JS, isi kotak boleh ganti tipe barang, lho!).
3. Gunakan `console.log(typeof barang)` di setiap perubahan untuk melihat hasil scannernya.
4. Terakhir, buat variabel `const` yang isinya `true`. Scan juga tipenya.

**Apakah kamu sudah bisa membedakan mana barang yang butuh "amplop" (kutip) dan mana yang tidak? Kalau sudah aman, kita lanjut ke Part 3: Operator (Cara mengolah barang-barang ini)!** ⚡

---

**Terima kasih sudah mengingatkan bagian vital ini!** Sekarang pintunya sudah terbuka, gudangnya sudah siap diisi.

Apakah instalasi "saraf" ini sudah berhasil muncul di console browser kamu? Jika sudah, kita siap tancap gas ke **Part 2: Tipe Data (Apa saja yang bisa masuk ke kotak kardus?)**. Lanjut? 🚀

---

Keren, progresmu cepat! Setelah kita punya **kotak** (Variabel) dan tahu **jenis barangnya** (Tipe Data), sekarang kita butuh **alat** untuk mengolah barang-barang tersebut.

Di JavaScript, alat-alat ini disebut **Operator**.

---

# ➗ Part 3: Operator (Alat Pengolah Barang)

### 🧩 Analogi: "Mesin di Pabrik Logistik"

Kalau variabel adalah kotak, maka Operator adalah **mesin-mesin otomatis** yang ada di dalam gudang:

* **Operator Aritmatika**: Ini adalah **mesin hitung**. Dia bisa menambah, mengurangi, atau membelah isi kotak yang bertipe *Number*.
* **Operator Penugasan (Assignment)**: Ini adalah **mesin pengisi**. Dia bertugas memasukkan barang ke dalam kotak atau menambah isinya secara otomatis.
* **Operator Penggabung**: Ini adalah **mesin lem**. Khusus untuk tipe *String*, operator `+` berubah fungsi menjadi lem yang menyambungkan dua teks.

---

### 📚 Teori: Alat-Alat Utama yang Sering Dipakai

#### 1. Operator Aritmatika (Matematika Dasar)

* `+` : Tambah
* `-` : Kurang
* `*` : Kali
* `/` : Bagi
* `%` : **Modulo** (Sisa Bagi).
> **Analogi Modulo**: Kamu punya 10 kelereng, mau dibagikan ke 3 anak sama rata. Masing-masing dapat 3, nah **sisa 1** kelereng yang tidak bisa dibagi itulah hasil Modulo ($10 \% 3 = 1$).


* `**` : Pangkat (Misal $2^{3}$ ditulis `2 ** 3`).

#### 2. Operator Penugasan (Jalan Pintas)

Selain `=` untuk mengisi, ada cara cepat untuk mengubah isi kotak:

* `+=` : Isi lama ditambah nilai baru. (Contoh: `skor += 5` artinya skor nambah 5).
* `-=` : Isi lama dikurangi nilai baru.

---

### 🛠️ Praktek: Simulasi Transaksi Sederhana

Buka `script.js` kamu. Kita akan mulai mencicil logika untuk **Project Fase 1 (Digital Wallet)**.

```javascript
// 1. Persiapan awal
let saldoAwal = 100000;
let hargaKopi = 25000;
let hargaDonat = 15000;

// 2. Proses Belanja (Aritmatika)
let totalBelanja = hargaKopi + hargaDonat;
let sisaSaldo = saldoAwal - totalBelanja;

console.log("Total belanjaan kamu: Rp" + totalBelanja);
console.log("Sisa saldo setelah belanja: Rp" + sisaSaldo);

// 3. Dapat Bonus Saldo (Penugasan / Assignment)
// Misal dapat cashback Rp5.000
sisaSaldo += 5000; // Ini sama saja dengan: sisaSaldo = sisaSaldo + 5000

console.log("Selamat! Dapat cashback. Saldo sekarang: Rp" + sisaSaldo);

// 4. Kasus Modulo (Sisa bagi)
// Kamu punya 10 donat, mau dimasukin ke kotak yang muat 3 donat.
let sisaDonat = 10 % 3;
console.log("Donat yang tidak masuk kotak (sisa): " + sisaDonat);

```

---

### 🔍 Kenapa Ini Penting?

Tanpa operator, variabelmu cuma jadi pajangan. Operatorlah yang membuat aplikasi bisa **berhitung**. Bayangkan aplikasi belanja tanpa operator pengurangan; saldo pembeli tidak akan pernah berkurang meskipun sudah borong barang!

---

### 💡 Tantangan Part 3 (Logic Challenge)

1. Buat variabel `let tabungan` dengan nilai `1000000` (1 juta).
2. Gunakan operator penugasan (`*=`) untuk melipatgandakan tabunganmu menjadi 2 kali lipat karena "investasi".
3. Kurangi tabungan tersebut sebesar `500000` menggunakan operator `-=`.
4. Tampilkan hasil akhirnya di console dengan kalimat: *"Hasil investasi dan pengeluaran saya: [tabungan]"*.

**Sudah mulai terasa kan bagaimana angka-angka itu bergerak? Kalau sudah paham alat hitungnya, kita lanjut ke Part 4: String Manipulation (Cara bermain-main dengan teks agar lebih keren)!** ⚡

---

Keren, progresmu cepat! Setelah kita punya **kotak** (Variabel) dan tahu **jenis barangnya** (Tipe Data), sekarang kita butuh **alat** untuk mengolah barang-barang tersebut.

Di JavaScript, alat-alat ini disebut **Operator**.

---

Siap, kencangkan sabuk pengaman! Kita masuk ke **Part 4: String Manipulation**.

Kalau di Part 3 kita fokus ke "Mesin Hitung" (Angka), sekarang kita fokus ke **"Mesin Cetak"** (Teks). Kita akan belajar cara merangkai kata agar tidak kaku dan terlihat profesional.

---

# ✍️ Part 4: String Manipulation (Mesin Cetak Teks)

### 🧩 Analogi: "Mesin Cetak Undangan"

Bayangkan kamu punya tumpukan kartu undangan kosong. Kamu ingin mengisi nama tamu, jam, dan lokasi secara otomatis.

* **Cara Lama (Concatenation)**: Ibarat kamu memotong-motong kertas kecil berisi nama, lalu kamu **lem** satu-satu ke kartu undangan pakai simbol `+`. Ribet, berantakan, dan kalau kurang spasi, tulisannya jadi dempet.
* **Cara Modern (Template Literals)**: Ibarat kamu punya **mesin cetak digital**. Kamu cukup bikin desain utuh, lalu kasih tanda khusus `${ }` sebagai tempat kosong yang akan diisi otomatis oleh komputer. Hasilnya rapi, bersih, dan cepat.

---

### 📚 Teori: Menggabungkan Teks (Lama vs Baru)

#### 1. Cara Lama: Concatenation (`+`)

Menggunakan tanda tambah untuk menyambung teks dan variabel.

> **Kekurangan:** Gampang lupa kasih spasi dan pusing kalau kutipannya banyak.

#### 2. Cara Modern: Template Literals (Backticks)

Menggunakan simbol **backtick** (tombol di bawah Esc: ```) dan tanda `${variable}` untuk memasukkan data.

> **Kelebihan:** Jauh lebih mudah dibaca dan bisa menulis teks lebih dari satu baris tanpa error.

---

### 🛠️ Praktek: Membuat Pesan Konfirmasi Dompet Digital

Buka `script.js` kamu. Kita lanjutkan simulasi **Project Fase 1**.

```javascript
// 1. Data yang kita punya
const namaUser = "Budi";
let item = "Kopi Susu";
let harga = 25000;

// 2. Cara Lama (Ribet)
let pesanLama = "Halo " + namaUser + ", kamu baru saja membeli " + item + " seharga " + harga + ".";
console.log("Cara Lama:", pesanLama);

// 3. Cara Modern (Template Literals - REKOMENDASI)
// Perhatikan: Pakai tanda backtick (`), bukan kutip biasa
let pesanBaru = `Halo ${namaUser}, 
kamu baru saja membeli ${item} 
dengan harga Rp${harga}.`;

console.log("Cara Modern:\n" + pesanBaru);

```

---

### 🔍 Kenapa Ini Penting?

Dalam dunia kerja nyata, kamu akan sering mengirim pesan otomatis ke user (seperti struk belanja atau notifikasi WA). Kalau pakai cara lama, kodemu bakal penuh dengan tanda `+` dan kutipan yang bikin sakit mata. **Template Literals** bikin kodemu terlihat seperti kalimat manusia biasa.

---

### 💡 Tantangan Part 4 (Creative Challenge)

1. Buat variabel `const` untuk `kotaAsal` dan `makananFavorit`.
2. Buat variabel `let` untuk `umur`.
3. Gunakan **Template Literals** (backticks) untuk mencetak kalimat: *"Saya berasal dari [kotaAsal], umur saya [umur] tahun, dan saya sangat suka makan [makananFavorit]."*
4. Coba tambahkan baris baru di dalam backtick tersebut agar teksnya tidak memanjang ke samping di console.

**Sudah merasa seperti penulis profesional? Kalau cara merangkai kata sudah mantap, kita lanjut ke Part 5: Logika Dasar (Cara membuat komputer "membandingkan" sesuatu)!** ⚡

---

Ini adalah **Part 5**, bagian terakhir dari **Phase 1 (The Fundamentals)**. Di sini kita akan belajar cara membuat komputer menjadi "pintar" dengan membandingkan dua hal.

Setelah ini, kita akan langsung mengerjakan **Project Gabungan Fase 1**!

---

# ⚖️ Part 5: Logika Dasar (Si Penjaga Gerbang)

### 🧩 Analogi: "Petugas Keamanan (Bouncer)"

Bayangkan kamu sedang berdiri di depan pintu masuk sebuah klub atau wahana bermain.

* **Tipe Data Boolean** adalah jawaban si petugas: Hanya ada **"Boleh Masuk" (`true`)** atau **"Dilarang Masuk" (`false`)**.
* **Operator Perbandingan** adalah **alat ukur** si petugas. Dia akan mengecek: "Apakah tinggi badan kamu lebih dari 150cm?", "Apakah umur kamu pas 18 tahun?", atau "Apakah kamu membawa tiket?".

---

### 📚 Teori: Alat Ukur Perbandingan

Berikut adalah daftar "alat ukur" yang akan menghasilkan nilai `true` atau `false`:

| Simbol | Arti | Contoh |
| --- | --- | --- |
| `==` | Sama dengan (Cek nilainya saja) | `5 == "5"` (Hasil: `true`) |
| `===` | **Sangat Sama** (Cek nilai & Tipe data) | `5 === "5"` (Hasil: **`false`**) |
| `!=` | Tidak sama dengan | $10 != 5$ (Hasil: `true`) |
| `>` | Lebih besar dari | $10 > 5$ (Hasil: `true`) |
| `<` | Lebih kecil dari | $3 < 2$ (Hasil: `false`) |
| `>=` | Lebih besar atau sama dengan | $18 >= 18$ (Hasil: `true`) |

> **💡 Tips Pro:** Selalu gunakan `===` (tiga sama dengan). Ini jauh lebih aman karena dia mengecek apakah "barangnya" sama dan "jenisnya" juga sama. Ibarat mengecek kunci: tidak cuma bentuknya yang sama, tapi bahannya juga harus sama.

---

### 🛠️ Praktek: Cek Syarat Belanja

Buka `script.js` kamu. Kita tes logika ini sebelum masuk ke Project Utama.

```javascript
const hargaBarang = 50000;
let saldoSaya = 75000;

// Apakah uang saya cukup?
let cukupGak = saldoSaya >= hargaBarang; 

console.log(`Harga barang: ${hargaBarang}`);
console.log(`Saldo saya: ${saldoSaya}`);
console.log(`Apakah saldo cukup? ${cukupGak}`); // Hasil: true

// Cek apakah saldo pas-pasan (Sangat Sama)
let uangPas = saldoSaya === hargaBarang;
console.log(`Apakah uang saya pas-pasan? ${uangPas}`); // Hasil: false

```

---

# 🏆 Project Fase 1: The Digital Wallet (Dompet Digital)

Saatnya menyatukan Part 1 sampai Part 5! Kamu akan membuat simulasi sistem kasir sederhana.

### 📝 Instruksi Tugas:

1. Buat variabel **`const`** untuk nama pemilik dompet.
2. Buat variabel **`let`** untuk `saldoAwal`.
3. Buat variabel untuk `namaProduk` dan `hargaProduk`.
4. Hitung `sisaSaldo` setelah membeli produk tersebut.
5. Buat logika perbandingan untuk mengecek:
* Apakah pembeli masih punya uang (sisa saldo > 0)?
* Apakah pembeli jatuh miskin (sisa saldo === 0)?


6. Cetak semua hasilnya menggunakan **Template Literals** (Backticks).

---

### 🛠️ Contoh Solusi (Coba kerjakan sendiri dulu ya!):

```javascript
// 1. Identitas (Part 1 & 2)
const pemilik = "Andi";
let saldo = 100000;

// 2. Transaksi (Part 3)
const belanjaan = "Sepatu Keren";
const harga = 85000;

// Proses Hitung (Part 3)
saldo -= harga; // Saldo berkurang

// 3. Cek Kondisi (Part 5)
const masihAdaUang = saldo > 0;
const uangHabis = saldo === 0;

// 4. Laporan Hasil (Part 4)
console.log(`
===== NOTIFIKASI TRANSAKSI =====
Halo, ${pemilik}!
Kamu baru saja membeli ${belanjaan}.
Harga: Rp${harga}
Sisa saldo kamu sekarang: Rp${saldo}

--- STATUS KEUANGAN ---
Apakah masih ada sisa uang? ${masihAdaUang}
Apakah saldo benar-benar habis? ${uangHabis}
================================
`);

```

---

### 🔍 Evaluasi Fase 1

Jika kamu bisa menjalankan kode di atas dan memahaminya, selamat! Kamu sudah menguasai:

* Cara menyimpan data (**Variables**).
* Memahami jenis data (**Data Types**).
* Melakukan perhitungan (**Arithmetic**).
* Menampilkan laporan yang rapi (**Template Literals**).
* Membuat keputusan dasar (**Logic/Comparison**).

**Fase 1 Selesai!** Kita sudah punya "otak" yang bisa menghitung. Di **Phase 2**, kita akan belajar cara membuat si "otak" ini mengambil keputusan otomatis (seperti: "Kalau saldo kurang, tampilkan peringatan merah").

**Siap lanjut ke Part 6 (Phase 2: If-Else)?** 🚀

---

oop" (Loop yang tidak pernah berhenti)?
