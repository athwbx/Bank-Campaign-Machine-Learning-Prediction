# Bank Campaign Machine Learning Prediction

by: Aryo Atha Rizaldi

## Bussiness Understanding
### **Context**

Data ini mencakup hasil dari kampanye pemasaran bank yang melibatkan panggilan telepon langsung ke rumah atau ponsel untuk mengajak orang menaruh deposit berjangka. Jika klien setuju untuk menaruh deposit, variabel target akan diset sebagai **'yes'**, dan jika tidak, akan diset sebagai **'no'**.

Target: 
* 0 : Tidak menaruh deposit 
* 1 : Menaruh deposit



### **Problem Statement**

Stakeholder: Tim Pemasaran, Penjualan dan Layanan Pelanggan, dan Manajemen

Proses kampanye penawaran deposit berjangka memerlukan alokasi waktu dan sumber daya finansial yang signifikan. Tanpa adanya penyaringan terlebih dahulu, jika bank memutuskan untuk menjangkau semua nasabah tanpa mempertimbangkan potensi mereka untuk menaruh deposit, hal ini dapat **mengakibatkan pemborosan sumber daya yang berharga** seperti uang yang dikeluarkan oleh bank dan waktu untuk menghubungi nasabah-nasabah tersebut. Oleh karena itu, dengan adanya **Machine Learning**, dapat meningkatkan efisiensi proses kampanye yang dilakukan oleh bank.  

**Machine Learning** akan membantu bank dalam **mengevaluasi dan memodelkan pola-pola kompleks dari data historis**, memungkinkan identifikasi faktor-faktor yang paling berpengaruh terhadap keputusan calon nasabah. Dengan pendekatan ini, bank dapat **meningkatkan efisiensi kampanye** pemasaran mereka, **mengoptimalkan penggunaan sumber daya**, dan secara **lebih tepat menargetkan kandidat** yang memiliki peluang tinggi untuk berinvestasi dalam deposit berjangka. Disini, **Machine Learning** dapat membantu bank untuk **menyaring calon nasabah** berdasarkan data dengan cermat, menargetkan mereka yang memiliki **potensi tertinggi** untuk menaruh deposit. Dengan pendekatan ini, bank berharap dapat mengoptimalkan penggunaan waktu dan biaya, sambil tetap fokus pada segmen nasabah yang lebih mungkin merespons secara positif terhadap penawaran deposit berjangka.


### **Goals**

Dalam menghadapi tantangan tersebut, bank memiliki keinginan untuk mengembangkan kemampuan prediktif guna memprediksi apakah seorang calon nasabah bersedia menaruh deposit atau tidak. Tujuannya adalah untuk dapat dengan baik **menargetkan kampanye pemasaran pada kandidat yang memiliki potensial tertinggi** untuk melakukan investasi dalam bentuk deposit berjangka. Dengan adanya bantuan dari **Machine Learning** ini, bank berharap dapat **meningkatkan efisiensi dan efektivitas** strategi pemasaran mereka, dapat mengurangi kerugian bank, dan mengarahkan upaya pada segmen nasabah yang paling mungkin memberikan respons positif terhadap tawaran deposit berjangka. Selain itu, bank juga tidak harus menghubungi setiap calon nasabah untuk mengurangi kerugian materiil dan waktu dengan bantuan dari **Machine Learning**.


### **Analytic Approach**

Rencananya adalah melakukan analisis mendalam terhadap data untuk **mengidentifikasi pola-pola** yang dapat **membedakan antara kandidat nasabah yang bersedia menaruh deposit dan yang tidak**. Selanjutnya **membangun sebuah model klasifikasi yang dapat menjadi alat prediktif** bagi bank, membantu dalam memperkirakan probabilitas bahwa seorang kandidat nasabah akan atau tidak akan menaruh deposit.

Pendekatan analitik yang akan diambil melibatkan **eksplorasi data** secara menyeluruh untuk mengungkap hubungan dan tren yang mungkin ada di antara variabel-variabel terkait. Selanjutnya, akan dilakukan **pemilihan fitur** dan **penyesuaian data** untuk mempersiapkannya sebagai **input bagi model klasifikasi**. Proses ini didesain untuk **meningkatkan akurasi prediksi** dan **mengidentifikasi faktor-faktor kunci** yang memengaruhi keputusan nasabah.

Dalam membangun model klasifikasi, akan digunakan teknik-teknik **Machine Learning** yang sesuai, seperti **Logistic Regression** atau **Decision Tree**, yang dapat memproses pola-pola kompleks dalam data. Model ini akan **diuji dan dievaluasi menggunakan data holdout yang tidak terlihat sebelumnya** untuk memastikan keandalan dan kinerja yang baik dalam memprediksi perilaku calon nasabah.

Dengan pendekatan analitik ini, bank berharap dapat memperoleh pemahaman mendalam tentang faktor-faktor kritis yang mempengaruhi keputusan nasabah dan menerapkan solusi yang tepat untuk meningkatkan efektivitas kampanye pemasaran mereka.


