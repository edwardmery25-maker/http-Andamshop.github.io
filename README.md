# http-Andamshop.github.io
<!DOCTYPE html>
<html lang="fa">
<head>

    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Totally Normal Store</title>

    <!-- Modern Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Playfair+Display:wght@500;600;700&display=swap"
          rel="stylesheet">


    <style>

        /* =========================
           GENERAL
        ========================= */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }


        body {

            font-family: "Inter", Arial, sans-serif;

            background: #ffffff;

            color: #142640;

        }


        a {
            text-decoration: none;
            color: inherit;
        }


        button {
            font-family: inherit;
        }



        /* =========================
           HEADER
        ========================= */

        header {

            height: 78px;

            background: #142640;

            color: white;

            display: flex;

            align-items: center;

            justify-content: space-between;

            padding: 0 6%;

            position: sticky;

            top: 0;

            z-index: 1000;

            border-bottom: 1px solid rgba(255,255,255,0.12);

        }



        /* LOGO */

        .logo {

            display: flex;

            align-items: center;

        }


        .logo img {

            height: 52px;

            width: auto;

            display: block;

        }



        /* NAVIGATION */

        nav {

            display: flex;

            align-items: center;

            gap: 28px;

        }


        nav a {

            color: white;

            font-size: 14px;

            font-weight: 500;

            transition: opacity 0.2s;

        }


        nav a:hover {

            opacity: 0.65;

        }



        /* =========================
           AMAZON-STYLE SEARCH ICON
        ========================= */

        .search-button {

            width: 46px;

            height: 40px;

            border: 1px solid rgba(255,255,255,0.8);

            border-radius: 20px;

            background: transparent;

            display: flex;

            align-items: center;

            justify-content: center;

            cursor: pointer;

            transition: background 0.2s;

        }


        .search-button:hover {

            background: rgba(255,255,255,0.12);

        }


        .search-icon {

            width: 17px;

            height: 17px;

            border: 2px solid white;

            border-radius: 50%;

            position: relative;

        }


        .search-icon::after {

            content: "";

            width: 7px;

            height: 2px;

            background: white;

            position: absolute;

            right: -5px;

            bottom: -3px;

            transform: rotate(45deg);

            border-radius: 2px;

        }



        /* =========================
           HERO
        ========================= */

        .hero {

            background: #142640;

            color: white;

            min-height: 400px;

            display: flex;

            align-items: center;

            justify-content: center;

            text-align: center;

            padding: 70px 20px;

        }


        .hero-content {

            max-width: 800px;

        }


        .hero-small {

            font-size: 12px;

            letter-spacing: 6px;

            margin-bottom: 20px;

            opacity: 0.75;

        }


        .hero h1 {

            font-family: "Playfair Display", Georgia, serif;

            font-size: clamp(48px, 7vw, 82px);

            line-height: 1;

            margin-bottom: 22px;

        }


        .hero p {

            font-size: 18px;

            opacity: 0.8;

        }



        /* =========================
           PRODUCTS SECTION
        ========================= */

        .products-section {

            padding: 80px 6% 100px;

        }


        .section-heading {

            text-align: center;

            margin-bottom: 50px;

        }


        .section-heading small {

            letter-spacing: 5px;

            font-size: 11px;

            font-weight: 600;

            color: #53657d;

        }


        .section-heading h2 {

            font-family: "Playfair Display", Georgia, serif;

            font-size: 42px;

            margin: 12px 0;

            color: #142640;

        }


        .section-heading p {

            color: #667386;

            font-size: 15px;

        }



        /* =========================
           PRODUCT GRID
        ========================= */

        .products {

            display: grid;

            grid-template-columns: repeat(4, 1fr);

            gap: 28px;

        }



        /* =========================
           PRODUCT CARD
        ========================= */

        .product {

            background: white;

            border: 1px solid #dce1e8;

            border-radius: 10px;

            overflow: hidden;

            transition: transform 0.2s, box-shadow 0.2s;

        }


        .product:hover {

            transform: translateY(-5px);

            box-shadow: 0 15px 35px rgba(20,38,64,0.10);

        }



        /* PRODUCT IMAGE */

        .product-image-container {

            position: relative;

            width: 100%;

            height: 260px;

            overflow: hidden;

            background: #eef1f5;

        }


        .product-image {

            width: 100%;

            height: 100%;

            object-fit: cover;

            display: block;

        }



        /* SOLD OUT BADGE */

        .sold-badge {

            position: absolute;

            top: 14px;

            left: 14px;

            background: #142640;

            color: white;

            padding: 7px 11px;

            border-radius: 5px;

            font-size: 10px;

            font-weight: 700;

            letter-spacing: 1px;

        }



        /* PRODUCT INFO */

        .product-info {

            padding: 22px;

        }


        .product-title {

            font-family: "Playfair Display", Georgia, serif;

            font-size: 21px;

            color: #142640;

            margin-bottom: 8px;

        }


        .product-description {

            color: #718096;

            font-size: 13px;

            line-height: 1.6;

            min-height: 42px;

            margin-bottom: 18px;

        }


        .price {

            font-size: 18px;

            font-weight: 700;

            color: #142640;

            margin-bottom: 16px;

        }



        /* BUY BUTTON */

        .buy-button {

            width: 100%;

            height: 44px;

            border: none;

            border-radius: 6px;

            background: #142640;

            color: white;

            cursor: pointer;

            font-size: 13px;

            font-weight: 600;

            transition: background 0.2s;

        }


        .buy-button:hover {

            background: #233c5d;

        }



        /* SOLD OUT BUTTON */

        .sold-button {

            background: #d8dde4;

            color: #536174;

            cursor: not-allowed;

        }


        .sold-button:hover {

            background: #d8dde4;

        }



        /* =========================
           POPUP
        ========================= */

        .popup-overlay {

            display: none;

            position: fixed;

            inset: 0;

            background: rgba(10,20,35,0.65);

            z-index: 5000;

            align-items: center;

            justify-content: center;

            padding: 20px;

        }


        .popup {

            width: 100%;

            max-width: 470px;

            background: white;

            border-radius: 12px;

            padding: 35px;

            text-align: center;

            box-shadow: 0 25px 70px rgba(0,0,0,0.3);

            animation: popupAppear 0.18s ease-out;

        }


        @keyframes popupAppear {

            from {

                opacity: 0;

                transform: scale(0.94);

            }

            to {

                opacity: 1;

                transform: scale(1);

            }

        }


        .popup-message {

            color: #142640;

            font-size: 17px;

            line-height: 1.9;

            margin-bottom: 25px;

        }


        .close-button {

            border: none;

            background: #142640;

            color: white;

            padding: 11px 30px;

            border-radius: 6px;

            cursor: pointer;

            font-size: 13px;

        }



        /* =========================
           FOOTER
        ========================= */

        footer {

            background: #142640;

            color: white;

            padding: 35px 6%;

            text-align: center;

        }


        footer p {

            opacity: 0.7;

            font-size: 12px;

        }



        /* =========================
           TABLET
        ========================= */

        @media (max-width: 1000px) {

            .products {

                grid-template-columns: repeat(2, 1fr);

            }

        }



        /* =========================
           MOBILE
        ========================= */

        @media (max-width: 650px) {

            header {

                height: 68px;

                padding: 0 20px;

            }


            .logo img {

                height: 44px;

            }


            nav {

                gap: 14px;

            }


            nav a {

                display: none;

            }


            .search-button {

                width: 43px;

                height: 37px;

            }


            .hero {

                min-height: 330px;

                padding: 60px 20px;

            }


            .hero h1 {

                font-size: 45px;

            }


            .hero p {

                font-size: 15px;

            }


            .products-section {

                padding: 60px 20px;

            }


            .section-heading h2 {

                font-size: 34px;

            }


            .products {

                grid-template-columns: 1fr;

            }


            .product-image-container {

                height: 280px;

            }

        }

    </style>

