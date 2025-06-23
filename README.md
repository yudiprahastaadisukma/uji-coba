<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kedai Kopi</title>
    <!--font-->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap" rel="stylesheet">
    <!--Feather Icons-->
    <script src="https://unpkg.com/feather-icons"></script>

    <!--my Style-->
    <style>
        :root{
    --promary:#b6895b ;
    --background : #010101 ;
    --wt : #fff;
}

* {
    margin:0;
    padding:0;
    box-sizing: border-box;
    outline: none;
    border: none;
    text-decoration: none;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: 'Poppins' sans-serif;
    background-color: var(--background);
    color: #fff ;
}

/*navbar*/
.navbar {
    display: flex;
    justify-content: space-between ;
    align-items: center;
    padding: 1.4rem 7%;
    background-color: rgba(1, 1, 1)0%, 8%;
    border-bottom: 1px solid #513c28 ;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 9999;
}

.navbar .navbar-logo {
    font-size: 2rem;
    font-weight: 700 ;
    color: #fff;
    font-style: italic;
}

.navbar .navbar-logo span {
    color: var(--promary);
}

.navbar .navbar-nav a {
    color: #fff;
    display: inline-block;
    font-size: 2rem;
    margin: 0 1rem;
}

.navbar .navbar-nav a:hover {
    color: var(--promary);
}

.navbar.navbar-nav ::after {
    content: '';
    display: block;
    padding-bottom: 0.5rem;
    border-bottom: 0.1rem solid var(--promary) ;
    transform: scaleX(0);
    transition: 0.25 linear;
}

.navbar .navbar-nav a:hover::after {
    transform: scaleX(0.5rem);
}

.navbar .navbar-extra a {
    color: #fff;
    margin: 0 0.5rem;
}

.navbar .navbar-extra a:hover {
    color: var(--promary)
}

#hamburger-menu {
    display: none;
}

/*hero section*/

.hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    background-image:('../gambar/kopi.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    position: relative;
}

.hero::after {
    content: "";
    display: block;
    position: absolute;
    width: 100%;
    height: 20%;
    bottom: 0;
    background: linear-gradient(0deg, rgba(1,1,3,1)8%,rgba(255,255,255,0)50%);
    mix-blend-mode: difference;
}

.hero .content {
    padding: 1.4rem 7%;
    max-width: 60rem;
}
.hero .content h1 {
    font-size: 2cm;
    color: #fff;
    text-shadow: 1px 1px 3px rgba(1,1,3,0.5);
    line-height: 1.2;
}

.hero .content h1, p span{
    color: var(--promary);
}

.hero .content p {
    font-size: 1.6rem;
    margin-top: 1rem;
    line-height: 1.2;
    font-weight: 100;
    text-shadow: 1px 1px 3px rgba(1,1,3,0.5);
}

.hero .content a.cta {
    margin-top: 1rem;
    display: inline-block;
    padding: 1rem 3rem;
    font-size: 0.5cm;
    color: #fff;
    background-color: var(--promary);
    border-radius: 0.5rem;
    box-shadow: 1px 1px 3px rgba(1,1,3,0.5);
}

/*about section*/
.about, 
.menu, 
.contact {
    padding: 8rem 7% 1.4rem;
}

.about h2, 
.menu h2, 
.contact h2 {
    text-align: center;
    font-size: 2.5rem;
    margin-bottom: 2.5rem;
}

.about h2 span, 
.menu h2,
.contact h2 span {
    color: var(--promary);
}

.about .row {
    display: flex;
}

.about .row .about-img {
    flex: 1 1 45rem ;
}

.about .row .about-img img {
    width: 100%;
}

.about .row .content {
    flex: 1 1 35rem;
    padding: 0 1rem;
}

.about .row .content h3 {
    font-size: 1.8rem;
    margin-bottom: 1rem;
}
.about .row ,.contact h7 

.about .row .content p {
    margin-bottom: 0.8rem;
    font-size: 1.4rem;
    font-weight: 100;
    line-height: 1.6;
}

/* menu section*/
.menu h2,
.contact h2 {
    margin-bottom: 1rem;
}
.menu p,
.contact p {
    text-align: center;
    max-width: 30rem;
    margin: auto;
    font-weight: 100;
    line-height: 1.6;
}

.menu .row {
    display: flex;
    flex-wrap: wrap;
    margin-top: 5rem;
    justify-content: center;
}

