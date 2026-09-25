<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Kigali Homes | Apartments for Rent</title>

    <style>

        /* =========================
           GENERAL STYLING
        ========================== */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, sans-serif;
            background: #f5f7fb;
            color: #172033;
        }


        /* =========================
           NAVIGATION BAR
        ========================== */

        nav {
            height: 75px;
            background: #102a43;

            display: flex;
            align-items: center;
            justify-content: space-between;

            padding: 0 8%;

            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .logo {
            color: white;
            font-size: 25px;
            font-weight: bold;
        }

        .logo span {
            color: #38d9a9;
        }

        .nav-links {
            display: flex;
            gap: 30px;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-size: 16px;
        }

        .nav-links a:hover {
            color: #38d9a9;
        }


        /* =========================
           HERO SECTION
        ========================== */

        .hero {
            min-height: 520px;

            display: flex;
            align-items: center;
            justify-content: center;

            text-align: center;

            padding: 60px 20px;

            background:
                linear-gradient(
                    rgba(16, 42, 67, 0.82),
                    rgba(16, 42, 67, 0.82)
                ),
                url("https://images.unsplash.com/photo-1600607687939-ce8a6c25118c?auto=format&fit=crop&w=1600&q=80");

            background-size: cover;
            background-position: center;
        }

        .hero-content {
            max-width: 800px;
            color: white;
        }

        .hero h1 {
            font-size: 60px;
            margin-bottom: 20px;
        }

        .hero h1 span {
            color: #38d9a9;
        }

        .hero p {
            font-size: 20px;
            line-height: 1.7;
            margin-bottom: 30px;
            color: #e8f1f8;
        }

        .hero-button {
            display: inline-block;

            background: #38d9a9;
            color: #102a43;

            padding: 15px 30px;

            border-radius: 30px;

            text-decoration: none;
            font-weight: bold;

            transition: 0.3s;
        }

        .hero-button:hover {
            transform: translateY(-4px);
            box-shadow: 0 10px 25px rgba(56, 217, 169, 0.4);
        }


        /* =========================
           SEARCH BAR
        ========================== */

        .search-area {
            background: white;

            width: 85%;
            max-width: 1000px;

            margin: -45px auto 60px;

            padding: 25px;

            border-radius: 15px;

            box-shadow: 0 10px 35px rgba(0, 0, 0, 0.12);

            position: relative;
        }

        .search-area h2 {
            margin-bottom: 15px;
            color: #102a43;
        }

        .search-box {
            display: flex;
            gap: 10px;
        }

        .search-box input {
            flex: 1;

            padding: 14px;

            border: 1px solid #ccd6e0;

            border-radius: 8px;

            font-size: 16px;
        }

        .search-box button {
            padding: 14px 25px;

            border: none;

            border-radius: 8px;

            background: #102a43;
            color: white;

            cursor: pointer;
        }

        .search-box button:hover {
            background: #38d9a9;
            color: #102a43;
        }


        /* =========================
           APARTMENT SECTION
        ========================== */

        .apartments {
            width: 85%;
            max-width: 1200px;

            margin: auto;

            padding-bottom: 80px;
        }

        .section-title {
            text-align: center;

            font-size: 38px;

            margin-bottom: 10px;

            color: #102a43;
        }

        .section-description {
            text-align: center;

            color: #68788a;

            margin-bottom: 40px;
        }


        /* =========================
           APARTMENT CARDS
        ========================== */

        .apartment-grid {
            display: grid;

            grid-template-columns:
                repeat(auto-fit, minmax(280px, 1fr));

            gap: 30px;
        }

        .card {
            background: white;

            border-radius: 16px;

            overflow: hidden;

            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.08);

            transition: 0.3s;
        }

        .card:hover {
            transform: translateY(-10px);

            box-shadow:
                0 15px 35px rgba(0, 0, 0, 0.15);
        }

        .card-image {
            width: 100%;
            height: 210px;

            object-fit: cover;
        }

        .card-content {
            padding: 22px;
        }

        .card-content h3 {
            font-size: 23px;

            color: #102a43;

            margin-bottom: 8px;
        }

        .location {
            color: #68788a;

            margin-bottom: 15px;
        }

        .details {
            display: flex;

            gap: 15px;

            margin-bottom: 18px;

            color: #52616f;

            font-size: 14px;
        }


        /* =========================
           PRICE TAG
        ========================== */

        .price {
            display: inline-block;

            background: #38d9a9;

            color: #102a43;

            font-size: 20px;

            font-weight: bold;

            padding: 10px 15px;

            border-radius: 8px;

            margin-bottom: 18px;
        }


        /* =========================
           CARD BUTTON
        ========================== */

        .view-button {
            display: block;

            width: 100%;

            padding: 12px;

            background: #102a43;

            color: white;

            text-align: center;

            text-decoration: none;

            border-radius: 8px;

            transition: 0.3s;
        }

        .view-button:hover {
            background: #38d9a9;
            color: #102a43;
        }


        /* =========================
           WHY CHOOSE US
        ========================== */

        .why {
            background: #102a43;

            color: white;

            text-align: center;

            padding: 70px 10%;
        }

        .why h2 {
            font-size: 38px;

            margin-bottom: 40px;
        }

        .features {
            display: flex;

            justify-content: center;

            gap: 30px;

            flex-wrap: wrap;
        }

        .feature {
            max-width: 250px;

            padding: 25px;
        }

        .feature-icon {
            font-size: 45px;

            margin-bottom: 15px;
        }

        .feature h3 {
            margin-bottom: 10px;

            color: #38d9a9;
        }

        .feature p {
            line-height: 1.6;

            color: #d5e2eb;
        }


        /* =========================
           FOOTER
        ========================== */

        footer {
            background: #071827;

            color: #aebdca;

            text-align: center;

            padding: 30px;
        }

        footer strong {
            color: #38d9a9;
        }


        /* =========================
           MOBILE DESIGN
        ========================== */

        @media (max-width: 700px) {

            .hero h1 {
                font-size: 42px;
            }

            .nav-links {
                gap: 10px;
            }

            .nav-links a {
                font-size: 13px;
            }

            .search-box {
                flex-direction: column;
            }

            .search-area {
                width: 90%;
            }

            .apartments {
                width: 90%;
            }
        }

    </style>
