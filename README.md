# Capstone2_Rahadian-Yaumal-Etantyo
# Capstone Project Modul 2
## Analisis Vendor 2 - NYC TLC Trip Record
**Nama:** Rahadian Yaumal Etantyo  
**Dataset:** NYC TLC Trip Record  
**Fokus:** Analisis faktor yang mempengaruhi `total_amount` pada Vendor Verifone
## Tujuan Proyek
Proyek ini bertujuan untuk mengidentifikasi faktor-faktor yang mempengaruhi `total_amount` pada Vendor verifone dari dataset NYC TLC Trip Record. Hasil analisis ini akan digunakan untuk merumuskan strategi peningkatan pendapatan bagi Vendor verifone

## Data Understanding
Dataset yang digunakan merupakan data perjalanan taksi di NYC. Fokus analisis ini hanya pada transaksi yang dilakukan oleh Vendor verifone. Fitur-fitur penting dalam dataset meliputi:

- `tpep_pickup_datetime` & `tpep_dropoff_datetime`: waktu penjemputan dan pengantaran
- `passenger_count`: jumlah penumpang
- `trip_distance`: jarak perjalanan
- `payment_type`: metode pembayaran
- `fare_amount`, `tip_amount`, `total_amount`: komponen biaya
- `Rate code` : Kode Tarif
## Data Cleaning
Beberapa langkah pembersihan data yang telah dilakukan:
- Menghapus kolom yang tidak memiliki nilai seperti pada kolom `ehail_fee`
- Mengisi nilai kolom yang kosong dengan modus atau median karena data memiliki outlier
- Memfilter data hanya untuk Vendor verifone
- Mengubah format data yang belum tepat seperti pada kolom `tpep_pickup_datetime` & `tpep_dropoff_datetime` dll.
## Exploratory Data Analysis
Analisis dilakukan untuk memahami distribusi dan hubungan antar fitur. Beberapa insight awal:
- Mencari distribusi `total_amount`
- Mencari rata - rata `total_amount`
- Mencari median `total_amount`
- Mencari q1 dan q3 `total_amount`
- Mencari outlier dari data kolom `total_amount` kemudian menyaring data rentang upper bound dan lower bound
- Menyimpan data yang sudah tersaring ke file csv baru
- Mencari Korelasi antara `trip_distance` dan `total_amount`
- Mencari Korelasi antara `passenger_count` dan `total_amount`
- Mencari Korelasi antara `PUlocationID` dan `total_amount`
- Mencari Korelasi antara `DOlocationID` dan `total_amount`
- Mencari Korelasi antara `fare_amount` dan `total_amount`
- Mencari Korelasi antara `tip_amount` dan `total_amount`
- Mengetahui hubungan antara `day` dan `total_amount`
- Mengetahui hubungan antara `payment_type` dan `total_amount`
- Mengetahui hubungan antara `Rate code` dan `total_amount`
## Insight dan Rekomendasi
Berdasarkan analisis, beberapa insight yang diperoleh:

- `fare_amount`dan`tip_amount` memiliki korelasi yang kuat dengan `total_amount`.
- `day`,`payment_type`,`Rate code` memiliki pengaruh signifikan terhadap `total_amount`
- Pembayaran menggunakan **credit card** lebih umum dan cenderung memiliki `tip_amount` lebih tinggi.
- Rate Code Newark menghasilkan rata - rata total amount lebih tinggi dibanding rate code yang lain

### Rekomendasi Strategi:
- Dorong penggunaan credit card melalui loyalty point yang dapat ditukarkan dengan reward trip gratis.
- Beri diskon trip pada hari sabtu dan minggu dan Optimalkan armada di lokasi populer akhir pekan
- Prioritaskan rute ke bandara (JFK/Newark); jalin kerjasama B2B untuk negotiated fare
- Tingkatkan training sopir untuk dorong pelayanan lebih bagus sehingga tip lebih tinggi
- Terapkan Skema Tarif Progresif untuk Jarak Lebih Jauh sehingga meningkatkan pendapatan
- Audit data perjalanan dengan distance/amount tidak valid







