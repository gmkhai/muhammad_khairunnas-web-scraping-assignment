# 1. GraphQL

Case graphQL menggunakan public GraphQL API dari `https://github.com/trevorblades/countries/tree/main` API tersebut berisi kumpulan API untuk mendapatkan data dari sebuah country, mulai dari daftar country, states, phone number, dan lain sebagainya.

untuk mendapatkan API menggunakan graphQL digunakan library python requests. untuk hit API nya hampir sama dengan mengakses API pada umumnya. Tetapi method yang digunakan request adalah `POST` karena untuk graphQL memerlukan request body, yang berisi parameter query yang ingin diambil.

pada code `Assigment_web_scrapper_muhammad_khairunnas.ipynb` untuk:
- grapQL pertama digunakan graphQL untuk mendapatkan data dari berbagai country dengan filter regex dari negara yang berawal huruf `I`. 
- graphQL kedua digunakan graphQL untuk mendapatkan data dari country indonesia berdasarkan code negara `ID` data tersebut terdiri dari code telepon (phone), code negara (country code), nama negara (country name), aws region (aws region), code provinsi (state_code), dan nama provinsi (state name).

untuk export data ke `indonesia_region_dataset.csv.csv` data yang digunakan adalah data dari graphQL code negara `ID` export data yang dilakukan menggunakan pandas setelah daftar state country diubah ke dataframe.


# 2. BeautifulSoup

Case BeautifulSoup digunakan website dari `https://www.dekoruma.com/`. Website tersebut berisi beberapa product furniture bagi customer yang ingin mencari perlengkapan rumah tangga. pada code `Assigment_web_scrapper_muhammad_khairunnas.ipynb` pada header `BeautifulSoup` dilakukan penambahan variabel `count_scrap_item` untuk mengakses halaman pada website tersebut. untuk tahap yang dilakukan adalah:

- membuat perulangan loop untuk mengakses item product sesuai dengan batas `count_scrap_item`.
- menggunakan request untuk mengambil content dari page website diatas.
- menggunakan beautifulsoup untuk parsing html dari halaman website
- mengambil semua data product furniture di class `pure-u-1-4 phs mbxl`
- data yang diambil adalah gambar product, nama product, harga product, discount product, harga product setelah discount, rating product, dan service yang ditawarkan oelh websitenya.
- kemudian digunakan sleep dari library `time` ke 20 detik untuk mencegah downnya website diatas, agar tetap menghargai server dari yang discrap.
- setelah data diperoleh data diubah ke dataframe dan diexport ke csv dengan nama `furniture_dataset.csv`



Author: Muhammad Khairunnas
Email: heft0305@gmail.com