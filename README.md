**Latar Belakang**
<br>
Sebagai seorang data analis yang beroperasi di perusahaan bisnis properti, kami menyadari bahwa Airbnb semakin berkembang pesat sebagai platform penyewaan properti yang populer khususnya di kota Bangkok. Di tengah pesatnya perkembangan ini, pemahaman yang mendalam tentang karakteristik properti yang paling dicari oleh penyewa sangat penting. Memahami tren ini akan membantu perusahaan kami untuk mengambil keputusan yang lebih tepat dalam merancang strategi bisnis sewa properti di Bangkok, serta mengoptimalkan pendapatan.

**Pernyataan Masalah**
<br>
Dalam kapasitas kami sebagai data analis, pertanyaan utama yang kami hadapi adalah
 1. Apa karakteristik utama dari properti di Bangkok pada platform Airbnb yang paling diminati oleh penyewa? 
 2. Bagaimana merancang strategi yang tepat dalam membantu perusahaan untuk mengoptimalkan pendapatan?

Dengan pemahaman yang lebih baik tentang preferensi penyewa, perusahaan dapat mengambil langkah-langkah yang lebih tepat dalam mengelola portofolio properti dan meningkatkan daya saing di pasar.

**Data**
<br>
Kita akan melakukan analisis menggunakan dataset "Airbnb Listings Bangkok". Melalui analisis ini, kami akan dijawab pertanyaan-pertanyaan di atas

berikut Dataset "Airbnb Listings Bangkok":
1. **id**: Nomor identifikasi unik properti dalam sistem Airbnb.
2. **name**: Nama properti yang ditampilkan dalam daftar Airbnb.
3. **host_id**: Nomor identifikasi unik tuan rumah (pemilik properti) di Airbnb.
4. **host_name**: Nama tuan rumah (hanya nama depan biasanya).
5. **neighborhood**: Daerah atau lingkungan geografis di mana properti terletak.
6. **latitude**: Koordinat lintang properti menggunakan sistem proyeksi World Geodetic System (WGS84).
7. **longitude**: Koordinat bujur properti menggunakan sistem proyeksi World Geodetic System (WGS84).
8. **room_type**: Jenis kamar yang ditawarkan, seperti "Entire home/apt" (seluruh rumah/apartemen), "Private room" (kamar pribadi), "Shared room" (kamar bersama), atau "Hotel".
9. **price**: Harga sewa harian properti dalam mata uang lokal (bath).
10. **minimum_nights**: Jumlah minimum malam yang harus dipesan untuk properti tersebut.
11. **number_of_reviews**: Total jumlah ulasan yang diterima properti.
12. **last_review**: Tanggal ulasan terakhir dari tamu.
13. **reviews_per_month** :  Jumlah ulasan per bulan
14. **calculated_host_listings_count**: Jumlah total properti yang dimiliki oleh tuan rumah di Bangkok.
15. **availability_365**: Jumlah hari dalam setahun di mana properti tersedia untuk disewakan.
16. **number_of_reviews_ltm**: Jumlah ulasan yang diterima properti dalam 12 bulan terakhir.

**Analisa Data**
<br>
Dalam melihat karakteristik properti yang paling banyak diminati oleh penyewa, kami menggunakan kolom **'availability_365'** untuk menentukan properti mana yang paling laku. Sehingga semakin kecil availabilitynya, properti tersebut semakin laku. Kami mengidentifikasinya properti yang paling laku adalah properti yang tersewa 90%nya dalam 1 tahun. Minimal properti tersebut tidak ada yang menyewa sama sekali selama 3 hari per bulannya atau 36 hari per tahunnya. Sehingga kami akan menyaring(filter) data berdasarkan jumlah availabilitynya yang kurang dari sama dengan 36 hari.
<br>
Kami menetapkan target tingkat okupansi sebesar 90 persen karena hal ini penting dalam rangka mencari properti yang **sangat diminati**. Dari sini, kami akan melakukan analisis mendalam untuk mengidentifikasi karakteristik utama dari properti yang memiliki performa laku tersebut. Fokus kami adalah untuk memahami aspek-aspek yang akan mengoptimalkan pendapatan perusahaan.

**Kesimpulan**
<br>
Dari analisis yang telah dilakukan, kita dapat membuat kesimpulan terkait bagaimana karakteristik properti yang laku di airbnb Bangkok sebagai berikut :
1. Dari seluruh data list airbnb, hanya **7%** properti yang masuk ke dalam kategori laku (minimal tersewa 90% dalam 1 tahun)
2. Harga berdasarkan Tipe kamar yang paling tepat secara keseluruhan:
    - Hotel room: dengan kisaran harga 1700 bath. 
    - Entire home/apt: dengan kisaran 1536 bath.
    - Shared room : dengan kisaran harga 500 bath. 
    - Private room: dengan kisaran 1212 bath.
