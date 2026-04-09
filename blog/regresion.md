# Navigasi
- **Home** : [Home](index.md)
---
# Pengertian regresion

Regersion merupakan metode yang digunakan untuk mendeteksi tren grafik yang berbasi plot untuk menghasilkan perhitungan sesuai dengan parameter atau fitur sebagai variabel dan teta $\theta$  sebagai bobot yang berubah tiap pelatihan.

Berikut bentuk dari bentuk persamaan _regresion_ linier dengan 1 variabel atau 1 fitur:

$$y = \theta_0 + \theta \cdot X$$
Dalam regresion ini ada dua bentuk yang digunakan:
1. Regresion Linier 
	Regresion Linier merupakan metode yang digunakan pada perhitungan dengan target yang bersifat numerik dan saling korelasi atau bisa di sebut juga dengan persaman garis yang menjadi perhitungan pada regresion linier ini denga variabel y sebagai target dan variabel x sebagai fitur.
	$$y = \theta_0 + \theta_1 \cdot x_1 + \theta_2 \cdot x_2 + ...$$
	**keterangan:**
	- y : variabel nilai target.
	- x : variabel nilai fitur.
	- $\theta_0$ : sebagai konsanta
	- $\theta_{1,2,...}$ : sebagai koefisien.
2. Regresion Logistik 
	Regresion Logistik merupakan metode yang digunakan pada perhitungan dengan target yang bersifat kategori atau class, dia juga sama menggunakan pendekatan regresion linier sederhana tapi saat di akhir targetnya akan dijadikan dalam bentuk probabilitas dalam bentuk sigmoid. Rumus yang digunakan untuk regresion logistik ini adalah.
	**persamaan 1 :**
$$z = \theta_0 + \theta_1 \cdot x_1 + \theta_2 \cdot x_2 + ...$$
	**keterangan :** 
	- z : sebagai variabel yang nilainya akan di jadikan menjadi nilai pangkat nilai $e^{-z}$

	**persamaan 2 :**
	$$y = \frac{1}{1+e^{-z}}$$
	**keterangan :**
	- y: sebagai nilai akhir dalam bentuk probabilitas dalam rentang `0` sampai dengan `1`.
	- $e^{-1}$ : nilainya adalah $0.367879$
	- $e^1$ : nilainya adalah $2.71828$

# Regresion linier

Regresion linier merupakan sebuah cabang mesing learning tradisional yang bersifat **supervised learning**, yang mana dia menggunakan hubungan dari persamaan garis lurus denga y sebagai target dan x sebagai fitur dengan memperhatikan perubaha dari koefisien tiap pergeseran atau perubahan dari persamaan garis tersebut.

Ada 2 teknik yang digunakan pada regresion linier :
- Teknik statistik.
- Teknik penggunaan bobot dan bias.

## Teknik statistik 

Penggunaan perhitungan ini menggunakan pendekatan **Ordinary Last Squares (OLS)**. Pendekatan merupakan teknik statistik untuk mencari parameter dengan menghitung:

* Rumus menghitung slope ($\theta_{1,2,3,...}$) :
$$\theta_{1,2,3,...} =\frac{n\sum(x\cdot y) - \sum x \cdot \sum y}{n\sum x^2 - (\sum x)^2}$$
* Rumus menghitung intercept $\theta_0$ :
$$\theta_0 = \frac{\sum y - \theta_{1,2,3,...}\cdot \sum x}{n}$$
- Rumus hitung cepat intecept untuk mencari nilai konstan $\theta_0$:
$$\theta_0 = \bar{y} + \theta_{1,2,3,...}\cdot\bar{x}$$
Dalam menyelesaikan atau mencari nilai kofesion dan konsanta nya secara statistik berikut algoritmanya :
1. Membuat tabel bantuan atau baru dengan kriteria rumus yang kita gunakan untuk mencari nilai $x\cdot y$, $x^2$, $y^2$, $x$, $y$.
2. Sudah membuat tabel lalu menghitung total keseluruhan dari masing-masing $x\cdot y$, $x^2$, $y^2$, $x$, $y$.
3. Mencari nilai rata-rata dari `y` dan `x`.
4. Menggunakan rumus untuk menghitung slop $\theta_{1,2,3,...}$ denga memasukan nilai nilai fitur tabel baru nya dari total keseluruhan masing masing $x\cdot y$, $x^2$, $y^2$, $x$, $y$.
5. Menggunakan rumus untuk menghitung intercept untuk mendapatkan nilai $\theta_0$.
6. Atau juga bisa menggunaka rumus untuk menghitung nilai konstan dengan menggunakan rata rata dari $\bar{y}$ dan $\bar{x}$.
7. Sesudah itu memasukan ke dalam persamaan regresion $\theta_0 + \theta_{1}\cdot x + ...=y$
8. Evaluasi prediksi.
