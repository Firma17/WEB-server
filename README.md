# WEB-server
Web server adalah sebuah software (perangkat lunak) yang memberikan layanan berupa data. Berfungsi untuk menerima permintaan HTTP atau HTTPS dari klien atau kita kenal dengan web browser (Chrome, Firefox, dan sebagainya). Selanjutnya ia akan mengirimkan respon atas permintaan tersebut kepada client dalam bentuk halaman web.

# Tujuan web
Untuk profile pribadi.
# resource
1. ubuntu server
2. ssh
3. apache
4. php


# porgess
1.	Install Ubuntu Server di Hardisk Eksternal.
2.	Install Apache2.
   
   $sudo apt install apache2
   $sudo systemctl start apache2
   $sudo systemctl status apache2

4. Install php
   
   $sudo apt install php libapache2-mod-php php-mysql
   $sudo systemctl restart apache2
   $echo "<?php phpinfo(); ?>" | sudo tee /var/www/html/info.php

6. Install ssh
   
   $sudo apt install openssh-server
   $sudo systemctl status ssh
   $sudo nano /etc/ssh/sshd_config
   $sudo systemctl restart ssh

8. Hasil Codingan
   
   $index.html
   <!DOCTYPE html>
<!-- Coding by CodingLab | www.codinglabweb.com-->
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Profile Card UI Design</title>

    <!-- CSS -->
    <link rel="stylesheet" href="style.css" />

    <!-- Boxicons CSS -->
    <link
      href="https://unpkg.com/boxicons@2.1.2/css/boxicons.min.css"
      rel="stylesheet"
    />
  </head>
  <body>
    <div class="profile-card">
      <div class="image">
        <img src="https://drive.google.com/uc?id=1VfrVOaVuiSTdXEKtVkHE5lB5t15SsZUd" alt="" class="profile-img">
      </div>

      <div class="text-data">
        <span class="name">Firma Danu Kusuma</span>
        <span class="job">Volley Ball Player</span>
      </div>

      <div class="media-buttons">
        <a href="https://web.facebook.com/firma.kusuma.566" style="background: #4267b2" class="link">
          <i class="bx bxl-facebook"></i>
        </a>
        <a href="profil.html" style="background: #1da1f2" class="link">
          <i class="bx bxl-twitter"></i>
        </a>
        <a href="https://instagram.com/danu_baron" style="background: #e1306c" class="link">
          <i class="bx bxl-instagram"></i>
        </a>
        <a href="https://youtube.com/@danukusuma90" style="background: #ff0000" class="link">
          <i class="bx bxl-youtube"></i>
        </a>
      </div>

      <div class="buttons">
        <a href="profil.html">Profil</a>
        <a href="#">Message</a>
      </div>

      <div class="analytics">
        <div class="data">
          <i class="bx bx-heart"></i>
          <span class="number">60k</span>
        </div>
        <div class="data">
          <i class="bx bx-message-rounded"></i>
          <span class="number">20k</span>
        </div>
        <div class="data">
          <i class="bx bx-share"></i>
          <span class="number">12k</span>
        </div>
      </div>
    </div>
  </body>
</html>

   $profil.html
   <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Profil Diri</title>
  <link rel="stylesheet" href="stylee.css">
</head>
<body>

  <header>
    <h1>Profil Diri</h1>
  </header>

  <section class="text">
    <p><strong>Nama:</strong> Firma Danu Kusuma</p>
    <p><strong>Alamat:</strong> Sumber Mulyo, Buay Madang Timur, Oku Timur. Palembang</p>
    <p><strong>Email:</strong> kusumadanu817@gmial.com</p>
    <p><strong>Telepon:</strong> 0857777777777</p>
  </section>

  <section>
    <h2>Tentang Saya</h2>
    <p>
      Saya adalah seorang anak laki-laki yang lagi menempuh hidup di kota orang.
      Biasanya saya di panggil danu, saya anak ke dua sekaligus anak terakhir.
      Hobi saya bermain Bola Voly dan zodiak saya Taurus.
      Saya lahir di palembang namun keluarga saya asli suku jawa timur lebih tepat nya di Tulunganggung.
      Sekarang ini saya sedang menempuh pendidikan di Universitas Amikom Yogyakarta.
      Saya juga memiliki perinsip jika saya belum lulus kuliah saya tidak mau pacaran dulu dan kalo bisa Taaruf.
      Saya samasekali belum pernah berpacaran karena prinsip tersebut.
    </p>
  </section>

  <footer class="text-footer">
    <p>Terima kasih telah mengunjungi halaman profil saya!</p>
  </footer>