3. Properti yang paling laku, persebarannya berada di harga properti yang murah pada setiap tipenya.
4. Daerah dengan jumlah properti yang paling banyak banyak laku adalah Huai Khwang, posisi kedua : Vadhana, posisi ketiga : Khlong Toei
5. Properti yang laku tersebut, tersebar di daerah pusat/ tengah kota. Kemudian semakin ke pinggir kanan(timur) dan kiri(barat), semakin sedikit jumlah properti yang laku. Pada daerah pinggir juga ada daerah yang sama sekali tidak memenuhi kriteria laku/ tidak ada properti yang laku pada daerah tersebut.
6. Pada 10 daerah yang paling laku, terlihat bahwa shared room memiliki kisaran harga yang ter-rendah. Hotel room memiliki memiliki kisaran harga yang paling tinggi.
7. Tipe kamar yang paling banyak laku adalah Entire home/apt, dan posisi kedua adalah Private room, dan posisi ketiga adalah Hotel Room, dan posisi terakhir adalah Shared room
8. Setiap daerah memiliki karakteristik tipe kamar dan harga yang berbeda-beda. Sehingga perlakuan dalam pengambilan keputusan harus didasarkan oleh karakteristik daerah itu sendiri.
9. Terdapat 5 daerah dengan harga terbaik dan banyak properti yang laku ( masuk ke dalam 10 daerah terlaku) yaitu : Huai Khwang, Vadhana, Ratchathewi, Parthum Wan, dan Bang Na.
10. Kamar yang laku dan harga yang baik, memiliki jumlah ninimum night yang tidak terlalu lama. Persebarannya ada di 2 hari.
11. Banyaknya jumlah review / tidak, tidak mempengaruhi properti tersebut menjadi laku.

**Rekomendasi**
Setelah kita temukan karakteristik properti yang laku di airbnb bangkok, sekarang kami akan memberikan rekomendasi ke perusahaan berdasarkan data ini :
1. **Penetapan Harga yang Kompetitif** : Atur harga agar bisa bersaing dengan properti sejenis di daerah yang sama. Ini bisa mempengaruhi minat penyewa untuk memilih properti. Sesuaikan harga dengan tipe kamar dan karakteristik daerah, untuk itu kami sudah mensortir harga yang terbaik dari beberapa daerah yang paling laku. Lima kota yang kami sarankan untuk bisnis yang baik berada di kota :
	1. Huai Khwang
		- Dengan tipe kamar :
		- Entire home/apt dengan harga 1.057 bath
		- Private Room dengan harga 1.200 bath
		- Hotel Room dengan harga 5.011 bath
	2. Vadhana
		- Dengan tipe kamar :
		- Entire home/apt dengan harga 2.000 bath
		- Private room dengan harga 1.500 bath
		- Hotel room dengan harga 5.350 bath
	3. Ratchatdewi
		- Dengan tiper kamar :
		- Entire home/apt dengan harga 2.100 bath
		- Private room dengan harga 1.120 bath
		- Hotel room dengan harga 4.829 bath
	4. Parthum Wan
		- Dengan tipe kamar :
		- Entire home/apt dengan harga 2.279 bath
		- Private room dengan harga 6.142 bath
		- Hotel room dengan harga 6.612 bath
	5. Bang Na
		- Dengan tipe kamar :
		- Entire home/apt dengan harga 1.090 bath
		- Private room dengan harga 10.000 bath
2. **Diversifikasi Portofolio** : Jika memungkinkan, pertimbangkan untuk memiliki properti di beberapa daerah yang berbeda. Ini dapat membantu mengurangi risiko jika suatu daerah mengalami fluktuasi. Pertimbangan diversifikasi dengan poin berikut :
	1. Jika perusahaan ingin properti laku lebih banyak dengan perputaran uang yang cepat, namun jumlah pemasukan di setiap peroperti yang disewa stabil. Bisnis dapat dilakukan di Huai Kwang dan Vadhana dengan tipe kamar Entire home/ apt.
	2. Jika perusahaan ingin mendapatkan pemasukan yang lumayan besar, dengan risiko properti yang laku hampir stabil. Bisnis dapat dilakukan di Huai Khwang, Vadhana, Ratchatewi dan Partum Wan dengan tipe kamar Hotel Room. 
	3. Jika perusahaan ingin mendapatkan pemasukan yang besar, dengan risiko properti yang laku lebih sedikit dibanding yang lain. Bisnis dapat dilakukan di Bang Na dan Parthum Wan dengan tipe kamar Private Room. Agar memiliki peluang yang tinggi, membangun bisnis ini dilakukan dilokasi yang berdekatan dengan lokasi properti yang sudah ada. Dikarenakan pada daerah ini properti cenderung tersebar di lokasi tertentu.
3. **Hindari Tipe Kamar Shared** : Tipe kamar Shared cenderung kurang diminati, bahkan jika harganya murah. Sebaiknya fokus pada tipe kamar lain.
4. **Minimum Malam**: Pertimbangkan untuk menetapkan jumlah minimum malam yang cukup fleksibel, seperti 2 malam. Hal ini dapat meningkatkan daya tarik properti Anda, terutama bagi mereka yang mencari akomodasi singkat.

**Tableau**
<br>
Anda dapat melihat visualisasi yang lebih lengkap lagi pada link <https://public.tableau.com/views/Capstone2-Anastasia/Story1?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link >
