# Capstone-Project-Module-2
Capstone Project Modul 2 Customer Personality Analysis

CUSTOMER SEGMENTATION

LATAR BELAKANG
Perusahaan yang sukses saat ini adalah perusahaan yang mengenal baik karakteristik pelanggannya sehingga mereka mampu menyediakan produk yang sesuai dengan kebutuhan pelanggannya. Hal ini dapat dicapai jika kita dapat mengelompokkan pelanggan ke dalam kelompok yang berbeda berdasarkan kesamaan dari karakter mereka.

Tujuan dari segmentasi ini adalah untuk melihat kebutuhan pelanggan, mengenal minat, gaya hidup, prioritas dan mempelajari kebiasaan belanja mereka sehingga dapat memaksimalkan nilai pelanggan bagi bisnis.


PERNYATAAN MASALAH
Dari dataset yang sudah di berikan, kita akan mencoba menjawab beberapa pertanyaan seputar prospek kedepannya agar perusahaan bisa lebih baik lagi. Pertanyaan tersebut diantaranya adalah:
1. Bagaimana karakteristik pelanggan?
2. Bagaimana kebiasaan berbelanja pelanggan?
3. Apakah ada produk dari perusahaan yang membutuhkan lebih banyak pemasaran?
4. Bagaimana pemasaran yang efektif untuk perusahaan?


DATA PROCESSING
Observasi:
- Terdapat missing value pada kolom `Income` sebesar 1.07%
- Kolom `Z_Revenue` dan `Z_CostContact` memiliki nilai konstan yang dimana tidak berpengaruh dalam      modeling
- `Marital_Status` dapat kita jadikan kategorikal variabel
- Tipe data `Dt_Customer` masih object dan akan di ganti menjadi Datetime

Handling anomalies:
- Drop missing value pada kolom income
- Mengganti format dari object ke datetime
- Drop data yang tidak di perlukan karena memiliki nilai yg sama dan tidak berpengaruh terhadap       modeling
- Pengecekan apakah ada data yg terduplikasi

Setelah di observasi datanya, para customer mendaftarkan diri ID pelanggannya ke perusahaan dari tahun 2012-2014. Saya akan berasumsi bahwa data ini diambil pada tahun 2015.


Kolom Marital_Status memiliki nilai yang berbeda, namun nilai tersebut memiliki kategori yang sama. Jadi kita akan membaginya menjadi 2 kategori utama yaitu Single dan In Relationship


Terdapat outliers pada `Income` dan `Age`. Maka dari itu kita akan melakukan pengecekan

DATA ANALYSIS
- Presentase antara customer yang memiliki pasangan dan yang tidak punya pasangan
- Visualisasi rata-rata pengeluaran antara customer yang memiliki pasangan dan yang tidak punya       pasangan


Setelah kita memvisualisasikan total pengeluaran customer yang Single dan In Relationship di atas, sekarang kita akan memvisualisasikan total pengeluaran customer yang tidak memiliki anak dan memiliki anak

Korelasi Age dan Total Spendings:
-Tidak ada hubungan kuat antara Umur customer dengan kebiasaan belanja customer

Korelasi Income dan Total Spendings:
-Terdapat korelasi positif antara Income dengan Total Spendings, dimana semakin besar Income yang di   dapat maka akan semakin besar juga pengeluaran customer terhadapt produk perusahaan


CLUSTERING
Kita akan mencari tahu perbedaan segmentasi pelanggan berdasarkan data pelanggan menggunakan K-means Cluster. Pertama kita akan drop kolom yang tidak di perlukan agar lebih simple dalam proses modeling

Identifikasi Cluster
Identifikasi 4 model cluster berdasarkan fitur data yang berbeda:
- Income
- Spendings
- Month Since Customer
- Age
- Number of Children

Interpretasi Cluster
Dari analisis diatas kita dapat mengelompokan customer menjadi 4 grup berdasarkan income dan total pengeluaran mereka:
- Platinum : Customer dengan pendapatan dan pengeluaran tertinggi
- Gold : Customer dengan pendapatan dan pengeluaran yang tinggi
- Silver : Customer dengan pendapatan dan pengeluaran yang rendah
- Bronze : Customer dengan pendapatan dan pengeluaran terendah

Korelasi Income dengan Total Pengeluaran tiap Cluster adalah positif dimana semakin besar pendapatan customer, maka akan semakin besar juga pengeluarannya


KESIMPULAN
- Mayoritas customer telah lulus dari universitas, hidup dengan pasangannya, mempunyai satu anak dan rata-rata pendapatannya antara $25.000 sampai dengan $85.000
- Customer yang tidak mempunyai anak dan yang masih Single pengeluarannya ternyata lebih besar dibandingkan yang memiliki anak dan yang hidup dengan pasangannya
- Produk Wine dan Meat merupakan produk yang sangat banyak dibeli oleh para customer
- Customer yang memiliki pendapatan tinggi ternyata pengeluarannya juga besar
- Mayoritas Customer lebih suka membeli produk dengan langsung datang ke Store dan lewat website perusahaan
- Platinum Customer lebih menunjukan ketertarikannya terhadap promosi yang dilakukan oleh perusahaan sementara itu Bronze Customer tidak tertarik dengan promosi yang di berikan oleh perusahaan

1.Bagaimana karakteristik pelanggan?
   Pelanggan perusahaan mayoritas sudah menikah. Mereka merupakan kelompok Middle Age Adults,    yang dimana usianya antara 40 sampai 60 tahun dan memiliki satu anak. Mayoritas mempunyai    gelar sarjana S1 dan pendapatannya mencapai $25.000 sampai dengan $85.000

2. Bagaimana kebiasaan berbelanja pelanggan? 
   Pelanggan banyak menghabiskan uangnya ke jenis produk Wine dan Meat. Mereka yang tidak        memilik anak memiliki pengeluaran yang lebih banyak dibandingkan yang memiliki anak.          Middle   aged adults pengeluarannya lebih bannyak dibandingkan kelompok grup yang lain.      Belanja melalui toko merupakan pilihan dari banyak pelanggan. Pembelian melalui Web dan      Catalog juga memiliki potensial yang bagus karena presentase belanjanya tinggi.

3. Apakah ada produk dari perusahaan yang membutuhkan lebih banyak pemasaran?
   Produk Sweet dan Fruits memerlukan pemasaran yang lebih efektif lagi karena kurangnya        minat customer untuk membeli produk tersebut. Perusahaan harus lebih mempromosikan produk    tersebut agar pendapatan perusahaan dapat meningkat. Rekomendasi saya mungkin dapat          diberlakukan potongan harga setiap pembelian produk tersebut.

4. Bagaimana pemasaran yang efektif untuk perusahaan?
   Sebagai rekomendasi pemasaran, berikan kupon belanja kepada pelanggan lama dan pelanggan      yang berbelanja dengan jumlah yang besar. Untuk produk-produk yang harganya murah bisa di    promosikan ke pelanggan yang pendapatannya rendah agar mereka memiliki minat dan masih        mampu untuk membeli produk tersebut. Dikarenakan pembelian melalui web memiliki potesial      yang besar, maka sebaiknya berikan potongan harga khusus kepada pelanggan yang mendaftar      lewat situs perusahaan



