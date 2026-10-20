# UTS Graf Sains Data — Sistem Rekomendasi Produk RetailRocket

## Identitas Mahasiswa

| Informasi | Keterangan |
|---|---|
| **Nama** | Ivan Andika Setyawan |
| **NIM** | `24031554085` |
| **Program Studi** | S1 Sains Data |
| **Fakultas** | Matematika dan Ilmu Pengetahuan Alam |
| **Universitas** | Universitas Negeri Surabaya |
| **Mata Kuliah** | Graf Sains Data |

## Deskripsi Proyek

Proyek ini merupakan pengerjaan Ujian Tengah Semester (UTS) mata kuliah Graf Sains Data yang menggunakan dataset **RetailRocket** untuk menganalisis interaksi pengguna dengan produk dan membangun sistem rekomendasi berbasis graf.

Data interaksi direpresentasikan menggunakan Neo4j, kemudian dianalisis melalui Vector Space Modelling (VSM), perhitungan kemiripan antar-item, serta pendekatan K-Nearest Neighbors (KNN). Kinerja rekomendasi dievaluasi menggunakan metrik Hit@5 dan NDCG@5.

## Tujuan

- Mengolah data interaksi pengguna berdasarkan periode waktu yang ditentukan.
- Merepresentasikan interaksi pengguna dan produk dalam bentuk graf menggunakan Neo4j.
- Menganalisis proyeksi User-Item dan Item-Item menggunakan Vector Space Modelling.
- Menghitung similarity antar-item dan menyimpannya sebagai relationship dalam graf.
- Menghasilkan rekomendasi produk menggunakan KNN.
- Mengevaluasi hasil rekomendasi menggunakan Hit@5 dan NDCG@5.

## Dataset

Dataset yang digunakan adalah **RetailRocket E-commerce Dataset**, yang berisi catatan interaksi pengguna dengan produk.

Beberapa atribut utama yang digunakan:

| Atribut | Keterangan |
|---|---|
| `timestamp` | Waktu terjadinya interaksi |
| `visitorid` | ID unik pengunjung |
| `event` | Jenis interaksi pengguna |
| `itemid` | ID unik produk |
| `transactionid` | ID transaksi, jika tersedia |

Jenis interaksi yang dianalisis meliputi `view`, `addtocart`, dan `transaction`.

Sumber dataset: [RetailRocket E-commerce Dataset — Kaggle](https://www.kaggle.com/datasets/retailrocket/ecommerce-dataset)

## Metodologi

1. **Data Wrangling dan Filtering** — Memfilter interaksi berdasarkan periode P1 dan P2 yang ditentukan.
2. **Graph Construction** — Membentuk node `Visitor` dan `Item`, serta relationship interaksi pada Neo4j.
3. **Graph Exploration** — Menganalisis komposisi node dan relationship.
4. **Vector Space Modelling** — Membentuk representasi matriks interaksi User-Item dan Item-User.
5. **Similarity Analysis** — Menghitung kemiripan antar-item berdasarkan representasi interaksi.
6. **Graph Similarity Storage** — Menyimpan hasil similarity ke Neo4j menggunakan relationship `SIMILAR_TO`.
7. **Recommendation** — Menghasilkan kandidat rekomendasi menggunakan KNN dengan nilai \(k=5\).
8. **Evaluation** — Mengevaluasi rekomendasi menggunakan Hit@5 dan NDCG@5.

## Teknologi yang Digunakan

- Python
- Neo4j
- Cypher Query Language
- Pandas
- NumPy
- SciPy
- NetworkX
- Scikit-learn
- Matplotlib

## Hasil dan Evaluasi

Hasil analisis mencakup karakteristik matriks VSM, pemilihan proyeksi graf, hasil similarity antar-item, rekomendasi produk, serta evaluasi rekomendasi.

Metrik evaluasi yang digunakan:

- **Hit@5:** Mengukur apakah terdapat setidaknya satu item relevan pada lima rekomendasi teratas.
- **NDCG@5:** Mengukur kualitas urutan rekomendasi dengan mempertimbangkan relevansi dan posisi item.

Hasil numerik dan pembahasan lengkap dapat dilihat pada notebook yang tersedia di repository ini.

## Cara Menjalankan

1. Clone repository:

   ```bash
   git clone [URL_REPOSITORY]
   ```

2. Masuk ke folder repository:

   ```bash
   cd [NAMA_FOLDER]
   ```

3. Buat dan aktifkan virtual environment sesuai sistem operasi yang digunakan.

4. Instal dependensi:

   ```bash
   pip install -r requirements.txt
   ```

5. Jalankan Neo4j dan sesuaikan konfigurasi koneksi database.

6. Buka notebook menggunakan Jupyter Notebook atau JupyterLab, kemudian jalankan sel sesuai urutan.

**Catatan:** Pastikan dataset tersedia di lokasi yang sesuai dan kredensial Neo4j tidak disimpan langsung dalam repository publik.

## Penutup

Repository ini disusun sebagai dokumentasi pengerjaan UTS Graf Sains Data, mulai dari pengolahan data, pemodelan graf, analisis kemiripan, hingga evaluasi sistem rekomendasi produk.

---

**Ivan Andika Setyawan**  
S1 Sains Data — Universitas Negeri Surabaya 
