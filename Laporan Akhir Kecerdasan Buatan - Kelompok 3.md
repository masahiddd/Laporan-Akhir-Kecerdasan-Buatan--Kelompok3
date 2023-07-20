# Laporan Akhir Kecerdasan Buatan - Kelompok 3

### Anggota Kelompok :

	1. Andika Gempar Masahid - NIM 3.34.21.1.03
	1. Fauzan Widyanursasongko Yusuf - NIM 3.34.21.1.11

## Domain Proyek

Tempat tinggal seperti rumah adalah kebutuhan primer bagi manusia untuk berlindung dan hidup menetap. Tempat tinggal ini memiliki nilai tergantung dari karakteristik yang dimiliki seperti lokasi, luas, jumlah kamar, jumlah kamar mandi, perabotan, serta fitur lainnya. Harga dari setiap rumah diukur dari nilai yang dimiliki oleh rumah tersebut. Namun, harga ini tidak selalu pasti dan sulit untuk melakukan prediksi akurat secara manual. Faktor ketidakpastian perlu dikurangi oleh perusahaan properti rumah dengan membangun sistem prediksi yang dapat menentukan berapa harga jual yang pantas untuk karakteristik rumah tertentu.

Dalam mencapai hal tersebut, maka dilakukan penelitian untuk memprediksi harga jual rumah menggunakan model *Data Visualization*. Diharapkan model ini mampu memprediksi harga jual yang sesuai dengan harga pasar. Prediksi ini nantinya dijadikan acuan bagi konsumen untuk mempertimbangkan dalam membeli sebuah rumah.

## Business Understanding

Proyek ini dibuat dengan karakteristik bisnis sebagai berikut :

- Konsumen dapat mengetahui secara mudah harga rumah dengan spesifikasi yang berbeda
- Rumah yang dijual oleh suatu properti dapat bersaing di pasaran karena harga jual yang sesuai dengan fitur yang tercantum
- Dengan adanya prediksi, Arsitektur dapat membangun project rumah dengan minimum budget tetapi maksimal output

#### Problem Statements

Berdasarkan persoalan yang telah dijabarkan sebelumnya problem statements dari proyek ini yaitu sebagai berikut.

	1. Faktor-faktor apa saja yang berdampak besar terhadap harga rumah ?
	1. Fitur apa yang paling berpengaruh terhadap harga jual rumah?
	1. Bagaimana cara memproses data agar dapat digunakan dengan baik oleh model?

#### Goals

Tujuan yang hendak dicapai dari proyek ini adalah sebagai berikut

	1. Mengetahui fitur yang paling berpengaruh pada harga jual rumah.
	1. Melakukan persiapan data untuk dapat digunakan oleh model.
	1. Membuat model machine learning yaitu Data Visualization yang dapat memprediksi harga jual rumah seakurat mungkin berdasarkan karakteristik tertentu.

#### Solution Statements

Solusi yang diajukan untuk menyelesaikan masalah yang telah diuraikan adalah sebagai berikut.

 	1. Melakukan analisis deskriptif untuk mengetahui pola dan informasi yang tersimpan di 	data mengenai fitur atau spesifikasi yang mempengaruhi harga rumah.
 	2. Melakukan Proses *Preprocessing* seperti :
     - Melakukan visualisasi fitur kategorikal untuk melihat data menggunakan berbagai jenis bagan dan grafik
     - Menggunakan Distribusi Nilai Numerik untuk variabel acak yang dapat mengambil nilai numerik apa pun. Diantaranya Menghitung probabilitas dari variabel acak mengambil nilai tertentu, seperti membandingkan distribusi nilai dari dua atau lebih variabel acak, Menentukan apakah serangkaian data mengikuti distribusi tertentu, dan Mengembangkan model statistik untuk data.
     - Melakukan *Encoding* terhadap kolom yang bertipe kategorikal menggunakan fungsi Map.

3. Melakukan pemilihan model.
   - Memilih 5 algoritma yang menghasilkan model dengan performa terbaik
   - Kinerja model terbaik tercermin dalam kesalahan kuadrat rata-rata (MSE), kesalahan kuadrat akar rata-rata (RMSE), dan kesalahan R-kuadrat (R2).
4. Lakukan proses manipulasi data untuk menggabungkan kolom-kolom yang mempengaruhi akurasi prediksi harga rumah 

## Data Understanding

