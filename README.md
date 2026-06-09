# 📊 Laporan Praktikum: Analisis Performa Penjualan E-commerce

**Nama:** [Mochamad Rafa Firbiansya]  
**Kelas:** XI RPL 4  
**Mata Kuliah:** Analisis dan Visualisasi Data  
**Tanggal:** Juni 2026  
**Dataset:** data_praktikum_analisis_data.xlsx (150 transaksi)

---

## 1. Business Question

- Kategori produk mana yang termasuk underperformer?
- Bagaimana segmentasi pelanggan menggunakan RFM?
- Kategori mana yang paling efisien dalam penggunaan anggaran iklan?
- Apakah peningkatan Ad_Budget di atas median menghasilkan peningkatan Total_Sales yang signifikan?
- Seberapa besar pengaruh Ad_Budget terhadap Total_Sales?

## 2. Data Wrangling

- Dataset asli berisi **150 baris**.
- Terdapat **7 missing values** pada kolom Total_Sales → baris tersebut dihapus.
- Total data setelah cleaning: **143 baris**.
- Kolom yang digunakan: Order_ID, CustomerID, Order_Date, Product_Category, Quantity, Price_Per_Unit, Ad_Budget, Total_Sales.

## 3. Insights

### 3.1 Identifikasi Underperformer
Kategori dengan harga rata-rata di atas keseluruhan tapi volume lebih rendah:
- **Home Decor**, **Fashion**, dan **Electronics**

### 3.2 RFM Analysis
- Jumlah pelanggan unik: **48**
- Pelanggan terbaik (high monetary + recent): CustomerID **5015, 5008, 5035, 5014, 5044**
- Banyak pelanggan dengan RFM Group **455** dan **555**

### 3.3 Efisiensi Kategori
Dari yang paling tidak efisien ke paling efisien:
- **Gadget** (paling tidak efisien)
- Home Decor
- Fashion
- Books
- **Electronics** (paling efisien)

### 3.4 Uji Hipotesis
- Median Ad_Budget: Rp 2.703.000
- **Hasil: Tidak signifikan** (p-value = 0.674)
- Kesimpulan: Di data ini, peningkatan Ad_Budget di atas median **tidak** menghasilkan Total_Sales yang signifikan lebih tinggi.

### 3.5 Regresi Linear
- Koefisien Ad_Budget: 0.096
- **R² = 0.003** (sangat rendah)
- Kesimpulan: Ad_Budget hampir tidak memiliki pengaruh terhadap Total_Sales pada dataset ini.

## 4. Recommendation

1. Fokuskan promosi dan diskon pada kategori **Gadget** karena efisiensinya paling rendah.
2. Berikan perhatian khusus (voucher, early access) kepada pelanggan dengan RFM tinggi (5015, 5008, 5035, dll).
3. Evaluasi kembali strategi iklan karena berdasarkan data, peningkatan Ad_Budget tidak terlalu berpengaruh terhadap penjualan.
4. Lakukan analisis lebih dalam terhadap kategori Home Decor dan Fashion yang memiliki harga tinggi tapi volume rendah.

## 5. File yang Disertakan

- `data_praktikum_analisis_data.xlsx` (Dataset asli)
- `README.md` (Laporan ini)
