Kelompok A15 :

Farrel Muhammad Taqi     05111840000071

Muhammad Iqbal Humam     05111840000103

**DNS**

1. Untuk membuat domain semerua15.pw maka perlu langkah yang perlu dilakukan adalah

    a. Install bind9
    
    b. Ubah file named.conf.local seperti dibawah
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/1.1.PNG)
    
    c. Buat folder jarkom dalam bind (/etc/bind/jarkom)
    
    d. Salin file db.local kedalam file jarkom
    
    e. Ganti localhost dengan nama domain
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/1.2.PNG)
    
    f. Buat GRESIK dan SIDOARJO menjadi client dengan mengubah resolv.conf
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/1.3.PNG)
    
    g. Jika berhasil akan seperti dibawah
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/1.99.PNG)

2. Agar domain mempunyai alias www.semerua15.pw langkah yang perlu dilakukan adalah

    a. Tambahkan www dan CNAME pada semerua15.pw seperti dibawah
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/2.1.PNG)
    
    b. restart bindnya
    
    c. Jika berhasil akan seperti dibawah
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/2.99.PNG)
    
3. Untuk membuat subdomain penanjakan.semerua15.pw dapat dilakukan
    
    a. Tambahkan penanjakan pada file semerua15.pw seperti dibawah
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/3.1.PNG)
    
    b. restart bindnya 
    
    c. Jika berhasil akan seperti dibawah
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/3.99.PNG)

4. Langkah untuk membuat reverse dns adalah

    a. Ubah file named.conf.local
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/4.1.PNG)
    
    b. Salin file db.local ke folder jarkom dengan nama 3 byte pertama IP MALANG yang terbalik
    
    c. Tambahkan PTR pada file tersebut
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/4.2.PNG)
    
    d. Restart bindnya
    
    e. Jika berhasil akan seperti dibawah
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/4.99.PNG)
    
    
5. Untuk membuat DNS Slave pada Mojokerto maka yang perlu dilakukan adalah

    a. Ubah file named.conf.local pada server MALANG seperti dibawah
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/5.1.PNG)

    b. Restart bindnya
    
    c. Update package pada file MOJOKERTO
    
    d. install bind pada file MOJOKERTO
    
    e. ubah file named.conf.local seperti dibawah
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/5.2.PNG)

    f. Restart bindnya
    
    g, Jika berhasil maka walaupun bind pada server MALANG sudah di stop maka tetap dapat melakukan ping
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/5.98.PNG)
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/5.99.PNG)


6. Untuk membuat subdomain dengan alamat gunung.semeruyyy.pw yang didelegasikan pada server MOJOKERTO dan mengarah ke IP
Server PROBOLINGGO dapat dilakukan dengan langkah
    
    a. Ubah file semerua15.pw seperti gambar dibawah
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/6.1.PNG)
    
    b. Pada file named.conf.options komenkan dnssec dan tambahkan allow query seperti gambar dibawah
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/6.2.PNG)

    c. Ubah file named.conf.local seperti gambar dibawah
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/6.3.PNG)
    
    d. Restart bindnya
    
    e. Pada server MOJOKERTO ubah file named.conf.options seperti server MALANG
    
    f. Ubah file named.conf.local seperti gambar dibawah
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/6.4.PNG)

    g. Buat folder delegasi
    
    h. Buat salinan db.local ke dalam folder delegasi dengan nama gunung.semerua15.pw
    
    i. Ubah file gunung.semerua15.pw seperti dibawah ini
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/6.5.PNG)
    
    j. Restart bindnya
    
    k. Jika berhasil maka akan seperti dibawah
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/6.99.PNG)
    
7. Untuk membuat subdomain naik.gunung.semerua15.pw yang diarahkan ke ip server PROBOLINGGO dapat dilakukan
   
    a. Tambahkan naik pada file gunung.semerua15.pw
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/7.1.PNG)
    
    b. Restart bindnya
    
    c. Jika berhasil akan seperti gambar dibawah
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/7.99.PNG)

   


**Web Server**

8. Setelah selesai membuat keseluruhan domain, kamu diminta untuk segera mengatur web server. (8) Domain http://semeruyyy.pw memiliki DocumentRoot pada /var/www/semeruyyy.pw.

    a. Instal Apache di Probolinggo
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/8.1.png)
    
    b. Instal PHP5
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/8.2.png)
    
    c. Ketik nano semerua15.pw di apache2/sites-available dan mengubah dokumen root dan directory sebagai berikut
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/8.3.png)
    
    d. download file zip yang disediakan di soal, unzip, dan kemudian rename menjadi semerua15
    
    e. sudah selesai
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/8.4.png)
    
    
9. Awalnya webdapat diakses menggunakan alamat http://semeruyyy.pw/index.php/home. Karena dirasa alamat urlnyakurang bagus, maka (9) diaktifkan mod rewrite agar urlnya menjadi http://semeruyyy.pw/home.

    a. ketikkan a2enmod rewrite untuk mengaktifkan modul rewrite
    
    b. buat file .htaccess dan masukkan script berikut
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/9.1.png)
    
    c. masuk ke semerua15.pw di apache dan masukkan script berikut
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/9.2.png)
    
    d. sudah selesai
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/9.3.png)
    