Dataset yang digunakan pada proyek ini diperoleh dari Kaggle. Silahkan kunjungi tautan berikut [Housing Price Prediction](https://www.kaggle.com/datasets/harishkumardatalab/housing-price-prediction) untuk mengakses dataset yang dipakai. Adapun variabel-variabel yang terdapat pada dataset adalah sebagai berikut :

 1. **Price** : harga rumah

 2. **Area :** Luas total rumah dalam meter persegi

 3. **Bedrooms :** Jumlah kamar tidur dalam rumah

 4. **Bathrooms :** Jumlah kamar mandi dalam rumah

 5. **Stories :** Jumlah lantai di dalam rumah

 6. **Mainroad :** Apakah rumah terhubung dengan jalan utama

 7. **Guestroom :** Apakah rumah memiliki ruang tamu

 8. **Basement :** Apakah rumah memiliki ruang bawah tanah

 9. **Hot Water Heating :** Apakah rumah memiliki sistem pemanas air panas

 10. **Air Conditioning :** Apakah rumah memiliki sistem pendingin udara

 11. **Parking :** Jumlah ruang parkir yang tersedia didalam rumah

 12. **Prefarea :** Apakah rumah tersebut terletak di area yang disukai

 13. **Furnishing Status :** Status perabotan rumah

       

​																					Tabel 1. Ringkasan Statistik Deskriptif

![image-20230720105815847](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20230720105815847.png)

Pada tahap *Data Understanding* dilakukan analisis data eksploratif untuk mendapatkan wawasan tentang karakteristik data, memahami struktur data, dan mengidentifikasi potensi masalah atau kesalahan yang mungkin terjadi. Kegiatan Data Understanding yang dilakukan pada Proyek ini antara lain :

- Memberikan informasi seperti jumlah data, *missing value*, duplikasi data, korelasi antar kolom, dan sebaran data.
- Melakukan manipulasi data karena *machine learning* dapat dilakukan dengan angka, hanya angka. Jadi pada dasarnya mengubah data menjadi angka.
- Melakukan visualisasi data untuk mengetahui korelasi dan sebaran data.

​																 Gambar 1. Visualisasi Korelasi Data menggunakan Heatmap

![image-20230720110053648](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20230720110053648.png)



​																			Gambar 2. Visualisasi Data pada Data

![image-20230720110257482](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20230720110257482.png)![image-20230720110316430](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20230720110316430.png)

![image-20230720110335195](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20230720110335195.png)

![image-20230720110455303](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20230720110455303.png)

## Data Preparation

Teknik data preparation yang dilakukan pada proyek ini adalah sebagai berikut :

1. Feature Selection : Melakukan pemilihan atribut yang tepat dan memiliki kontribusi dalam memprediksi harga rumah.
2. Data Splitting: Membagi dataset menjadi data latih dan data uji. Pada proyek ini perbandingan data latih dan data uji adalah 80 : 20.

## Modelling 

Pada tahap ini dilakukan proses pelatihan untuk mendapatkan model dengan performa terbaik. HistGradientBoostingRegressor, LGBMRegressor, PoissonRegressor. algoritma tersebut memiliki kecenderungan untuk memberikan hasil yang baik dalam prediksi harga rumah.

 1. Hist Gradient Boosting Regressor

    Hist Gradient Boosting Regressor adalah algoritma yang menggabungkan model yang lemah(weak learners) menjadi model yang kuat. model yang lemah seperti model regresi atau klasifikasi sederhana. Hist Gradient Boosting Regressor mengoptimalkan suatu fungsi objektif dengan mengevaluasi gradient pada setiap titik. Fungsi objektif yang umum digunakan dalam Hist Gradient Boosting Regressor adalah fungsi Mean Squared Error (MSE) untuk regresi dan fungsi Log-Loss untuk klasifikasi.

 2. LGBM Regressor

    LGBM Regressor adalah kerangka kerja peningkatan gradien sumber terbuka yang didasarkan pada algoritme pembelajaran pohon dan dirancang untuk memproses data lebih cepat dan memberikan akurasi yang lebih baik. Itu dapat menangani kumpulan data besar dengan penggunaan memori yang lebih rendah dan mendukung pembelajaran terdistribusi. LGBM dapat digunakan untuk regresi, klasifikasi, dan peringkat.

 3. Poisson Regressor

    Poisson Regressor adalah salah satu regresi nonlinier yang sering digunakan untuk memodelkan hubungan antara variabel respon yang berupa data diskrit dengan variabel prediktor yang berupa data diskrit atau kontinu. Regresi Poisson merupakan penerapan dari Generalized Linear Model (GLM).Generalized Linear Model (GLM) merupakan perluasan dari model regresi umum untuk variabel respon yang memiliki sebaran eksponensial. Regresi Poisson digunakan untuk menganalisis data count (berjenis diskrit). Pada regresi Poisson diasumsikan variabel respon berdistribusi Poisson dan tidak terjadi multikolinearitas diantara masingmasing variabel prediktor (X).

    ## Evaluation

    - Metrik evaluasi yang digunakan adalah *Mean Square Error* (MSE), *Root Mean Square Error* (RMSE), dan *R Square* (R2 Score)

    - MSE mengurangi nilai data aktual dari data perkiraan dan hasilnya dikuadratkan (*kuadrat*) dan dijumlahkan dan dibagi dengan jumlah data yang ada.  Rumus dari MSE adalah sebagai berikut 
      $$
      MSE = \frac{1}{n} \Sigma_{i=1}^n({y}-\hat{y})^2
      $$
      Diketahui:

      - n = Jumlah Data
      - yi = *Actual Value* / Nilai Sebenarnya
      - ŷi = *Predicted Value* / Nilai Prediksi

    - RMSE adalah jumlah kesalahan kuadrat atau perbedaan antara nilai aktual dan nilai prediksi. Satu-satunya cara untuk menghitungnya adalah dengan melakukan root pada mse dengan fungsi *np.sqrt*.  Rumus dari RMSE adalah sebagai berikut.
      $$
      RMSE = \sqrt{(\frac{1}{n})\sum_{i=1}^{n}(y_{i} - x_{i})^{2}}
      $$
      Diketahui:

      - n = Jumlah Data
      - yi = *Actual Value* / Nilai Sebenarnya
      - ŷi = *Predicted Value* / Nilai Prediksi

    - Nilai skor R2 digunakan sebagai ukuran seberapa baik garis regresi mendekati nilai data asli yang ditentukan oleh model.  Rumus dari R2 Score adalah sebagai berikut.
      $$
      R^2 = 1 - {SS_R \over SS_T} =  1 - {\sum_{i} (y_i - ŷ_p) ^ 2 \over \sum_{i} (y_i - ȳ) ^ 2}
      $$

      - SSR : Kuadrat dari selisih nilai Y prediksi dengan nilai rata-rata Y = ∑ (Ypred – Yrata-rata)²
      - SST : Kuadrat dari selisih nilai Y aktual dengan nilai rata-rata Y = ∑ (Yaktual – Yrata-rata)².

      Setelah melalui tahap pelatihan dan evaluasi menggunakan MSE, RMSE, dan R Square, diperoleh hasil bahwa algoritma **Random Forest Classification** memiliki performa yang paling baik seperti ditunjukan Tabel 3. Maksud performa yang paling baik adalah memiliki nilai MSE dan RMSE yang mendekati nilai 0, serta memiliki nilai R2 Score yang mendekati nilai 1.

      |  id  | Model Name                       | R2 Score  | RMSE       |
      | :--: | :------------------------------- | --------- | ---------- |
      |  1   | Hist Gradient Boosting Regressor | 0.61;0.66 | 1263526.07 |
      |  2   | LGBM Regressor                   | 0.60;0.65 | 1281544.25 |
      |  3   | Poisson Regressor                | 0.59;0.63 | 1306998.52 |

    ## Conclussion

    1. Berdasarkan hasil pengukuran, terdapat 13 Fitur yaitu *Price, Area, Bedrooms, Bathrooms, Stories, Mainroad, Guestrooms, Basement, Hot Water Heating, Air Conditioning, Parking, Prefarea, Furnishing Status.* 
    2. Berdasarkan hasil pengujian model, diperoleh hasil bahwa algoritma Hist Gradient Boosting Regressor memiliki performa yang paling baik yaitu memiliki nilai RMSE paling kecil dan R2 Score paling besar.
    3. Menghilangkan nilai-nilai outlier dari dataset, agar dapat meningkatkan performa atau skor *machine learning*. Outlier adalah nilai yang secara signifikan berbeda dari nilai-nilai lain dalam dataset, dan dapat mempengaruhi analisis atau model pembelajaran mesin. Dengan menghapus nilai-nilai outlier, maka dapat membersihkan dataset dari gangguan yang tidak diinginkan dan meningkatkan akurasi.
    4. Rekayasa fitur adalah proses memanipulasi atau mengubah fitur-fitur dalam dataset untuk meningkatkan pemahaman dan kinerja dalam menganalisis data tersebut. Dengan melakukan rekayasa fitur, maka pemahaman komputer terhadap dataset akan meningkat dan analisis data akan menjadi lebih baik.

    ## Referensi 

    [1] Febriyanto, F. D., Endroyono, E., & Kusnendar, Y. (2023). House Price Prediction using Multiple Linear Regression and KNN. *JAREE (Journal on Advanced Research in Electrical Engineering)*, *7*(1).

    [2] Borde, S., Rane, A., Shende, G., & Shetty, S. (2017). Real estate investment advising using machine learning. *International Research Journal of Engineering and Technology (IRJET)*, *4*(3), 1821-1825.

    [3] Imran, I., Zaman, U., Waqar, M., & Zaman, A. (2021). Using machine learning algorithms for housing price prediction: the case of Islamabad housing data. *Soft Computing and Machine Intelligence*, *1*(1), 11-23.

    ### 

    