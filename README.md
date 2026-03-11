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

# 🚦 Part 6: Pengkondisian (If, Else If, Else)

### 🧩 Analogi: "Mesin Vending Machine"

Bayangkan kamu sedang berdiri di depan mesin minuman otomatis:

* **`if` (Rencana A)**: Kamu menekan tombol Cola. Mesin mengecek: "Apakah uangmu cukup?". Jika **Ya**, Cola keluar.
* **`else if` (Rencana B)**: Jika uangmu tidak cukup untuk Cola, mesin mengecek: "Apakah uangmu cukup untuk air mineral?". Jika **Ya**, air mineral keluar.
* **`else` (Pilihan Terakhir)**: Jika uangmu tidak cukup untuk apapun, mesin berbunyi *Tiiit!* dan menampilkan pesan: "Maaf, saldo tidak cukup."

---

### 📚 Teori: Membuat Cabang Keputusan

Dalam JavaScript, kita menggunakan tanda kurung `()` untuk syaratnya, dan kurung kurawal `{}` untuk instruksi yang dijalankan jika syarat itu benar.

```javascript
if (syarat_pertama) {
    // Jalankan kode ini kalau syarat_pertama TRUE
} else if (syarat_kedua) {
    // Jalankan kode ini kalau syarat_pertama FALSE, tapi syarat_kedua TRUE
} else {
    // Jalankan kode ini kalau SEMUA syarat di atas FALSE
}

```

---

### 🛠️ Praktek: Sistem Filter Umur Bioskop

Mari kita buat sistem yang mengecek apakah seseorang boleh menonton film berdasarkan umurnya.

```javascript
let umur = 15;

console.log(`Umur kamu: ${umur} tahun`);

if (umur >= 17) {
    console.log("Akses Diterima: Silahkan menonton film dewasa.");
} else if (umur >= 13) {
    console.log("Akses Terbatas: Kamu hanya boleh menonton film remaja.");
} else {
    console.log("Akses Ditolak: Kamu hanya boleh menonton kartun anak-anak.");
}

```

---

### 🔍 Kenapa Ini Penting?

Tanpa `if-else`, websitemu tidak akan bisa memberikan respon yang berbeda kepada user.

* Kalau password benar -> Masuk ke Dashboard.
* Kalau password salah -> Tampilkan pesan error merah.
Logika "Jika - Maka" adalah inti dari semua aplikasi hebat di dunia.

---

### 💡 Tantangan Part 6 (Decision Challenge)

1. Buat variabel `let nilaiUjian = 85`.
2. Gunakan `if`, `else if`, dan `else` untuk memberikan predikat:
* Nilai **90 ke atas** -> "Sangat Memuaskan"
* Nilai **70 - 89** -> "Memuaskan"
* Nilai **di bawah 70** -> "Coba Lagi Tahun Depan"


3. Ubah-ubah angka `nilaiUjian` kamu untuk memastikan semua pesan muncul di console.

**Bagaimana? Apakah si "Persimpangan Jalan" ini sudah jelas logikanya? Jika sudah, kita lanjut ke Part 7: Switch Case (Cara membuat pilihan yang lebih rapi jika opsinya banyak)!** ⚡

---

Lanjut! Kita masih di **Phase 2 (Control Flow)**. Kalau di Part 6 kita belajar tentang persimpangan jalan yang luas (`if-else`), sekarang kita akan belajar tentang **"Tombol Lift"** dan **"Jalan Pintas"**.

---

# 🔘 Part 7: Switch Case & Ternary Operator

### 🧩 Analogi 1: "Tombol Lift" (Switch Case)

Bayangkan kamu masuk ke dalam lift di sebuah mall:

* Kamu menekan tombol angka tertentu.
* Lift tidak akan bertanya "Apakah tombol ini lebih besar dari 1?", tapi dia langsung mengecek: "Apakah ini tombol 1? Apakah ini tombol 2? Atau tombol 3?".
* **`switch`** sangat cocok digunakan jika kamu punya satu variabel yang nilainya sudah pasti (spesifik), bukan berupa rentang (seperti umur > 17).

### 🧩 Analogi 2: "Gerbang Tol Otomatis" (Ternary Operator)

Pernah lihat papan pengumuman singkat yang cuma punya dua pilihan?

* "Punya kartu? Tempel : Ambil tiket."
* **Ternary Operator** adalah jalan pintas untuk `if-else` yang sangat sederhana. Daripada menulis 5 baris kode, kamu bisa merangkumnya dalam **1 baris** saja.

---

### 📚 Teori: Cara Kerja Si "Pemilih Cepat"

#### 1. Switch Case

Kita menggunakan `switch` untuk memeriksa satu nilai, lalu `case` untuk setiap pilihannya. Jangan lupa gunakan **`break`** agar liftnya berhenti di lantai yang tepat dan tidak meluncur ke bawah terus.

#### 2. Ternary Operator

Rumusnya: `(kondisi) ? "Hasil jika Benar" : "Hasil jika Salah";`

---

### 🛠️ Praktek: Menu Kantin Digital

Mari kita coba di `script.js` kamu:

```javascript
// --- CONTOH SWITCH CASE ---
let nomorMenu = 2;

switch (nomorMenu) {
    case 1:
        console.log("Kamu memilih: Nasi Goreng");
        break;
    case 2:
        console.log("Kamu memilih: Mie Ayam");
        break;
    case 3:
        console.log("Kamu memilih: Ayam Bakar");
        break;
    default:
        console.log("Menu tidak tersedia.");
}

// --- CONTOH TERNARY OPERATOR ---
let jam = 19;
// Jika jam kurang dari 18, maka "Selamat Siang", jika tidak "Selamat Malam"
let ucapan = (jam < 18) ? "Selamat Siang" : "Selamat Malam";

console.log(ucapan);

```

---

### 🔍 Perbedaan Penting: Kapan pakai yang mana?

* **`if-else`**: Pakai kalau syaratnya rumit atau berupa rentang (Contoh: nilai antara 80-100).
* **`switch`**: Pakai kalau pilihannya banyak tapi sudah pasti nilainya (Contoh: pilihan menu 1, 2, 3 atau hari Senin, Selasa, Rabu).
* **`ternary`**: Pakai kalau pilihannya cuma dua (Ya/Tidak) dan kodenya sangat pendek.

---

### 💡 Tantangan Part 7 (Efficiency Challenge)

1. Buat variabel `let kodePromo = "DISKON30"`.
2. Gunakan **Switch Case** untuk mengecek:
* Jika `"DISKON10"`, cetak "Potongan 10%".
* Jika `"DISKON30"`, cetak "Potongan 30%".
* Selain itu, cetak "Kode tidak valid".


3. Buat variabel `let umur = 20`. Gunakan **Ternary Operator** untuk mengecek apakah user sudah dewasa atau belum (syarat: 18 tahun). Masukkan hasilnya ke variabel `let status` lalu cetak.

**Bagaimana? Apakah lift dan jalan pintas ini membuat kodemu lebih rapi? Jika sudah paham, kita akan lanjut ke Part 8: Perulangan Dasar (Cara menyuruh komputer bekerja lembur tanpa mengeluh)!** ⚡