.menu .row .menu-card {
    text-align: center;
    padding-bottom: 4rem;
    padding: 2rem;
}

/* untuk gambar produk */
.menu .row .menu-card img {
    border-radius: 50%;
    width: 100%;
}

.menu .row .menu-card .menu-card-title {
    margin-top: 1.5rem auto 0.5rem;
}

/* contact section*/

.contact .row {
    display: flex;
    margin-top: 2rem;
    background-color: var(--promary);
    flex-wrap: wrap;
}

.contact .row .map {
    flex: 1 1 45rem;
    width: 100%;
    object-fit: cover;
}

.contact .row form {
    flex: 1 1 45rem;
    padding: 5rem 2rem;
    text-align: center;
}

.contact .row form .input-group {
    display: flex;
    align-items: center;
    margin-top: 2rem;
    background-color: #010101;
    border: 1px solid #eee;
    padding-left: 2rem;
}

.contact .row form .input-group input {
    width: 100%;
    padding: 2rem;
    font-size: 1.7rem;
    background: none;
    color: #fff;
}

.contact .row form .btn {
    margin-top: 3rem;
    display: inline-block;
    padding: 1rem 3rem;
    font-size: 1.7rem;
    color: #fff;
    background-color: var(--background);
    cursor: pointer;
}

/*footer*/
footer {
   background-color: var(--promary);
   text-align: center;
   padding: 1rem 0;
   margin-top: 3rem; 
}

footer .sosial {
    padding: 0;
}

footer .sosial a {
    color: #fff;
    margin: 1rem;
}

footer .sosial a:hover {
    color: var(--background);
}

footer .link {
    margin-bottom: 1rem;
}

footer .link a {
    font-size: 1rem;
    color: #fff;
    font-weight: 700;
}

footer .credit {
    font-size: 1rem;
}

footer .credit a {
    color: var(--background);
    font-weight: 700;
}

/*meida quaris*/

/*laptop*/
@media (max-width: 1000px) {
    html {
        font-size: 75%;
    }
    .menu p {
        font-size: 1.5rem;
    }
}

/*lablet*/
@media (max-width: 500px) {
    html {
        font-size: 62.5%;
    }

    #hamburger-menu {
        display: inline-block;
    }

    .navbar .navbar-nav {
        position: absolute;
        top: 100%;
        right: -100%;
        background-color: #fff;
        width: 30rem;
        height: 100vh;
        transition: 0.3s;
    }

    .navbar .navbar-nav.active { 
        right: 0;
    }

    .navbar .navbar-nav a { 
        color: var(--background);
        display: block;
        margin: 1.5rem;
        padding: 0.5rem;
        font-size: 2rem;
    }

    .navbar .navbar-nav a::after{
        transform-origin: 0 0 ;
    }

    .navbar .navbar-nav a:hover::after {
        transform: scaleX(0.2);
    }

    .navbar .navbar-nav.active {
        right: 0;
    }

    .about .row {
        flex-wrap: wrap;
    }

    .about .row .about-img img {
        height: 24rem;
        object-fit: cover;
        object-position: center;
    }

    .about .row .content {
        padding: 0;
    }
    .about .row .content h3 {
        margin-top: 1rem;
        font-size: 2rem;
    }
    .about .row .content p {
        font-size: 1.5rem;
    }
    .menu p {
        font-size: 2rem;
    }

    .contact .row {
        flex-wrap: wrap;
    }
    .contact .row form {
        padding-top: 0;
        padding-bottom: 0;
    }
}

/*mobile phone*/
@media (max-width: 450px) {
    html {
        font-size: 55%;
    }
}

    </style>
</head>
<body>

    <!--Navbar star-->
    <nav class="Navbar">
        <a href="#" class="navbar-logo">kenangan<span>senja</span>,</a>

        <div class="navbar-nav">
            <a href="#">home</a>
            <a href="#about">tentang kami</a>
            <a href="#menu">menu</a>
            <a href="#contact">kontak</a>
        </div>

        <div class="navbar-extra">
            <a href="#" id="search"><i data-feather="search"></i></a>
            <a href="#" id="shopping-cart"><i data-feather="shopping-cart"></i></a>
            <a href="#" id="hamburger-menu"><i data-feather="menu"></i></a>

        </div>
    </nav>
    <!--Narvbar end-->

