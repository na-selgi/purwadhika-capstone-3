# purwadhika-capstone-3
**Konteks**

Di suatu perusahaan E-commerce, pemahaman yang mendalam tentang perilaku pelanggan sangat penting untuk kesuksesan jangka panjang. Pergantian pelanggan atau churn merupakan salah satu masalah utama yang dihadapi perusahaan dalam menjaga keberlanjutan dan pertumbuhan bisnis mereka. Oleh karena itu, penting untuk memiliki pemahaman yang baik tentang dinamika yang mempengaruhi tingkat pergantian pelanggan serta langkah-langkah yang dapat diambil untuk mengurangi risiko pergantian tersebut.

**Problem Statement**

Perusahaan menghadapi tantangan dalam mengidentifikasi dan memprediksi potensi pergantian pelanggan (Customer Churn). Dengan mempertimbangkan beberapa variabel seperti jarak antara gudang perusahaan dengan alamat pelanggan, jumlah perangkat yang terdaftar oleh pelanggan, kategori pesanan yang disukai pelanggan, skor kepuasan pelanggan, dan beberapa variabel lainnya. 

Dengan memahami variabel-variabel ini, maka divisi analisis data ditugaskan untuk mengembangkan model prediksi yang dapat mengklasifikasikan pelanggan sebagai "Churn" atau "Non-Churn" dengan tingkat akurasi yang tinggi. Dengan demikian, perusahaan dapat mengambil tindakan pencegahan yang sesuai untuk mempertahankan pelanggan yang rentan beralih dan meningkatkan retensi pelanggan secara keseluruhan.

Masalah ini penting karena pengaruhnya terhadap kesehatan keuangan perusahaan dan pertumbuhan jangka panjangnya. Tingkat pergantian pelanggan yang tinggi menandakan bahwa ada ketidakpuasan atau kebutuhan yang tidak terpenuhi yang perlu ditangani oleh perusahaan. Dengan mempertahankan pelanggan yang ada, perusahaan dapat menghemat biaya pemasaran dan akuisisi pelanggan baru, sambil memperkuat basis pelanggan yang sudah ada.

**Tujuan**

Maka berdasarkan context dan permasalahan tersebut, perusahaan membutuhkan kemampuan memprediksi kemungkinan pelanggan yang dapat churn dikemudian hari. Hal tersebut bertujuan agar pendapatan perusahaan tidak akan berkurang dikemudian hari kare terjadinya Customer Churn.

Selain itu, perusahaan juga ingin mengetahui faktor dan variabel apa saja yang menyebabkan terjadinya Customer Churn. Dengan mengetahui hal tersebut perusahaan dapat membuat rencana yang lebih baik untuk mendekati pelanggan agar tetap loyal terhadap layanan yang diberikan oleh perusahaan.

**Dataset**

Berikut adalah variabel-variabel yang terdapat dalam dataset.

* **Tenure** : masa jabatan pelanggan
* **WarehouseToHome** : gudang ke rumah pelanggan
* **NumberOfDeviceRegistered** : jumlah perangkat yang terdaftar
* **PreferedOrderCat** : kategori pesanan pilihan pelanggan dalam sebulan terakhir
* **SatisfactionScore** : skor kepuasan
* **MaritalStatus** : status pernikahan
* **NumberOfAddress** : nomor alamat
* **Complain** : komplain
* **DaySinceLastOrder** : hari sejak pesanan terakhir
* **CashbackAmount** : jumlah uang kembalian
* **Churn** : churn

Data yang dimiliki mencakup berbagai variabel yang berkaitan dengan perilaku dan karakteristik pelanggan. Setiap baris dalam dataset mewakili informasi tentang satu pelanggan, sementara setiap kolom merepresentasikan atribut atau fitur tertentu yang dapat digunakan untuk memprediksi tingkat churn pelanggan. Variabel-variabel seperti tenure, preferensi pesanan, skor kepuasan, dan jumlah keluhan dapat memberikan wawasan yang berharga tentang faktor-faktor yang mempengaruhi keputusan pelanggan untuk beralih. Dengan memahami data ini, kita dapat mengembangkan model prediksi yang tepat untuk mengidentifikasi pelanggan yang berisiko beralih dan mengambil tindakan yang sesuai untuk mempertahankan mereka.

**hasil**
Classification Report Model Tuned: 
               precision    recall  f1-score   support

           0       0.98      0.88      0.93       646
           1       0.63      0.90      0.74       143

    accuracy                           0.88       789
   macro avg       0.80      0.89      0.83       789
weighted avg       0.91      0.88      0.89       789

Precision dan Recall:

