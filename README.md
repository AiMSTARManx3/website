**Proyek Artikel**

**css grid dan penggunaannya**

CSS Grid adalah sistem layout berbasis grid yang memungkinkan kita untuk membuat desain web yang lebih fleksibel dan responsif. Dengan CSS Grid, kita bisa membagi halaman web menjadi kolom dan baris, sehingga memudahkan penataan elemen-elemen di dalamnya.

**Struktur Dasar CSS Grid**

CSS Grid memiliki dua konsep utama:

Grid Container: Elemen yang menjadi wadah grid (biasanya div dengan class tertentu).

Grid Items: Elemen-elemen di dalam grid yang akan disusun menggunakan grid.

**Cara Penggunaan CSS Grid:**

**1. Menentukan Grid Container**

Pertama, kita tentukan elemen yang menjadi grid container menggunakan properti display: grid;.


.container {
  display: grid;
}

**2. Menentukan Kolom dan Baris**

Setelah container ditentukan, kita bisa mengatur kolom dan baris menggunakan properti grid-template-columns dan grid-template-rows.

.container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr; 
  grid-template-rows: 100px auto 200px; 
}

1fr, 2fr, dan seterusnya adalah unit fraksi yang berarti "fraction of the available space." Jadi, 1fr akan mendapatkan sepertiga dari ruang yang tersedia.

**3. Mengatur Jarak Antar Grid Item**

Kita bisa menggunakan grid-gap (atau gap pada versi terbaru) untuk mengatur jarak antar elemen grid.


.container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  gap: 10px;
}

**4. Menyusun Grid Item**

Grid items bisa ditentukan di dalam container dengan menggunakan properti grid-column dan grid-row.


.item {
  grid-column: 1
  grid-row: 2;
}

**5. Membuat Grid Responsif**

CSS Grid memudahkan pembuatan layout responsif dengan media queries. Misalnya, kita bisa mengubah jumlah kolom berdasarkan lebar layar.

.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr); 
  gap: 10px;
}

@media (max-width: 768px) {
  .container {
    grid-template-columns: 1fr 1fr; 
  }
}

@media (max-width: 480px) {
  .container {
    grid-template-columns: 1fr; 
  }
}

**Contoh Penggunaan**

<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
  <div class="item">Item 3</div>
  <div class="item">Item 4</div>
</div>

<style>
  .container {
    display: grid;
    grid-template-columns: repeat(2, 1fr); 
    gap: 20px;
  }
  .item {
    background: lightblue;
    padding: 20px;
    text-align: center;
  }
</style>

**Keuntungan Menggunakan CSS Grid:**

Fleksibilitas: Layout bisa dibuat dengan lebih fleksibel dan mudah, tanpa perlu mengatur posisi secara manual.

Responsif: Mudah membuat desain yang responsif dengan mengubah jumlah kolom dan baris berdasarkan ukuran layar.

Pengelolaan Ruang: Menggunakan unit fraksi (fr) untuk pembagian ruang secara dinamis.

Dengan CSS Grid, kamu bisa lebih mudah membuat desain yang bersih dan terstruktur. Apakah ada contoh spesifik yang ingin kamu buat?
