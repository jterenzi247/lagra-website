<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LAGRA - Italian Vodka Spritz</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --cream: #F5F1ED;
            --warm-white: #FAFAF8;
            --travertine: #E8E3DB;
            --soft-gold: #D4AF87;
            --terracotta: #C85A3A;
            --olive: #6B7D5F;
            --stone-gray: #8B8B7E;
            --med-blue: #4A7BA7;
            --serif: 'Garamond', 'Georgia', serif;
            --sans: 'Helvetica Neue', 'Arial', sans-serif;
        }

        body {
            font-family: var(--sans);
            color: #2C2C2C;
            background: var(--warm-white);
            line-height: 1.6;
        }

        /* HEADER / NAV */
        header {
            background: var(--warm-white);
            padding: 1.5rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid var(--travertine);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .logo {
            font-family: var(--serif);
            font-size: 1.8rem;
            font-weight: 600;
            letter-spacing: 3px;
            color: #2C2C2C;
        }

        nav {
            display: flex;
            gap: 2.5rem;
            list-style: none;
        }

        nav a {
            text-decoration: none;
            color: #2C2C2C;
            font-size: 0.95rem;
            letter-spacing: 1px;
            transition: color 0.3s ease;
        }

        nav a:hover {
            color: var(--soft-gold);
        }

        .nav-cta {
            background: var(--olive);
            color: white;
            padding: 0.7rem 1.8rem;
            border-radius: 2px;
            text-decoration: none;
            font-size: 0.9rem;
            letter-spacing: 1px;
            transition: background 0.3s ease;
        }

        .nav-cta:hover {
            background: var(--terracotta);
        }

        @media (max-width: 768px) {
            nav {
                display: none;
            }
            .logo {
                font-size: 1.4rem;
            }
        }

        /* HERO SECTION */
        .hero {
            background: linear-gradient(135deg, var(--cream) 0%, var(--warm-white) 100%);
            padding: 6rem 2rem;
            text-align: center;
            min-height: 600px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        .hero h1 {
            font-family: var(--serif);
            font-size: 3.5rem;
            font-weight: 400;
            letter-spacing: 2px;
            margin-bottom: 1.5rem;
            color: #2C2C2C;
            line-height: 1.2;
        }

        .hero p {
            font-size: 1.3rem;
            color: var(--stone-gray);
            margin-bottom: 2.5rem;
            font-weight: 300;
            letter-spacing: 0.5px;
        }

        .hero-cta {
            display: inline-block;
            background: var(--olive);
            color: white;
            padding: 1rem 2.5rem;
            text-decoration: none;
            font-size: 0.95rem;
            letter-spacing: 1.5px;
            transition: all 0.3s ease;
            border: 2px solid var(--olive);
        }

        .hero-cta:hover {
            background: transparent;
            color: var(--olive);
        }

        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.2rem;
            }
            .hero p {
                font-size: 1.1rem;
            }
            .hero {
                padding: 4rem 1.5rem;
            }
        }

        /* PRODUCT SHOWCASE */
        .products {
            padding: 5rem 2rem;
            background: var(--warm-white);
        }

        .section-title {
            font-family: var(--serif);
            font-size: 2.8rem;
            text-align: center;
            margin-bottom: 0.5rem;
            color: #2C2C2C;
            font-weight: 400;
            letter-spacing: 1px;
        }

        .section-subtitle {
            text-align: center;
            color: var(--stone-gray);
            font-size: 1rem;
            margin-bottom: 3rem;
            letter-spacing: 0.5px;
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .product-card {
            background: var(--cream);
            padding: 2rem;
            text-align: center;
            border: 1px solid var(--travertine);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.08);
        }

        .product-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .product-card h3 {
            font-family: var(--serif);
            font-size: 1.6rem;
            margin-bottom: 0.5rem;
            color: #2C2C2C;
            font-weight: 400;
        }

        .product-origin {
            color: var(--soft-gold);
            font-size: 0.9rem;
            letter-spacing: 1px;
            margin-bottom: 1rem;
            text-transform: uppercase;
        }

        .product-card p {
            color: var(--stone-gray);
            font-size: 0.95rem;
            line-height: 1.8;
            margin-bottom: 1.5rem;
        }

        /* BRAND PILLARS */
        .pillars {
            background: var(--cream);
            padding: 5rem 2rem;
        }

        .pillars-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .pillar {
            text-align: center;
            padding: 1.5rem;
        }

        .pillar h4 {
            font-family: var(--serif);
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: #2C2C2C;
            font-weight: 400;
        }

        .pillar p {
            color: var(--stone-gray);
            font-size: 0.9rem;
        }

        /* PHILOSOPHY SECTION */
        .philosophy {
            background: var(--warm-white);
            padding: 5rem 2rem;
            text-align: center;
        }

        .philosophy-content {
            max-width: 700px;
            margin: 0 auto;
        }

        .philosophy-content h2 {
            font-family: var(--serif);
            font-size: 2.5rem;
            margin-bottom: 2rem;
            color: #2C2C2C;
            font-weight: 400;
            line-height: 1.4;
        }

        .philosophy-content p {
            color: var(--stone-gray);
            font-size: 1.1rem;
            margin-bottom: 1.5rem;
            line-height: 1.8;
        }

        /* CTA SECTION */
        .cta-section {
            background: linear-gradient(135deg, var(--olive) 0%, var(--stone-gray) 100%);
            color: white;
            padding: 4rem 2rem;
            text-align: center;
        }

        .cta-section h2 {
            font-family: var(--serif);
            font-size: 2.2rem;
            margin-bottom: 1rem;
            font-weight: 400;
            letter-spacing: 1px;
        }

        .cta-section p {
            font-size: 1rem;
            margin-bottom: 2rem;
            opacity: 0.95;
        }

        .cta-button {
            display: inline-block;
            background: white;
            color: var(--olive);
            padding: 1rem 2.5rem;
            text-decoration: none;
            font-weight: 600;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            border: 2px solid white;
        }

        .cta-button:hover {
            background: transparent;
            color: white;
        }

        /* FOOTER */
        footer {
            background: #2C2C2C;
            color: white;
            padding: 2.5rem;
            text-align: center;
            font-size: 0.9rem;
        }

        footer p {
            margin-bottom: 0.5rem;
            letter-spacing: 0.5px;
        }

        footer a {
            color: var(--soft-gold);
            text-decoration: none;
        }

        footer a:hover {
            text-decoration: underline;
        }

        /* RESPONSIVE */
        @media (max-width: 768px) {
            .section-title {
                font-size: 2rem;
            }
            .philosophy-content h2 {
                font-size: 1.8rem;
            }
            .cta-section h2 {
                font-size: 1.6rem;
            }
        }
    </style>