</body>
</html>

   $style.css
   /* Google Fonts - Poppins */
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600&display=swap");

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
}
body {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(to top, #0e4bf1, #e7e7e7);
}
.profile-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 370px;
  width: 100%;
  background: #fff;
  border-radius: 24px;
  padding: 25px;
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
  position: relative;
}
.profile-card::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 36%;
  width: 100%;
  border-radius: 24px 24px 0 0;
  background-color: #4070f4;
}
.image {
  position: relative;
  height: 150px;
  width: 150px;
  border-radius: 50%;
  background-color: #4070f4;
  padding: 3px;
  margin-bottom: 10px;
}
.image .profile-img {
  position: absolute;
  height: 100%;
  width: 100%;
  object-fit: cover;
  border-radius: 50%;
  border: 3px solid #fff;
}
.profile-card .text-data {
  display: flex;
  flex-direction: column;
  align-items: center;
  color: #333;
}
.text-data .name {
  font-size: 22px;
  font-weight: 500;
}
.text-data .job {
  font-size: 15px;
  font-weight: 400;
}
.profile-card .media-buttons {
  display: flex;
  align-items: center;
  margin-top: 15px;
}
.media-buttons .link {
  display: flex;
  align-items: center;
  justify-content: center;
  color: #fff;
  font-size: 18px;
  height: 34px;
  width: 34px;
  border-radius: 50%;
  margin: 0 8px;
  background-color: #4070f4;
  text-decoration: none;
}
.profile-card .buttons {
  display: flex;
  align-items: center;
  margin-top: 25px;
}
.buttons a{
  color: #fff;
  font-size: 14px;
  font-weight: 400;
  border: none;
  border-radius: 24px;
  margin: 0 10px;
  padding: 8px 24px;
  background-color: #4070f4;
  cursor: pointer;
  transition: all 0.3s ease;
  text-decoration: none;
}
.buttons .button:hover {
  background-color: #0e4bf1;
}
.profile-card .analytics {
  display: flex;
  align-items: center;
  margin-top: 25px;
}
.analytics .data {
  display: flex;
  align-items: center;
  color: #333;
  padding: 0 20px;
  border-right: 2px solid #e7e7e7;
}
.data i {
  font-size: 18px;
  margin-right: 6px;
}
.data:last-child {
  border-right: none;
}

   $stylee.css
   body {
    font-family: Arial, sans-serif;
    margin: 20px;
    padding: 20px;
    background: linear-gradient(to left, #6890ff, #e7e7e7);
}
h1 {
    color: #333;
    text-align: center;
}  
h2 {
    color: #333;
    text-align: center;
}
p {
    color: #555;
    text-align: justify;
}
.text p {
    color: #555;
    margin-left: 500px;
}
.profile-img {
    max-width: 200px;
    border-radius: 50%;
}
.text-footer p{
    text-align: center;
}
# Tampilan Web
![Cuplikan layar 2023-12-20 024759](https://github.com/Firma17/WEB-server/assets/148019668/74a4f2d4-dde2-4580-b6d4-2d7d88f8fd20)

![Cuplikan layar 2023-12-20 024843](https://github.com/Firma17/WEB-server/assets/148019668/c2d2821d-91a7-46d6-a117-ae5e28efeefd)


   


