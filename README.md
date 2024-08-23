# Supermarket Analysis

## Supermarket Dataset 
Dataset dapat diakses [di sini](https://drive.google.com/drive/folders/1WodnBbuYTvsF0-6HTuQABQ0KCS31lqbK).

## Latar Belakang
Dalam konteks pertumbuhan positif yang dialami oleh supermarket, penting bagi manajemen untuk memahami lebih dalam perilaku dan karakteristik pelanggan mereka. Dengan pemahaman yang mendalam ini, supermarket dapat meningkatkan strategi pemasaran, mengoptimalkan penawaran produk, dan meningkatkan pengalaman pelanggan secara keseluruhan.

Oleh karena itu, sebagai Data Scientist, tugas Anda adalah untuk menganalisis data pelanggan supermarket dan mengidentifikasi segmentasi pelanggan berdasarkan perilaku dan karakteristik mereka saat berbelanja. Tujuan akhirnya adalah memberikan rekomendasi produk yang lebih personal dan relevan kepada pelanggan, meningkatkan kepuasan pelanggan, dan mendukung pertumbuhan revenue yang berkelanjutan.

Dengan pemahaman yang lebih mendalam tentang pelanggan, supermarket dapat lebih efektif dalam mempertahankan dan menarik pelanggan baru, serta memperkuat posisi mereka di pasar yang semakin kompetitif.

## Pernyataan Masalah
Sebagai perusahaan ritel yang beroperasi dalam industri supermarket, perusahaan memiliki tujuan untuk memahami karakteristik costumer yang loyal dan berharga tinggi. Dengan informasi ini, perusahaan dapat mengembangkan strategi pemasaran yang lebih efektif dan menyesuaikan layanan perusahaan untuk mempertahankan dan menarik pelanggan yang bernilai.

Dengan mempertimbangkan berbagai faktor yang mempengaruhi perilaku pembelian konsumen, perusahaan ingin seoarang data analyst untuk menjawab pertanyaan berikut:

- Apa saja ciri-ciri khas costumer yang loyal dan memiliki nilai tinggi bagi perusahaan perusahaan?
- Bagaimana perusahaan dapat mengidentifikasi segmentasi pelanggan yang membeli secara online dan offline, serta bagaimana kita dapat mengoptimalkan pengalaman mereka sesuai dengan preferensi dan kebutuhan masing-masing?

Dengan memperjelas tujuan perusahaan dalam memahami perilaku dan preferensi pelanggan, perusahaan berharap dapat mengumpulkan informasi yang lebih akurat dan relevan untuk membimbing keputusan strategis dan taktis perusahaan dalam meningkatkan loyalitas pelanggan dan pertumbuhan bisnis secara keseluruhan.

Dataset ini berisi informasi terkait (Sesudah Cleaning)

** People
* ID: Customer's unique identifier
* Age_Category: Customer's Age Category
* Education: Customer's education level
* Marital_Status: Customer's marital status
* Income: Customer's yearly household income
* Kidhome: Number of children in customer's household
* Teenhome: Number of teenagers in customer's household
* Dt_Customer: Date of customer's enrollment with the company

** Products
* MntWines: Amount spent on wine in last 2 years
* MntFruits: Amount spent on fruits in last 2 years
* MntMeatProducts: Amount spent on meat in last 2 years
* MntFishProducts: Amount spent on fish in last 2 years
* MntSweetProducts: Amount spent on sweets in last 2 years
* MntGoldProds: Amount spent on gold in last 2 years

** Places
* NumWebPurchases: Number of purchases made through the company’s website
* NumCatalogPurchases: Number of purchases made using a catalog
* NumStorePurchases: Number of purchases made directly in stores
* NumWebVisitsMonth: Number of visits to the company’s website in the last months
* OnlineP: Number of purchases customer made through online store
* OfflineP: Number of purchases customer made through offline store

** RFM
* Recency: Number of days since customer's last purchase
* Frequency: Number of how often a customer make a purchase 
* Monatery: Number of how many amount a customer spend


Melalui Visualisasi diatas, dapat ditarik kesimpulan bahwasannya:
- Produk `Wines` memiliki nilai penjualan yang tertinggi dengan mengambil average __59.3%__ dari total produk yang dibeli oleh customer
- Selanjutnya diikuti oleh produk `Meat` di posisi kedua dengan __22.9%__ average dari total produk yang dibeli oleh customer
- Lalu ada produk `Gold` pada posisi ketiga dengan average  __8.21%__
- Selanjutnya ada produk `Fish` dengan average __4.1%__
- yang terakhir ada produk `fruits` dan `sweet` yang memiliki average yang sama pada __2.74%__

Dengan mengetahui presentase product yang berhasil dijual, supermarket dapat menentukan rencana dan strategi yang baik berdasarkan avarege penjualan produk-produk diatas
- Supermarket dapat memfokuskan untuk lebih mempromosikan dan meningkatkan penjualan mereka terhadap produk `wines`, dan `meat`, karena kedua produk ini merupakan penyumbang revenue terbanyak untuk supermarket.
- Mengetahui segementasi pasar untuk setiap produk juga dapat membantu supermarket untuk membangun strategi marketing yang tepat sasaran dan efektif, hal ini akan dianalisis lebih lanjut melalui RFM analysis.
- Untuk produk-produk yang tidak begitu populer di supermarket seperti `fruits` dan `sweets`, supermarket dapat merencakan strategi2 baru untuk menarik customer2 dapat melirik produk2 tersebut, atau mungkin saja customer2 yang dapat dijangkau oleh supermarket bukanlah pasar yang tepat untuk produk2 tersebut.

## Suggestion and Recomendation based on the Recency Segmentation

Berdasarkan dari analisis mengenai segmentasi customer terhadap recency mereka, dapat diambil kesimpulan bahwa:
 - Terdapat `24.47%` Customer `active` yang melakukan transaksi mereka setidaknya selama 1 bulan kebelakang dari 06-2014 (data terbaru dari DT_Costumer)
 - Lalu ada `24.53%` customer yang melakukan transaksi sudah lebih dari 24 - 50 hari kebelakang dan mereka masuk kedalam category `warm`
 - Setelahnya ada presentase customer terbanyak yaitu sebesar `30.45%` masuk ke dalam category `cold`, dimana mereka sudah lama tidak melakukan transaksi, sekitar 50 - 74 hari yang lalu
 - Lalu segmentasi `inactive` memiliki presentase `20.55%` dimana customer ini sudah lebh dari 75 hari yang lalu melakukan transaksinya

Supermarket berada dalam posisi yang bimbang, karena terdaapt sekitar 50% customer yang melakukan transaksi dalam 2bulan terakhir (tidak menutup kemungkinan adanya customer baru), dan juga ada 50% customer lainnya yang sudah tidak melakukan transaksi lagi lebih dari 2bulan. Supermarket perlu melakukan peninjauan ulang agar strateginya dapat menarik lebih banyak cutomer baru dan tidak melupakan customer lama untuk dipertahankan juga, sehingga rata-rata penjualan akan meningkat dan stabil.    

Berikut merupakan beberapa suggestion dan recomendation untuk recency segmentation:
 - Active Segment : Bisa lebih fokus untuk meningkatkan daya beli customer, bisa dengan menawarkan beberapa produk yang relate dengan mereka (Upselling / Crossselling)
 - Warm Segment : Fokus kepada retention strategy
 - Cold Segment : fokus untuk menarik kembali minat belanja customer ini dengan reactivate atau retention strategy
 - Inactive Segment : Fokus untuk memberi reactivate strategy untuk menarik perhatian customer ini


## Suggestion and Recomendation based on the Frequency Segmentation with Monatery

Berdasarkan dari analisis mengenai segmentasi customer terhadap Frequency mereka dengan jumlah uang yang dikeluakan, dapat diambil kesimpulan bahwa:
 - Customer dengan segmentasi `Special Value` menyumbang sekitar `48.29%` sebagai revenue untuk supermarket
 - Lalu diikuti oleh segmentasi `High Valie` yang berkontribusi sekitar `39.78%` untuk supermarket
 - Setelahnya ada `Normal Customer` yang memilki andil dalam revenue supermarket sebanyak `10.25%`
 - Lalu segmentasi `Low Value` dengan kontribusi paling sedikit di sekitar `1.59%`

Revenue dari supermarket masih dalam keadaan yang aman dan baik, tetapi hal ini tidak berarti supermarket bisa lepas tangan, karena penyumbang terbesar untuk revenue supermarket `48.29%` hanya berasal dari 25 customer dan 10 diantaranya sedang dalam posisi `cold` berdasarkan transaksi terakhir mereka, sehingga supermarket harus mencari cara untuk meningkatkan revenue dan juga mempertahankan kesetiaan customer atau mungkin saja menarik kemabali customer yang sudah lama tidak melakukan transaksi   

Berikut merupakan beberapa suggestion dan recomendation untuk Frequency segmentation:
 - Customer special value dan high value sudah berkontribusi untuk 87% dari revenue supermarket, ini berarti supermarket dapat memfokuskan budget, effort, penwaran dan strategi mereka terhadapt dua segement ini, untuk memjaga kesetiaan customer dan meningkatkan value mereka.
 - Terdapat sekitar 20% customer yang masuk ke dalam category `Low Value`, meskipun kontribusi mereka ke revenue supermarket sangat sedikit tetapi alangkah baiknya mereka tidak dilupakan, karena mungkin saja ada dari mereka yang meruapakan customer baru sehingga kontribusi mereka masih lah sedikit, fokuskan penwaran dan pendekatan kepada mereka yang `Low Value` tapi `Actiive` karena mereka dapat disebut sebagai customer yang potential bagi supermarket kedepannya.
 - Membuat program yang bisa meningkatkan value dan kesetiaan para customer terhadap supermarket. Misalnya dengan subscription, membership. Lalu dari membership dan subscription para customer dapt diberi penawaran-penawaran menarik, seperti cahsback, diskon, promo, paket dan lain sebagainya.


## Online Vs Offline 
Supermarket memiliki 2 cara untuk melakukan transaksasi, yaitu proses transaksi langsung terjadi di tempat / toko offline hal ini disebut dengan `OfflineP`, sedangkan untuk proses transaksi yang terjual melewati web toko, hal ini disebut dengan `OnlineP`. 

Jika membandingkan pemanfaatan tempat melakukan transaksi, maka saran yang dapat diberikan ialah:
- pada segementasi `Special Value` pembelian di toko offline maupun online memiliki nilai yang tinggi, menandakan bahwa customer di segemntasi ini memiliki preferensi untuk melakukan transaksi secara online maupun offline. 
- Pada segmentasi `High Value` pembelian di toko offline lebih tinggi dibandingkan dengan online, maka supermarket diharapkan untuk memberikan penawaran khusus (diskon ekslusif di toko offline) untuk kemudian dapat mempertahankan kesetiaan dan menaikkan rata-rata penjualan dari segemntasi ini.
- Lalu untuk segemntasi customer `Normal dan Low Value` supermarket dapat fokus untuk memberikan penwaran yang menarik secara online maupun offline untuk kemudian menarik minat customer untuk setidaknya kembali berbelanja di supermarket ini dan jga meningkatkan frequency pembeliannya. Daripada berfokus kepada meningkatkan spend mereka, lebih baik untuk membuat mereka menjadi customer yang memiliki frequency yang bagus dan loyal. 