</head>
<body>

    <!-- HEADER -->
    <header>
        <div class="logo">LAGRA</div>
        <nav>
            <a href="#products">Products</a>
            <a href="#story">Our Story</a>
            <a href="#philosophy">Philosophy</a>
            <a href="#contact" class="nav-cta">Find Lagra</a>
        </nav>
    </header>

    <!-- HERO -->
    <section class="hero">
        <h1>Italian Summer.<br>Bottled.</h1>
        <p>Luxury vodka spritz crafted with real Italian ingredients.</p>
        <a href="#products" class="hero-cta">Discover Our Flavors</a>
    </section>

    <!-- PRODUCTS -->
    <section class="products" id="products">
        <h2 class="section-title">Core Collection</h2>
        <p class="section-subtitle">Crafted with premium vodka, sparkling water & authentic Italian ingredients.</p>
        
        <div class="product-grid">
            <div class="product-card">
                <div class="product-icon">🍊</div>
                <h3>Blood Orange</h3>
                <p class="product-origin">Sicilia</p>
                <p>Bright. Juicy. Elegant. The flagship that defines LAGRA.</p>
            </div>

            <div class="product-card">
                <div class="product-icon">🌸</div>
                <h3>Bergamot</h3>
                <p class="product-origin">Calabria</p>
                <p>Floral. Citrusy. Unexpected. The signature flavor nobody else owns.</p>
            </div>

            <div class="product-card">
                <div class="product-icon">🌿</div>
                <h3>Basil Citrus</h3>
                <p class="product-origin">Liguria</p>
                <p>Fresh basil. Italian lemon. Crisp. Sophisticated.</p>
            </div>
        </div>
    </section>

    <!-- BRAND PILLARS -->
    <section class="pillars">
        <h2 class="section-title">Our Foundation</h2>
        <p class="section-subtitle">Five principles guiding everything we craft.</p>
        
        <div class="pillars-grid">
            <div class="pillar">
                <h4>Italian Heritage</h4>
                <p>Inspired by centuries of aperitivo culture.</p>
            </div>
            <div class="pillar">
                <h4>Beautiful Simplicity</h4>
                <p>Luxury is choosing better, not adding more.</p>
            </div>
            <div class="pillar">
                <h4>Premium Ingredients</h4>
                <p>Real fruit. Real botanicals. No artificial anything.</p>
            </div>
            <div class="pillar">
                <h4>Modern Luxury</h4>
                <p>As comfortable at a yacht club as the Amalfi Coast.</p>
            </div>
            <div class="pillar">
                <h4>Gathering Together</h4>
                <p>Made for sunsets, tables, and shared moments.</p>
            </div>
        </div>
    </section>

    <!-- PHILOSOPHY -->
    <section class="philosophy" id="story">
        <div class="philosophy-content">
            <h2>Not Another Hard Seltzer</h2>
            <p>LAGRA is a premium lifestyle brand that brings the elegance of Italian aperitivo culture to modern America.</p>
            <p>We use premium vodka, natural sparkling water, and real Italian ingredients—nothing artificial, nothing unnecessary.</p>
            <p style="font-style: italic; color: var(--soft-gold);">Luxury isn't adding more. Luxury is choosing better.</p>
        </div>
    </section>

    <!-- CTA -->
    <section class="cta-section" id="contact">
        <h2>Find LAGRA Near You</h2>
        <p>Available at luxury hotels, country clubs, and premium retailers.</p>
        <a href="mailto:hello@lagra.com" class="cta-button">Get in Touch</a>
    </section>

    <!-- FOOTER -->
    <footer>
        <p>&copy; 2025 LAGRA. Italian Vodka Spritz.</p>
        <p>Crafted with real Sicilian blood oranges. | 4.5% ABV | 355 mL</p>
        <p><a href="#">Instagram</a> | <a href="#">Contact</a> | <a href="#">Retail Locator</a></p>
    </footer>

</body>
</html>
