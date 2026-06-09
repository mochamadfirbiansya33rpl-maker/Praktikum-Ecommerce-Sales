# 📊 Laporan Praktikum Lanjutan: Analisis Performa Penjualan E-commerce

**Nama:** Mochamad Rafa Firbiansya  
**Kelas:** XI RPL 4  
**Mata Kuliah:** Analisis dan Visualisasi Data  
**Tanggal:** Juni 2026  
**Dataset:** data_praktikum_analisis_data.xlsx

---

## 1. Business Question

Pertanyaan yang ingin dijawab dalam praktikum lanjutan ini:
- Kategori produk mana yang termasuk **underperformer**?
- Bagaimana **segmentasi pelanggan** menggunakan metode RFM?
- Kategori mana yang paling **efisien** dalam penggunaan anggaran iklan?
- Apakah peningkatan **Ad_Budget** di atas median menghasilkan peningkatan **Total_Sales** yang signifikan?
- Seberapa besar pengaruh Ad_Budget terhadap Total_Sales?

## 2. Data Wrangling

**Langkah yang dilakukan:**
- Dataset asli berisi **150 transaksi**.
- Ditemukan **7 missing values** pada kolom `Total_Sales`.
- Dilakukan pembersihan dengan menghapus baris yang memiliki data kosong.
- Total data setelah cleaning: **143 baris**.
- Semua kolom sudah dalam format yang sesuai untuk analisis.

## 3. Insights

### 3.1 Identifikasi Produk Underperformer
Kategori dengan rata-rata harga di atas keseluruhan namun volume penjualan lebih rendah:
- **Home Decor**
- **Fashion**
- **Electronics**

Kategori ini berpotensi membebani arus kas karena harga tinggi tetapi jarang terjual dalam jumlah besar.

### 3.2 Segmentasi Pelanggan (RFM Analysis)
- Jumlah pelanggan unik: **48 orang**
- Pelanggan terbaik (RFM tinggi):
  - CustomerID **5015, 5008, 5035, 5014, 5044**
- Banyak pelanggan memiliki kombinasi RFM Group **455** dan **555**

**Rekomendasi:** Berikan voucher loyalitas kepada pelanggan dengan RFM tinggi.

### 3.3 Efisiensi Kategori
Urutan kategori dari paling tidak efisien ke paling efisien:

| Peringkat | Kategori      | Efisiensi     | Keterangan                  |
|-----------|---------------|---------------|-----------------------------|
| 1 (Terburuk) | Gadget     | 1.025        | Iklan tinggi, sales rendah |
| 2         | Home Decor    | 1.170        | -                           |
| 3         | Fashion       | 1.241        | -                           |
| 4         | Books         | 1.277        | -                           |
| 5 (Terbaik)  | Electronics | 1.439        | Paling efisien              |

### 3.4 Uji Hipotesis (Ad_Budget vs Total_Sales)
- Median Ad_Budget: **Rp 2.703.000**
- Hasil uji t-test: **p-value = 0.674** (Tidak Signifikan)
- **Kesimpulan:** Peningkatan Ad_Budget di atas median **tidak** menghasilkan peningkatan Total_Sales yang signifikan pada data ini.

### 3.5 Regresi Linear Sederhana
- Koefisien Ad_Budget: **0.096**
- **R² = 0.003** (Sangat rendah)
- **Kesimpulan:** Ad_Budget hampir tidak memiliki pengaruh terhadap Total_Sales di dataset ini.

## 4. Recommendation

Berdasarkan hasil analisis, berikut rekomendasi yang dapat diberikan:

1. **Fokus promosi** pada kategori **Gadget** karena efisiensinya paling rendah.
2. Berikan **voucher loyalitas** kepada pelanggan dengan RFM tinggi (5015, 5008, 5035, dll).
3. **Evaluasi ulang** strategi periklanan karena peningkatan Ad_Budget tidak terbukti signifikan meningkatkan penjualan.
4. Lakukan peninjauan harga dan promosi pada kategori **Home Decor** dan **Fashion** yang memiliki harga tinggi tapi volume rendah.

## 5. Hasil Output Program

Analisis dilakukan menggunakan Python dengan library `pandas`, `matplotlib`, `seaborn`, `statsmodels`, dan `scipy`.

Beberapa hasil output penting:
- RFM Analysis berhasil mengelompokkan 48 pelanggan
- Uji hipotesis menunjukkan hasil tidak signifikan
- Model regresi memiliki R² yang sangat rendah (0.003)

## 6. File yang Disertakan

- `data_praktikum_analisis_data.xlsx` — Dataset asli
- `README.md` — Laporan analisis lanjutan ini
