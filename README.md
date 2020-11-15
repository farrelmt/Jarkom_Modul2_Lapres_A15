Kelompok A15 :

Farrel Muhammad Taqi     05111840000071

Muhammad Iqbal Humam     05111840000103

**DNS**

1. 


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