</head>



<body>


    <!-- =========================
         HEADER
    ========================== -->

    <header>

        <a href="#" class="logo">

            <img src="logo.png" alt="Totally Normal Store">

        </a>


        <nav>

            <a href="#"
               onclick="showMessage('به صفحه اصلی خوش آمدید.')">
                Home
            </a>


            <a href="#products"
               onclick="showMessage('چیزی برای دیدن نیست. همین‌ها هستند.')">
                Products
            </a>


            <a href="#"
               onclick="showMessage('اطلاعاتی درباره ما وجود ندارد.')">
                About
            </a>


            <a href="#"
               onclick="showMessage('لطفاً مزاحم نشوید.')">
                Contact
            </a>


            <!-- SEARCH -->

            <button
                class="search-button"
                onclick="showMessage('🔍 توی بدن خودت دنبالش بگرد، اینجا چیزی نیست.')"
                aria-label="Search">

                <span class="search-icon"></span>

            </button>

        </nav>

    </header>



    <!-- =========================
         HERO
    ========================== -->

    <section class="hero">

        <div class="hero-content">

            <div class="hero-small">
                WELCOME TO
            </div>


            <h1>
                Totally Normal Store
            </h1>


            <p>
                Everything you need. Probably.
            </p>

        </div>

    </section>



    <!-- =========================
         PRODUCTS
    ========================== -->

    <section class="products-section" id="products">


        <div class="section-heading">

            <small>
                OUR PRODUCTS
            </small>


            <h2>
                Some Totally Normal Stuff
            </h2>


            <p>
                Quality products for absolutely no reason.
            </p>

        </div>



        <div class="products">



            <!-- PRODUCT 1 -->

            <div class="product">

                <div class="product-image-container">

                    <img
                        src="product1.jpg"
                        alt="Product 1"
                        class="product-image">

                    <span class="sold-badge">
                        SOLD OUT
                    </span>

                </div>


                <div class="product-info">

                    <h3 class="product-title">
                        brain with average IQ
                    </h3>


                    <p class="product-description">
                        A completely normal product.
                    </p>


                    <div class="price">
                        29,900 $
                    </div>


                    <button
                        class="buy-button sold-button"
                        onclick="showMessage('این محصول فروخته شده. حتی خودمون هم نمی‌دونیم به کی.')">

                        SOLD OUT

                    </button>

                </div>

            </div>



            <!-- PRODUCT 2 -->

            <div class="product">

                <div class="product-image-container">

                    <img
                        src="product2.jpg"
                        alt="Product 2"
                        class="product-image">

                </div>


                <div class="product-info">

                    <h3 class="product-title">
                        heart for your lover
                    </h3>


                    <p class="product-description">
                        give her a real heart.
                    </p>


                    <div class="price">
                        39,900 $
                    </div>


                    <button
                        class="buy-button"
                        onclick="showMessage('به‌عنوان یه مدافع حقوق حیوانات، همچین کار غیرانسانی‌ای رو نمی‌ذارم بکنی. 🐦‍⬛‼️❌')">

                        خرید

                    </button>

                </div>

            </div>



            <!-- PRODUCT 3 -->

            <div class="product">

                <div class="product-image-container">

                    <img
                        src="product3.jpg"
                        alt="Product 3"
                        class="product-image">

                    <span class="sold-badge">
                        SOLD OUT
                    </span>

                </div>


                <div class="product-info">

                    <h3 class="product-title">
                        too rude to say
                    </h3>


                    <p class="product-description">
                        why is it so popular?
                    </p>


                    <div class="price">
                        49,900 $
                    </div>


                    <button
                        class="buy-button sold-button"
                        onclick="showMessage('این یکی هم فروخته شده. واقعاً سریع خرید می‌کنید.')">

                        SOLD OUT

                    </button>

                </div>

            </div>



            <!-- PRODUCT 4 -->

            <div class="product">

                <div class="product-image-container">

                    <img
                        src="product4.jpg"
                        alt="Product 4"
                        class="product-image">

                </div>


                <div class="product-info">

                    <h3 class="product-title">
                        perfect for alcoholics.
                    </h3>


                    <p class="product-description">
                        Nobody knows what this does.
                    </p>


                    <div class="price">
                        59,900 $
                    </div>


                    <button
                        class="buy-button"
                        onclick="showMessage('به‌عنوان یه مدافع حقوق حیوانات، همچین کار غیرانسانی‌ای رو نمی‌ذارم بکنی. 🐦‍⬛‼️❌')">

                        خرید

                    </button>

                </div>

            </div>



            <!-- PRODUCT 5 -->

            <div class="product">

                <div class="product-image-container">

                    <img
                        src="product5.jpg"
                        alt="Product 5"
                        class="product-image">

                </div>


                <div class="product-info">

                    <h3 class="product-title">
                        I promise you that's healthy.
                    </h3>


                    <p class="product-description">
                        If you keep smoking:
                    </p>


                    <div class="price">
                        69,900 $
                    </div>


                    <button
                        class="buy-button"
                        onclick="showMessage('به‌عنوان یه مدافع حقوق حیوانات، همچین کار غیرانسانی‌ای رو نمی‌ذارم بکنی. 🐦‍⬛‼️❌')">

                        خرید

                    </button>

                </div>

            </div>



            <!-- PRODUCT 6 -->

            <div class="product">

                <div class="product-image-container">

                    <img
                        src="product6.jpg"
                        alt="Product 6"
                        class="product-image">

                </div>


                <div class="product-info">

                    <h3 class="product-title">
                        Brown eye.
                    </h3>


                    <p class="product-description">
                        We think it's useful.
                    </p>


                    <div class="price">
                        7,900 $
                    </div>


                    <button
                        class="buy-button"
                        onclick="showMessage('به‌عنوان یه مدافع حقوق حیوانات، همچین کار غیرانسانی‌ای رو نمی‌ذارم بکنی. 🐦‍⬛‼️❌')">

                        خرید

                    </button>

                </div>

            </div>



            <!-- PRODUCT 7 -->

            <div class="product">

                <div class="product-image-container">

                    <img
                        src="product7.jpg"
                        alt="Product 7"
                        class="product-image">

                </div>


                <div class="product-info">

                    <h3 class="product-title">
                        2 of them.
                    </h3>


                    <p class="product-description">
                        Nobody asked for this.
                    </p>


                    <div class="price">
                        89,900 $
                    </div>


                    <button
                        class="buy-button"
                        onclick="showMessage('به‌عنوان یه مدافع حقوق حیوانات، همچین کار غیرانسانی‌ای رو نمی‌ذارم بکنی. 🐦‍⬛‼️❌')">

                        خرید

                    </button>

                </div>

            </div>



        