10. Web http://penanjakan.semeruyyy.pw akan digunakan untuk menyimpan assets file yang memiliki DocumentRoot pada /var/www/penanjakan.semeruyyy.pw dan memiliki struktur
folder sebagai berikut:

    a. masuk ke /var/www/ dengan cd
    
    b. download file zip yang disediakan di soal dengan wget
    
    c. unzip file dan kemudian rename sesuai dengan nama kelompok, yaitu penanjakan.semerua15.pw
    
    d. sudah selesai
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/10.1.png)

11. Pada folder /public dibolehkan directory listing namun untuk folder yang berada di dalamnya tidak dibolehkan.

    a. pada penanjakan.semerua15.pw di apache ditambahkan script sebagai berikut
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/11.1.png)
    
    b. hasil 
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/11.2.png)
    
    c. mencoba membuka salah satu file yang private
        
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/11.3.png)

12. Untuk mengatasi HTTP Error code 404, disediakan file 404.html pada folder /errors untuk mengganti error default 404 dari Apache.
    
    a. menambahkan script ErrorDocument 404 /errors/404.html pada penanjakan.semerua15.pw
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/12.1.png)


13. Untuk mengakses file assets javascript awalnya harus menggunakan url http://penanjakan.semeruyyy.pw/public/javascripts. Karena terlalu panjang maka dibuatkan konfigurasi virtual host agar ketika mengakses file assets menjadi http://penanjakan.semeruyyy.pw/js.

    a. menambahkan script alias seperti di penanjakan.semerua15.pw
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/13.1.png)
    
    b. sebelum ditambah script
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/13.2.png)
    
    c. setelah ditambah script
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/13.3.png)
    
14. Untuk web http://gunung.semeruyyy.pw belum dapat dikonfigurasi pada web server karena menunggu pengerjaan website selesai. (14) sedangkan web http://naik.gunung.semeruyyy.pw
sudah bisa diakses hanya dengan menggunakan port 8888. DocumentRoot web berada pada /var/www/naik.gunung.semeruyyy.pw.

    a. Membuat file site untuk naik.gunung.semerua15.pw dengan cp dari default atau default-8080 dan diedit sesuai berikut
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/14.1.png)
    
    b. download file zip yang ada di soal dengan wget, unzip, dan rename menjadi naik.gunung.semeru15.pw di /var/www
    
    c. tambahkan Listen 8888 di ports.conf di apache
    
    d. sudah selesai
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/14.2.png)

15. Dikarenakan web http://naik.gunung.semeruyyy.pw bersifat private (15) Bibah meminta kamu membuat web http://naik.gunung.semeruyyy.pw agar diberi autentikasi password dengan username “semeru” dan password “kuynaikgunung” supaya aman dan tidak sembarang orang bisa mengaksesnya.
    
    a. jalankan htpasswd -c /etc/apache2/.htpasswd semeru di Probolinggo dan masukkan password yang dikehendaki sesuai soal
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/15.1.png)
    
    b. Ubah naik.gunung.semerua15.pw di apache sites-available sesuai dengan script berikut
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/15.2.png)
    
    c. Pada bagian bawah file tersebut, tambahkan script sebagai berikut :
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/15.3.png)
    
    d. sudah selesai
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/15.4.png)

16. Saat Bibah mengunjungi IP PROBOLINGGO, yang muncul bukan web utama http://semeruyyy.pw melainkan laman default Apache yang bertuliskan “It works!”. (16) Karena dirasa kurang profesional, maka setiap Bibah mengunjungi IP PROBOLINGGO akan dialihkan secara otomatis ke http://semeruyyy.pw.

    a. tambahkan script redirect permanent pada site default di apache sesuai script berikut
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/16.1.png)
    
    b. sudah selesai
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/16.2.png)

17. Karena pengunjung pada /var/www/penanjakan.semeruyyy.pw/public/images sangat banyak maka semua request gambar yang memiliki substring “semeru” akan diarahkan menuju semeru.jpg.

    a. buat file .htaccess di probolinggo dan masukkan script sebagai berikut
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/17.1.png)
    
    b. sudah selesai
    
    ![fotooooo](https://github.com/farrelmt/Jarkom_Modul2_Lapres_A15/blob/main/screenshot/17.2.png)