</head>


<body>


    <!-- =========================
         NAVIGATION
    ========================== -->

    <nav>

        <div class="logo">
            Kigali<span>Homes</span>
        </div>

        <div class="nav-links">

            <a href="#home">Home</a>

            <a href="#apartments">Apartments</a>

            <a href="#about">About</a>

        </div>

    </nav>



    <!-- =========================
         HERO
    ========================== -->

    <section class="hero" id="home">

        <div class="hero-content">

            <h1>
                Find Your
                <span>Perfect Home</span>
            </h1>

            <p>
                Discover beautiful apartments available
                for rent across Kigali, Rwanda.
            </p>

            <a
                href="#apartments"
                class="hero-button"
            >
                Explore Apartments
            </a>

        </div>

    </section>



    <!-- =========================
         SEARCH
    ========================== -->

    <div class="search-area">

        <h2>🔎 Find an Apartment</h2>

        <div class="search-box">

            <input
                type="text"
                placeholder="Search by location..."
            >

            <button>
                Search
            </button>

        </div>

    </div>



    <!-- =========================
         APARTMENTS
    ========================== -->

    <section
        class="apartments"
        id="apartments"
    >

        <h2 class="section-title">
            Apartments in Kigali
        </h2>

        <p class="section-description">
            Explore different apartment styles and
            monthly rental prices.
        </p>


        <div class="apartment-grid">


            <!-- APARTMENT 1 -->

            <div class="card">

                <img
                    class="card-image"
                    src="https://images.unsplash.com/photo-1600607687920-4e2a09cf159d?auto=format&fit=crop&w=800&q=80"
                    alt="Modern apartment"
                >

                <div class="card-content">

                    <h3>
                        Modern City Apartment
                    </h3>

                    <p class="location">
                        📍 Kacyiru, Kigali
                    </p>

                    <div class="details">

                        <span>🛏 2 Beds</span>

                        <span>🚿 2 Baths</span>

                        <span>📐 85 m²</span>

                    </div>

                    <div class="price">
                        RWF 800,000 / month
                    </div>

                    <a
                        href="#"
                        class="view-button"
                    >
                        View Apartment
                    </a>

                </div>

            </div>



            <!-- APARTMENT 2 -->

            <div class="card">

                <img
                    class="card-image"
                    src="https://images.unsplash.com/photo-1600566753086-00f18fb6b3ea?auto=format&fit=crop&w=800&q=80"
                    alt="Luxury apartment"
                >

                <div class="card-content">

                    <h3>
                        Luxury Family Apartment
                    </h3>

                    <p class="location">
                        📍 Gacuriro, Kigali
                    </p>

                    <div class="details">

                        <span>🛏 3 Beds</span>

                        <span>🚿 3 Baths</span>

                        <span>📐 120 m²</span>

                    </div>

                    <div class="price">
                        RWF 1,500,000 / month
                    </div>

                    <a
                        href="#"
                        class="view-button"
                    >
                        View Apartment
                    </a>

                </div>

            </div>



            <!-- APARTMENT 3 -->

            <div class="card">

                <img
                    class="card-image"
                    src="https://images.unsplash.com/photo-1600607688969-a5bfcd646154?auto=format&fit=crop&w=800&q=80"
                    alt="Apartment interior"
                >

                <div class="card-content">

                    <h3>
                        Comfortable Apartment
                    </h3>

                    <p class="location">
                        📍 Kimironko, Kigali
                    </p>

                    <div class="details">

                        <span>🛏 2 Beds</span>

                        <span>🚿 2 Baths</span>

                        <span>📐 90 m²</span>

                    </div>

                    <div class="price">
                        RWF 700,000 / month
                    </div>

                    <a
                        href="#"
                        class="view-button"
                    >
                        View Apartment
                    </a>

                </div>

            </div>



            <!-- APARTMENT 4 -->

            <div class="card">

                <img
                    class="card-image"
                    src="https://images.unsplash.com/photo-1600607687920-4e2a09cf159d?auto=format&fit=crop&w=800&q=80"
                    alt="Apartment in Kigali"
                >

                <div class="card-content">

                    <h3>
                        Elegant City Home
                    </h3>

                    <p class="location">
                        📍 Nyarutarama, Kigali
                    </p>

                    <div class="details">

                        <span>🛏 2 Beds</span>

                        <span>🚿 2 Baths</span>

                        <span>📐 100 m²</span>

                    </div>

                    <div class="price">
                        RWF 1,200,000 / month
                    </div>

                    <a
                        href="#"
                        class="view-button"
                    >
                        View Apartment
                    </a>

                </div>

            </div>



            <!-- APARTMENT 5 -->

            <div class="card">

                <img
                    class="card-image"
                    src="https://images.unsplash.com/photo-1600210492486-724fe5c67fb0?auto=format&fit=crop&w=800&q=80"
                    alt="Affordable apartment"
                >

                <div class="card-content">

                    <h3>
                        Affordable Apartment
                    </h3>

                    <p class="location">
                        📍 Kicukiro, Kigali
                    </p>

                    <div class="details">

                        <span>🛏 1 Bed</span>

                        <span>🚿 1 Bath</span>

                        <span>📐 55 m²</span>

                    </div>

                    <div class="price">
                        RWF 500,000 / month
                    </div>

                    <a
                        href="#"
                        class="view-button"
                    >
                        View Apartment
                    </a>

                </div>

            </div>



            <!-- APARTMENT 6 -->

            <div class="card">

                <img
                    class="card-image"
                    src="https://images.unsplash.com/photo-1600566753190-17f0baa2a6c3?auto=format&fit=crop&w=800&q=80"
                    alt="Furnished apartment"
                >

                <div class="card-content">

                    <h3>
                        Furnished Apartment
                    </h3>

                    <p class="location">
                        📍 Kimihurura, Kigali
                    </p>

                    <div class="details">

                        <span>🛏 2 Beds</span>

                        <span>🚿 2 Baths</span>

                        <span>📐 95 m²</span>

                    </div>

                    <div class="price">
                        RWF 1,300,000 / month
                    </div>

                    <a
                        href="#"
                        class="view-button"
                    >
                        View Apartment
                    </a>

                </div>

            </div>


        </div>

    </section>



    <!-- =========================
         WHY CHOOSE US
    ========================== -->

    <section
        class="why"
        id="about"
    >

        <h2>
            Why KigaliHomes?
        </h2>

        <div class="features">


            <div class="feature">

                <div class="feature-icon">
                    🏠
                </div>

                <h3>
                    Many Homes
                </h3>

                <p>
                    Browse different types of
                    apartments across Kigali.
                </p>

            </div>



            <div class="feature">

                <div class="feature-icon">
                    💰
                </div>

                <h3>
                    Clear Prices
                </h3>

                <p>
                    See the monthly rental price
                    directly on each apartment.
                </p>

            </div>



            <div class="feature">

                <div class="feature-icon">
                    📍
                </div>

                <h3>
                    Kigali Locations
                </h3>

                <p>
                    Explore apartments in different
                    neighborhoods of Kigali.
                </p>

            </div>


        </div>

    </section>



    <!-- =========================
         FOOTER
    ========================== -->

    <footer>

        <p>
            © 2026
            <strong>KigaliHomes</strong>
            — Kigali Apartment Finder
        </p>

        <p>
            School project demonstration
        </p>

    </footer>


</body>

</html>
