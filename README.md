# E-Commerce Sales EDA 2019

Exploratory Data Analysis (EDA) pada dataset penjualan e-commerce tahun 2019 untuk memahami pola transaksi, produk yang paling banyak terjual, distribusi harga, serta karakteristik pembelian berdasarkan data transaksi.

## Tujuan

Project ini bertujuan untuk:

* Membersihkan dan mempersiapkan data transaksi.
* Mengeksplorasi karakteristik dataset.
* Mengetahui produk dengan jumlah penjualan tertinggi.
* Menganalisis distribusi harga produk (`Price Each`).
* Menganalisis jumlah produk yang terjual (`Quantity Ordered`).
* Mengidentifikasi pola dan insight dari data penjualan.
* Menggunakan konsep probabilitas dan distribusi binomial pada data transaksi.

## Dataset

Dataset berisi data transaksi penjualan e-commerce selama tahun 2019.

Beberapa kolom yang digunakan dalam analisis antara lain:

| Kolom              | Deskripsi                   |
| ------------------ | --------------------------- |
| `Order Date`       | Tanggal dan waktu transaksi |
| `Product`          | Nama produk yang dibeli     |
| `Quantity Ordered` | Jumlah produk yang dibeli   |
| `Price Each`       | Harga per unit produk       |
| `Sales`            | Total nilai penjualan       |
| `Purchase Address` | Alamat pembelian            |

## Data Cleaning

Tahapan data cleaning yang dilakukan meliputi:

* Menangani data yang tidak valid atau kosong.
* Mengubah tipe data sesuai kebutuhan analisis.
* Mengonversi `Order Date` menjadi tipe datetime.
* Menangani format tanggal yang berbeda.
* Memeriksa dan menangani duplikasi data.
* Memastikan kolom numerik memiliki tipe data yang sesuai.
* Mengecek konsistensi nilai pada kolom produk dan harga.

## Exploratory Data Analysis

Analisis dilakukan menggunakan beberapa pendekatan visualisasi dan agregasi data.

### Produk dengan Penjualan Tertinggi

Menganalisis jumlah produk yang terjual untuk mengetahui produk yang paling banyak dibeli.

### Distribusi `Price Each`

Histogram digunakan untuk melihat persebaran harga produk dan mengetahui rentang harga yang paling sering muncul.

* **Sumbu X:** `Price Each`
* **Sumbu Y:** Frekuensi transaksi

### Analisis `Quantity Ordered`

Menganalisis jumlah unit yang dibeli pada setiap transaksi untuk melihat pola kuantitas pembelian.

### Analisis Transaksi Bulanan

Data transaksi dikelompokkan berdasarkan bulan untuk melihat pola penjualan selama tahun 2019.

## Probabilitas Pembelian Produk

Salah satu analisis menggunakan data transaksi bulan Januari untuk mengestimasi probabilitas pembelian suatu produk.

Probabilitas pembelian Produk B dihitung dengan:

$$
P(\text{Produk B}) =
\frac{\text{Jumlah Pembelian Produk B}}
{\text{Jumlah Seluruh Pembelian}}
$$

Hasil estimasi probabilitas Produk B adalah:

**2,39%**

Probabilitas tersebut kemudian digunakan sebagai parameter `p` dalam distribusi binomial.

Dengan:

* `n = 3000` pembelian
* `x = 72` pembelian Produk B
* `p = 0,0239`
* `q = 1 - p = 0,9761`

Rumus distribusi binomial:

$$
P(X=x) = \binom{n}{x}p^xq^{n-x}
$$

Hasil perhitungan:

**P(X = 72) ≈ 4,7494%**

Artinya, berdasarkan probabilitas yang diestimasi dari data, peluang terjadinya tepat 72 pembelian Produk B dari 3000 pembelian adalah sekitar **4,75%**.

## Tools & Libraries

Project ini menggunakan:

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* SciPy
* Jupyter Notebook

## Project Structure

```text
E-Commerce-EDA-2019/
│
├── data/
│   └── sales_data.csv
│
├── notebook/
│   └── E-Commerce_EDA_2019.ipynb
│
├── images/
│   └── ...
│
└── README.md
```

## Key Insights

Beberapa insight yang diperoleh dari proses EDA meliputi:

* Terdapat perbedaan jumlah penjualan antarproduk.
* Distribusi `Price Each` menunjukkan rentang harga yang paling sering muncul dalam transaksi.
* Jumlah pembelian per transaksi memiliki pola tertentu yang dapat diamati melalui visualisasi.
* Data transaksi dapat digunakan untuk mengestimasi probabilitas pembelian suatu produk.
* Distribusi binomial dapat digunakan untuk memodelkan kemungkinan jumlah pembelian Produk B dalam sejumlah transaksi.

## How to Run

Clone repository:

```bash
git clone <repository-url>
```

Masuk ke folder project:

```bash
cd E-Commerce-EDA-2019
```

Install library yang dibutuhkan:

```bash
pip install pandas numpy matplotlib seaborn scipy jupyter
```

Jalankan Jupyter Notebook:

```bash
jupyter notebook
```

Kemudian buka notebook pada folder `notebook/`.

## Author

**Anggit**

Data Analysis & Exploratory Data Analysis Project — 2019 E-Commerce Sales Dataset.
