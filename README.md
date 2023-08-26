# Project 1 - Credit Risk Machine Learning Project

## Stage 0
### Background
Sebuah perusahaan memiliki client lending company bernama “AZ”. Project bersama client adalah membangun sebuah model untuk memprediksi credit risk peminjam berdasarkan data yang dimiliki company. Data tersebut merupakan data credit peminjam yang diterima dan ditolak. Model yang akan dibuat bermaksud untuk membuat keputusan peminjaman berbasis data dengan subprime mortgages (jenis pinjaman yang diberikan kepada peminjam dengan nilai credit buruk).
![image](https://github.com/hadasadida/Project-1---Credit-Risk-Machine-Learning-Project/assets/124650679/54b28bca-b1e5-485b-a95c-dcfb2f2f037a)

## Stage 1
### Exploratory Data Analysis
#### Descriptive Statistic
- Dataset memiliki 75 kolom dan 466285 baris.
- Terdapat 17 kolom yang tidak memiliki data sama sekali sehingga dilakukan penghapusan kolom tersebut.
- Terdapat 5 kolom yang memiliki missing value paling banyak sehingga dapat dilakukan penghapusan kolom tersebut.
- Belum terdapat kolom target yang spesifik sehingga perlu dilakukan feature engineering.
#### EDA 
![image](https://github.com/hadasadida/Project-1---Credit-Risk-Machine-Learning-Project/assets/124650679/c3c6d07d-cb8e-4658-bb69-8e36d28d0121)

Berdasarkan grafik di atas, grade B memiliki jumlah paling banyak dibandingkan dengan grade lainnya, namun memiliki selisih paling rendah dengan grade C dibanding dengan grade yang lain.
Sedangkan grade G memiliki jumlah paling sedikit dibandingkan dengan grade lainnya. 

![image](https://github.com/hadasadida/Project-1---Credit-Risk-Machine-Learning-Project/assets/124650679/d9dcb818-5636-4da9-a0c0-59d5e6859304)

Term (jumlah pembayaran atas pinjaman) paling banyak berada pada 36 months. Peminjam lebih banyak membayar pinjaman dalam waktu 36 months atau 3 tahun.  

![image](https://github.com/hadasadida/Project-1---Credit-Risk-Machine-Learning-Project/assets/124650679/33dda4c3-c69b-4e54-ad4f-7d0e45371f69)

Jumlah peminjam dengan status peminjaman “Current (melakukan pembayaran tepat waktu)” lebih banyak dibandingkan dengan status pinjaman yang lain. Sedangkan status peminjaman “charged: off (dikenakan biaya)” memiliki jumlah peminjam paling sedikit. 

![image](https://github.com/hadasadida/Project-1---Credit-Risk-Machine-Learning-Project/assets/124650679/3a5cdd2f-1299-4562-b643-e45be7b15fcc)

Jumlah peminjam dengan status verifikasi “verified (telah diverifikasi)” lebih banyak dibandingkan dengan status verifikasi yang lain. Jumlah peminjam dengan status verifikasi “source verified (sumber pendapatan diverifikasi)” dan “not verified (tidak diverifikasi)” hampir sama.

## Stage 2
### Data Preprocessing
#### Missing Value 
- Menghapus kolom yang tidak memiliki nilai.
- Menghapus kolom yang memiliki missing value terbanyak.
- Mengisi missing value dengan kolom tipe float/int dengan median dan modus untuk tipe object
#### Duplicate Data
- Tidak ada data duplikat dalam dataset.
#### Handle Outlier 
- Dilakukan handling outlier dengan zscore.
#### Featrue Engineering
#### Feature Encoding
- Dilakukan label encoding dan one hot encoding pada kolom tipe kategorical. Kolom-kolom tersebut hanya kolom yang memiliki unique value dengan jumlah tidak terlalu besar. 
#### Feature Selection
- Sebelum dilakukan feature selection, dilakukan penambahan kolom/feature target yang dikelompokkan berdasarkan kolom grade sehingga menjadi 0 (dengan score bagus) dan 1 (dengan score buruk). Kemudian dilakukan feature selection pada beberapa kolom yang digunakan untuk pemodelan. 
#### Class Imbalace 
- Pada kolom / feature target jumlah peminjam dengan score bagus dan score buruk tidak seimbang sehingga dilakukan class imbalance dengan SMOTE. 

## Stage 3
### Modeling
Untuk melakukan modeling, digunakan 70% labelled dataset dan model yang akan digunakan adalah Logistic Regression. Model ini akan memprediksi kemungkinan pembayaran kembali pinjaman untuk 30% pinjaman yang tersisa (test set). Dihasilkan:
#### Sebelum Tuning
![image](https://github.com/hadasadida/Project-1---Credit-Risk-Machine-Learning-Project/assets/124650679/176d088c-405d-4b3f-a256-8b22bffffef5)
#### Setelah Tuning
![image](https://github.com/hadasadida/Project-1---Credit-Risk-Machine-Learning-Project/assets/124650679/5d890e7d-2699-42cd-8e3f-00b8d354e9cd)
#### Fature Importance 
![image](https://github.com/hadasadida/Project-1---Credit-Risk-Machine-Learning-Project/assets/124650679/ec3e620a-299f-4c9a-86e5-0e75c233827c)


### Conclusion





