<!--hero section star-->
<section class="hero" id="home">
    <main class="content">
        <h1>mari menikmati secangkir <span>Kopi</span></h1>
        <p>Biji Kopi Arabika Berkualitas, <span>Terpercaya<span></p>
        <a href="#"class='cta'>beli sekarang</a>
    </main>
</section>
<!--hero section end-->

<!--about section start-->
<section id="about"class="about">
    <h2><span>Tentang</span> Kami</h2>

    <div class="row">
        <div class="about-img">
           <img src="Tentang Kami Kopi.jpg" alt="Tentang Kami">
        </div>
        <div class="content">
            <h3>Kenapa Memilih Kopi Kami</h3>
            <p>Kualitas biji kopi kami terjamin karena kami menerapkan beberapa standar penting,<p>

                <P>- *Pemilihan biji kopi dengan warna konsisten dan bebas bintik hitam* yang menandakan biji kopi segar dan bebas jamur</p>
                <p>- *Aroma biji kopi yang khas, segar, dan kuat*, sebagai indikator utama kesegaran dan kualitas kopi</p>
                <p>   Dengan standar tersebut, kami memastikan Anda mendapatkan biji kopi dengan rasa seimbang, aroma kuat, dan kualitas terbaik dari petani terpercaya</p>
    </div>
</section>
<!--about section end-->

<!--menu section strat-->
<section id="menu" class="menu">
    <h2><span>Menu</span> Kami</h2>
    <p>menu kami terdiri dari bji kopi arabika berkualitas yang berasal dari sumatera, dan vietnam</p>

    <div class="row">
        <div class="menu-card">
            <img src="arabika.jpeg" alt="arabika" class="menu-card-img">
            <h3 class="menu-card-title">-arabika-</h3>
            <p class="menu-card-price">IDR 130K per kg</p>
        </div>
        <div class="menu-card">
            <img src="arabika.jpeg" alt="arabika" class="menu-card-img">
            <h3 class="menu-card-title">-arabika sumatera-</h3>
            <p class="menu-card-price">IDR 149K per kg</p>
        </div>
        <div class="menu-card">
            <img src="arabika.jpeg" alt="arabika" class="menu-card-img">
            <h3 class="menu-card-title">-arabika vietnam-</h3>
            <p class="menu-card-price">IDR 199K per kg</p>
        </div>
        <div class="menu-card">
            <img src="arabika.jpeg" alt="arabika" class="menu-card-img">
            <h3 class="menu-card-title">-arabika premium-</h3>
            <p class="menu-card-price">IDR 350K per kg</p>
        </div>
    </div>
</section>
<!--menu section end-->

<!--contant section start-->
<section id="contact" class="contact">
    <h2><span>kontak</span> Kami</h2>
    <p>Bila adanya kendala dalam pemesanan atau komplan bisa menghubungi kontak dibawah</p>
    <div class="row">
        <iframe src="https://www.google.com/maps/embed?pb=!1m17!1m12!1m3!1d15840.62820064139!2d107.82861918210983!3d-6.990775639327415!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m2!1m1!2s!5e0!3m2!1sid!2sid!4v1749377939462!5m2!1sid!2sid" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade" class="maps"></iframe>
        
        <form action="">
            <div class="input-group">
                <i data-feather="user"></i>
                <input type="text" placeholder="nama">
            </div>
            <div class="input-group">
                <i data-feather="mail"></i>
                <input type="text" placeholder="email">
            </div>
            <div class="input-group">
                <i data-feather="phone"></i>
                <input type="text" placeholder="nomer hp">
            </div>
            <button type="submit" class="btn">Kirim Pesan</button>
        </form>
    </div>
</section>
<!--contant section end-->

<!--footer start-->
<footer>
    <div class="sosial">
        <a href="#"><i data-feather="instagram"></i></a>
    <div class="sosial">
        <a href="#"><i data-feather="facebook"></i></a>
    <div class="sosial">
        <a href="#"><i data-feather="twitter"></i></a>
    </div>

    <div class="link">
        <a href="#home">home</a>
        <a href="#about">Tentang Kami</a>
        <a href="#menu">menu</a>
        <a href="#contact">kontak</a>
    </div>

    <div class="credit">
        <p>credit by <a href="">Yudi prahasta adi sukma</a> &copy; 2025</p>
    </div>
</footer>
<!--footer end-->

    <!--Feather icons-->
    <script>
        feather.replace();
      </script>

      <!--my javascript-->
      <script src="script"></script>
</body>
</html>