### **Metric Evaluation**

Type 1 error : **False Positive** (Nasabah diprediksi bisa deposit, tetapi aktualnya tidak deposit)   
Konsekuensi: Membuang waktu dan biaya kampanye untuk nasabah yang tidak berpotensial menaruh deposit

Type 2 error : **False Negative** (Nasabah diprediksi tidak bisa deposit, tetapi aktualnya berpotensi untuk deposit)  
Konsekuensi: Kehilangan kandidat nasabah potensial

Berikut adalah estimasi biaya yang akan dikeluarkan oleh bank untuk setiap false positive dan false negative:

* **False Positive**
Biaya yang akan dikeluarkan oleh bank untuk setiap false positive adalah biaya kampanye yang dikeluarkan untuk nasabah tersebut. Biaya kampanye ini dapat berupa biaya tenaga kerja, biaya media, dan biaya lainnya.

Berdasarkan penelitian yang dilakukan oleh McKinsey & Company, biaya kampanye pemasaran untuk produk perbankan di Indonesia diperkirakan mencapai Rp500 ribu per nasabah.

Dengan demikian, biaya yang akan dikeluarkan oleh bank untuk setiap false positive adalah Rp500.000.

* **False Negative**
Biaya yang akan dikeluarkan oleh bank untuk setiap false negative adalah potensi pendapatan yang hilang dari nasabah tersebut. Potensi pendapatan ini dapat berupa besaran deposit dari nasabah.

Menurut OJK Indonesia, minimal deposito bank adalah Rp. 8.000.000. Dengan demikian, potensi pendapatan yang hilang dari setiap false negative adalah Rp.8.000.000 per nasabah.

* **Perbandingan dengan Kehilangan Kandidat Nasabah Potensial**

Kehilangan kandidat nasabah potensial dapat berdampak negatif terhadap pendapatan bank dalam jangka panjang. Hal ini karena bank akan kehilangan kesempatan untuk menawarkan produk dan layanannya kepada nasabah tersebut.

Berdasarkan penelitian yang dilakukan oleh Frederick F. Reichheld & W. Earl Sasser, Jr., bank yang kehilangan satu nasabah berpotensi kehilangan pendapatan hingga Rp50 juta per tahun.

>**Apabila kita buat perhitungan False Positive, tanpa machine learning dan tanpa adanya kemungkinan kehilangan nasabah (karena semua nasabah dihubungi):**  
>Asumsi biaya yang dikeluarkan sesuai dengan statement diatas, yaitu Rp. 500.000/nasabah.  
>Banyak nasabah (total data test dan holdout tanpa adanya penyaringan terlebih dahulu): 2813 nasabah.   
>Apabila tanpa penyaringan, bank akan menghubungi semua nasabah tanpa adanya pertimbangan/guidance, bank akan mengeluarkan biaya sebanyak:  
>2813 nasabah x Rp. 500.000/nasabah = ± Rp. 1,406,500,000 (**± 1.4 miliar**) tanpa adanya kemungkinan pasti bahwa nasabah tersebut akan melakukan deposit. 

Hal ini kurang make sense apabila dilakukan, karena pengeluaran kasarnya, bank harus mengeluarkan biaya sebanyak ± **1.4 M** hanya untuk melakukan campaign, dan biaya yang dikeluarkan bank ini tidak sebanding dengan potensi pendapatan yang akan diperoleh dari nasabah tersebut, dan juga akan menyita waktu yang banyak untuk menghubungi nasabah tersebut. Maka dari itu, dengan mempertimbangkan konsekuensinya, fokus utama adalah mengembangkan model ini adalah **mengurangi False Negative** dan **meningkatkan False Positive**, karena bank akan mengalami **kerugian yang lebih besar apabila kehilangan kandidat nasabah potensial** apabila dibandingkan dengan kerugian biaya kampanye dan waktu. Tujuan utama adalah meningkatkan **Recall**, memaksimalkan identifikasi calon nasabah yang sebenarnya bersedia menaruh deposit, meskipun ada peningkatan false positive yang dapat diterima. Pendekatan ini diharapkan mencapai keseimbangan optimal antara efisiensi biaya kampanye dan pemeliharaan potensi nasabah yang dicari.  

**Sumber**:

[McKinsey & Company, "The Data-Driven Organization: How Analytics and Machine Learning Are Transforming Business"](https://www.mckinsey.com/capabilities/quantumblack/our-insights/the-data-driven-enterprise-of-2025)    
[OJK Indonesia, "BERINVESTASI MELALUI DEPOSITO"](https://sikapiuangmu.ojk.go.id/FrontEnd/CMS/Article/252)  
[Frederick F. Reichheld and W. Earl Sasser, Jr., "The Cost of Losing a Customer"](https://hbr.org/1990/09/zero-defections-quality-comes-to-services)  
