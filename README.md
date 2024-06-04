# Image Compression dengan SVD

Artikel ini membahas tentang penerapan Singular Value Decomposition (SVD) dalam kompresi gambar.

## A. Definisi dan Teori

SVD adalah faktorisasi matriks yang memecah matriks menjadi tiga matriks: U, Σ, dan V.

- **U** adalah matriks orthonormal eigenvector dari operasi A<sup>T</sup>A.
- **Σ** adalah matriks diagonal yang berisi akar eigenvalue dari operasi A<sup>T</sup>A.
- **V** adalah matriks orthonormal eigenvector dari operasi AA<sup>T</sup>.

Matriks A dapat ditulis sebagai A = UΣV<sup>T</sup>.

## B. Konsep SVD dalam Image Compression

Gambar dapat dianggap sebagai matriks. SVD dapat digunakan untuk mengompresi gambar dengan cara:

- **Mengambil eigenvalue dan eigenvector yang signifikan:** Eigenvalue dan eigenvector yang memiliki nilai kecil tidak signifikan dan dapat dihilangkan.
- **Merekonstruksi gambar:** Gambar direkonstruksi menggunakan eigenvalue dan eigenvector yang signifikan.

## C. Implementasi dan Analisis

Implementasi kompresi gambar dengan SVD dijelaskan menggunakan Python. Langkah-langkahnya adalah:

1. **Mengimport library:** Pillow, numpy, pandas, matplotlib, dan requests.
2. **Memuat gambar:** Mengambil gambar dari internet dan menyimpannya sebagai matriks A.
3. **Melakukan SVD:** Menghitung SVD dari matriks A dengan menggunakan fungsi `np.linalg.svd()`.
4. **Mengompresi gambar:** Mengambil elemen-elemen matriks U, Σ, dan V<sup>T</sup> dengan rasio tertentu.
5. **Menampilkan hasil:** Menampilkan gambar hasil kompresi dengan rasio yang berbeda.

## Kesimpulan

SVD dapat digunakan untuk mengompresi gambar dengan cara membuang informasi yang tidak signifikan. Hasil kompresi dapat disesuaikan dengan rasio yang digunakan. Semakin kecil rasio yang digunakan, semakin tinggi tingkat kompresi dan semakin rendah kualitas gambar.

## Informasi Tambahan

- Kode lengkap untuk implementasi kompresi gambar dengan SVD dapat diakses pada [\[link ke repository kode\]](https://github.com/ZufarSyaafie/SVD-Image-Compressing/blob/e49d048617fa32d44e42489cd03459aa80823054/SVD.ipynb).
- Artikel ini hanya membahas dasar-dasar kompresi gambar dengan SVD. Anda dapat mempelajari lebih lanjut tentang topik ini di [\[link ke sumber belajar tambahan\]](https://ocw.mit.edu/courses/18-06-linear-algebra-spring-2010/).