Precision (Ketepatan): Dari semua pelanggan yang diprediksi akan churn oleh model, sekitar 63% di antaranya benar-benar akan churn.
Recall (Ketepatan Deteksi): Model berhasil mengidentifikasi sekitar 91% dari semua pelanggan yang sebenarnya akan churn.
F1-score: F1-score untuk kelas 1 adalah 0.74, yang merupakan rata-rata dari precision dan recall. F1-score yang baik menunjukkan bahwa model memiliki keseimbangan yang baik antara precision dan recall.

Accuracy: Model ini mampu memprediksi dengan benar sekitar 89% dari semua pelanggan apakah mereka akan churn atau tidak. Ini memberikan gambaran seberapa baik model dapat mengklasifikasikan pelanggan secara keseluruhan.

**Kesimpulan:**  
1. Model yang telah dituning memiliki kinerja yang baik dalam memprediksi churn.
2. Precision yang tinggi untuk kelas 0 (non-churn) menunjukkan bahwa model dapat dengan baik mengidentifikasi pelanggan yang tidak akan churn.
3. Recall yang tinggi untuk kelas 1 (churn) menunjukkan bahwa model mampu mengidentifikasi sebagian besar pelanggan yang sebenarnya churn.
4. Dengan demikian, model ini dapat menjadi alat yang berguna bagi perusahaan dalam mengidentifikasi pelanggan yang berpotensi churn dan mengambil tindakan preventif untuk mempertahankan mereka.
   
Dengan menggunakan model yang telah dibuat, perusahaan dapat memperkirakan pelanggan yang berpotensi untuk melakukan churn. Dengan demikian, perusahaan dapat mengambil langkah-langkah yang tepat untuk mempertahankan pelanggan-pelanggan ini.

Perusahaan dapat memperhitungkan keuntungan tambahan yang diperoleh dari pelanggan yang dipertahankan dengan menggunakan model. Kita dapat memperkirakan keuntungan tambahan dari pelanggan yang tidak melakukan churn dengan cara mengestimasi nilai seberapa banyak mereka berbelanja di masa mendatang.

Misalnya, dengan model ini, perusahaan berhasil mempertahankan sekitar 91% dari pelanggan yang sebenarnya akan melakukan churn. Dari 143 pelanggan yang sebenarnya akan churn, sekitar 130 di antaranya berhasil dipertahankan.

Jika kita asumsikan bahwa rata-rata pendapatan tahunan dari setiap pelanggan adalah Rp 5.000.000,-, maka dengan mempertahankan 130 pelanggan tersebut, perusahaan dapat memperoleh pendapatan tambahan sebesar Rp 650.000.000,-.

**Recomendation**

**Rekomendasi untuk Model:**

1. Penambahan Data: Model dapat diperbaiki dengan menambahkan lebih banyak data pelanggan churn dan tidak churn jika memungkinkan. Semakin banyak data yang digunakan untuk melatih model, semakin baik kinerjanya.
2. Penyetelan Hyperparameter: Melakukan penyetelan lebih lanjut pada hyperparameter model dapat meningkatkan performa model. Hal ini dapat dilakukan dengan menggunakan teknik seperti GridSearchCV untuk mencari kombinasi hyperparameter yang optimal.
3. Peningkatan Feature Engineering: Mungkin terdapat fitur-fitur baru yang dapat diekstraksi dari data yang ada, atau fitur-fitur yang ada dapat diubah atau dikombinasikan untuk meningkatkan keakuratan model.

**Rekomendasi untuk Perusahaan:**

1. Implementasi Model: Model yang telah disesuaikan dapat diimplementasikan dalam sistem perusahaan untuk membantu mengidentifikasi pelanggan yang berpotensi churn dengan lebih akurat.
2. Pelatihan Karyawan: Karyawan perusahaan, terutama yang terlibat dalam layanan pelanggan, dapat dilatih untuk menggunakan model ini sebagai alat untuk mengidentifikasi pelanggan yang memerlukan perhatian khusus.
3. Monitoring Berkala: Model perlu dipantau secara berkala untuk memastikan bahwa kinerjanya tetap optimal seiring waktu. Pemantauan ini dapat membantu dalam mengidentifikasi perubahan tren atau perubahan perilaku pelanggan yang mungkin memengaruhi performa model.
4. Pengembangan Strategi Retensi: Informasi yang diberikan oleh model dapat digunakan untuk mengembangkan strategi retensi pelanggan yang lebih efektif. Misalnya, menawarkan insentif khusus kepada pelanggan yang terindikasi berpotensi churn untuk mendorong mereka untuk tetap setia kepada perusahaan.
