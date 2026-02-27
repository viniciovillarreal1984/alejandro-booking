[index.html](https://github.com/user-attachments/files/25609065/index.html)
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Alejandro's Booking - Accesorios LDNIO Ecuador</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #FF6B00;
            --secondary: #0066CC;
            --dark: #1a1a2e;
            --light: #f8f9fa;
            --accent: #00d4ff;
            --success: #00c851;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: var(--dark);
            overflow-x: hidden;
        }

        header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 20px rgba(0,0,0,0.1);
        }

        nav {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0.5rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .logo-icon {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, var(--secondary), var(--primary));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
        }

        .logo-text {
            display: flex;
            flex-direction: column;
        }

        .logo-main {
            font-size: 1.8rem;
            font-weight: 800;
            color: var(--secondary);
            line-height: 1;
        }

        .logo-sub {
            font-size: 0.9rem;
            color: var(--primary);
            font-weight: 600;
            letter-spacing: 3px;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 600;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .whatsapp-btn {
            background: var(--success);
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: all 0.3s;
        }

        .whatsapp-btn:hover {
            transform: scale(1.05);
        }

        .hero {
            margin-top: 80px;
            background: linear-gradient(135deg, var(--secondary) 0%, #0099ff 100%);
            padding: 5rem 2rem;
            text-align: center;
            color: white;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
        }

        .hero h1 span {
            color: var(--primary);
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
        }

        .badge-container {
            display: flex;
            justify-content: center;
            gap: 1rem;
            flex-wrap: wrap;
            margin-top: 2rem;
        }

        .badge {
            background: white;
            color: var(--secondary);
            padding: 0.8rem 1.5rem;
            border-radius: 50px;
            font-weight: 700;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .badge.discount {
            background: var(--primary);
            color: white;
            font-size: 1.2rem;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        .mayorista-banner {
            background: var(--primary);
            color: white;
            padding: 1.5rem;
            text-align: center;
            font-size: 1.2rem;
            font-weight: 600;
        }

        .mayorista-banner span {
            background: var(--secondary);
            padding: 0.2rem 0.8rem;
            border-radius: 20px;
            margin: 0 5px;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 3rem 2rem;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            color: white;
        }

        .section-title h2 {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
        }

        .filter-buttons {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-bottom: 3rem;
            flex-wrap: wrap;
        }

        .filter-btn {
            background: white;
            border: none;
            padding: 0.8rem 1.5rem;
            border-radius: 50px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s;
        }

        .filter-btn:hover, .filter-btn.active {
            background: var(--primary);
            color: white;
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
        }

        .product-card {
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            transition: transform 0.3s;
        }

        .product-card:hover {
            transform: translateY(-10px);
        }

        .product-image {
            width: 100%;
            height: 250px;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
        }

        .product-image i {
            font-size: 5rem;
            color: var(--secondary);
            opacity: 0.3;
        }

        .product-badge {
            position: absolute;
            top: 10px;
            left: 10px;
            background: var(--secondary);
            color: white;
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 700;
        }

        .product-badge.hot {
            background: #ff4757;
        }

        .product-info {
            padding: 1.5rem;
        }

        .product-code {
            color: #666;
            font-size: 0.9rem;
            margin-bottom: 0.5rem;
        }

        .product-title {
            font-size: 1.1rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
        }

        .product-specs {
            color: #666;
            font-size: 0.85rem;
            margin-bottom: 1rem;
        }

        .price-container {
            background: #f8f9fa;
            padding: 1rem;
            border-radius: 12px;
            margin-bottom: 1rem;
            border-left: 4px solid var(--secondary);
        }

        .price-row {
            display: flex;
            justify-content: space-between;
            margin-bottom: 0.5rem;
        }

        .price-row:last-child {
            border-top: 2px dashed #ccc;
            padding-top: 0.5rem;
            margin-bottom: 0;
        }

        .price-label {
            font-size: 0.85rem;
            color: #666;
        }

        .price {
            font-weight: 700;
        }

        .price.mayorista {
            color: var(--success);
            font-size: 1.2rem;
        }

        .savings {
            background: var(--primary);
            color: white;
            padding: 0.2rem 0.5rem;
            border-radius: 10px;
            font-size: 0.75rem;
        }

        .order-btn {
            width: 100%;
            background: linear-gradient(135deg, var(--secondary) 0%, #0099ff 100%);
            color: white;
            border: none;
            padding: 1rem;
            border-radius: 12px;
            font-weight: 700;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        .order-btn:hover {
            background: linear-gradient(135deg, var(--primary) 0%, #ff8c00 100%);
        }

        .contact-section {
            background: var(--dark);
            color: white;
            padding: 4rem 2rem;
            text-align: center;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            max-width: 1000px;
            margin: 3rem auto;
        }

        .contact-card {
            background: rgba(255,255,255,0.1);
            padding: 2rem;
            border-radius: 15px;
        }

        .contact-card i {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }

        .phone-display {
            font-size: 2rem;
            font-weight: 800;
            color: var(--primary);
            margin: 1rem 0;
        }

        footer {
            background: #0f0f1e;
            color: white;
            text-align: center;
            padding: 2rem;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-bottom: 1rem;
        }

        .social-links a {
            color: white;
            font-size: 1.5rem;
        }

        @media (max-width: 768px) {
            .hero h1 { font-size: 2rem; }
            .nav-links { display: none; }
            .products-grid { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>

    <header>
        <nav>
            <div class="logo">
                <div class="logo-icon">
                    <i class="fas fa-mobile-alt"></i>
                </div>
                <div class="logo-text">
                    <span class="logo-main">ALEJANDRO'S</span>
                    <span class="logo-sub">BOOKING</span>
                </div>
            </div>
            <ul class="nav-links">
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#productos">Productos</a></li>
                <li><a href="#contacto">Contacto</a></li>
            </ul>
            <a href="https://wa.me/593998469225" class="whatsapp-btn" target="_blank">
                <i class="fab fa-whatsapp"></i>
                Pedir
            </a>
        </nav>
    </header>

    <section class="hero" id="inicio">
        <div class="hero-content">
            <h1>Bienvenido a <span>Alejandro's Booking</span></h1>
            <p>Distribuidor Oficial LDNIO Ecuador. Importadores directos con garantía de 1 año.</p>
            <div class="badge-container">
                <div class="badge">
                    <i class="fas fa-shipping-fast"></i>
                    Envíos a todo el país
                </div>
                <div class="badge discount">
                    <i class="fas fa-percentage"></i>
                    -10% DESDE 20 UNIDADES
                </div>
                <div class="badge">
                    <i class="fas fa-shield-alt"></i>
                    Garantía 1 Año
                </div>
            </div>
        </div>
    </section>

    <div class="mayorista-banner">
        🏷️ DESCUENTO MAYORISTA: Compra <span>20+ unidades</span> y obtén <span>10% DE DESCUENTO</span>
    </div>

    <section class="container" id="productos">
        <div class="section-title">
            <h2>Catálogo de Productos</h2>
            <p>Precios por unidad. Descuento automático del 10% desde 20 unidades</p>
        </div>

        <div class="filter-buttons">
            <button class="filter-btn active" onclick="filterProducts('all')">Todos</button>
            <button class="filter-btn" onclick="filterProducts('audio')">Audífonos</button>
            <button class="filter-btn" onclick="filterProducts('cables')">Cables</button>
            <button class="filter-btn" onclick="filterProducts('cargadores')">Cargadores</button>
            <button class="filter-btn" onclick="filterProducts('powerbank')">Power Banks</button>
            <button class="filter-btn" onclick="filterProducts('auto')">Auto</button>
        </div>

        <div class="products-grid" id="productsGrid">
            
            <!-- AUDÍFONOS -->
            <div class="product-card fade-in" data-category="audio">
                <div class="product-image">
                    <i class="fas fa-headphones"></i>
                    <span class="product-badge hot">MÁS VENDIDO</span>
                </div>
                <div class="product-info">
                    <div class="product-code">Código: 15576</div>
                    <h3 class="product-title">Audífonos LD-T05 LDNIO</h3>
                    <p class="product-specs">36H reproducción • Bluetooth 5.3 • Cancelación de ruido</p>
                    <div class="price-container">
                        <div class="price-row">
                            <span class="price-label">Precio Unitario:</span>
                            <span class="price">$25.00</span>
                        </div>
                        <div class="price-row">
                            <span class="price-label">Desde 20 unids:</span>
                            <span class="price mayorista">$22.50 <span class="savings">AHORRA $2.50</span></span>
                        </div>
                    </div>
                    <button class="order-btn" onclick="orderProduct('15576', 'Audífonos LD-T05', 25)">
                        <i class="fab fa-whatsapp"></i> Pedir
                    </button>
                </div>
            </div>

            <div class="product-card fade-in" data-category="audio">
                <div class="product-image">
                    <i class="fas fa-headphones"></i>
                </div>
                <div class="product-info">
                    <div class="product-code">Código: 14989</div>
                    <h3 class="product-title">Audífonos LD-T01 LDNIO</h3>
                    <p class="product-specs">20H reproducción • Case con batería • Sonido estéreo</p>
                    <div class="price-container">
                        <div class="price-row">
                            <span class="price-label">Precio Unitario:</span>
                            <span class="price">$25.00</span>
                        </div>
                        <div class="price-row">
                            <span class="price-label">Desde 20 unids:</span>
                            <span class="price mayorista">$22.50</span>
                        </div>
                    </div>
                    <button class="order-btn" onclick="orderProduct('14989', 'Audífonos LD-T01', 25)">
                        <i class="fab fa-whatsapp"></i> Pedir
                    </button>
                </div>
            </div>

            <div class="product-card fade-in" data-category="audio">
                <div class="product-image">
                    <i class="fas fa-headphones"></i>
                </div>
                <div class="product-info">
                    <div class="product-code">Código: 15768</div>
                    <h3 class="product-title">Audífonos LD-N01 LDNIO</h3>
                    <p class="product-specs">Diseño deportivo • Resistente al sudor</p>
                    <div class="price-container">
                        <div class="price-row">
                            <span class="price-label">Precio Unitario:</span>
                            <span class="price">$15.00</span>
                        </div>
                        <div class="price-row">
                            <span class="price-label">Desde 20 unids:</span>
                            <span class="price mayorista">$13.50</span>
                        </div>
                    </div>
                    <button class="order-btn" onclick="orderProduct('15768', 'Audífonos LD-N01', 15)">
                        <i class="fab fa-whatsapp"></i> Pedir
                    </button>
                </div>
            </div>

            <!-- CABLES -->
            <div class="product-card fade-in" data-category="cables">
                <div class="product-image">
                    <i class="fas fa-plug"></i>
                    <span class="product-badge hot">POPULAR</span>
                </div>
                <div class="product-info">
                    <div class="product-code">Código: 15277</div>
                    <h3 class="product-title">Cable LS841 25W 1MT</h3>
                    <p class="product-specs">Carga rápida 25W • Samsung/Tipo C/iPhone</p>
                    <div class="price-container">
                        <div class="price-row">
                            <span class="price-label">Precio Unitario:</span>
                            <span class="price">$2.00</span>
                        </div>
                        <div class="price-row">
                            <span class="price-label">Desde 20 unids:</span>
                            <span class="price mayorista">$1.80</span>
                        </div>
                    </div>
                    <button class="order-btn" onclick="orderProduct('15277', 'Cable LS841 25W', 2)">
                        <i class="fab fa-whatsapp"></i> Pedir
                    </button>
                </div>
            </div>

            <div class="product-card fade-in" data-category="cables">
                <div class="product-image">
                    <i class="fas fa-plug"></i>
                </div>
                <div class="product-info">
                    <div class="product-code">Código: 14014</div>
                    <h3 class="product-title">Cable LS441 2.4A 1MT Goma</h3>
                    <p class="product-specs">Reforzado en goma • Alta resistencia</p>
                    <div class="price-container">
                        <div class="price-row">
                            <span class="price-label">Precio Unitario:</span>
                            <span class="price">$4.00</span>
                        </div>
                        <div class="price-row">
                            <span class="price-label">Desde 20 unids:</span>
                            <span class="price mayorista">$3.60</span>
                        </div>
                    </div>
                    <button class="order-btn" onclick="orderProduct('14014', 'Cable LS441 Goma', 4)">
                        <i class="fab fa-whatsapp"></i> Pedir
                    </button>
                </div>
            </div>

            <div class="product-card fade-in" data-category="cables">
                <div class="product-image">
                    <i class="fas fa-bolt"></i>
                </div>
                <div class="product-info">
                    <div class="product-code">Código: 15580</div>
                    <h3 class="product-title">Cable LC601 100W Tipo C</h3>
                    <p class="product-specs">Carga ultra rápida 100W • Tipo C a Tipo C</p>
                    <div class="price-container">
                        <div class="price-row">
                            <span class="price-label">Precio Unitario:</span>
                            <span class="price">$5.00</span>
                        </div>
                        <div class="price-row">
                            <span class="price-label">Desde 20 unids:</span>
                            <span class="price mayorista">$4.50</span>
                        </div>
                    </div>
                    <button class="order-btn" onclick="orderProduct('15580', 'Cable LC601 100W', 5)">
                        <i class="fab fa-whatsapp"></i> Pedir
                    </button>
                </div>
            </div>

            <!-- CARGADORES -->
            <div class="product-card fade-in" data-category="cargadores">
                <div class="product-image">
                    <i class="fas fa-charging-station"></i>
                </div>
                <div class="product-info">
                    <div class="product-code">Código: 15950</div>
                    <h3 class="product-title">Cargador Q1245W GaN 45W</h3>
                    <p class="product-specs">Tecnología GaN • 1 Tipo C + 1 USB</p>
                    <div class="price-container">
                        <div class="price-row">
                            <span class="price-label">Precio Unitario:</span>
                            <span class="price">$14.00</span>
                        </div>
                        <div class="price-row">
                            <span class="price-label">Desde 20 unids:</span>
                            <span class="price mayorista">$12.60</span>
                        </div>
                    </div>
                    <button class="order-btn" onclick="orderProduct('15950', 'Cargador Q1245W 45W', 14)">
                        <i class="fab fa-whatsapp"></i> Pedir
                    </button>
                </div>
            </div>

            <div class="product-card fade-in" data-category="cargadores">
                <div class="product-image">
                    <i class="fas fa-charging-station"></i>
                    <span class="product-badge">POTENTE</span>
                </div>
                <div class="product-info">
                    <div class="product-code">Código: 15951</div>
                    <h3 class="product-title">Cargador Q8100W GaN 100W</h3>
                    <p class="product-specs">3 Tipo C + 1 USB • Para laptops</p>
                    <div class="price-container">
                        <div class="price-row">
                            <span class="price-label">Precio Unitario:</span>
                            <span class="price">$38.00</span>
                        </div>
                        <div class="price-row">
                            <span class="price-label">Desde 20 unids:</span>
                            <span class="price mayorista">$34.20 <span class="savings">AHORRA $3.80</span></span>
                        </div>
                    </div>
                    <button class="order-btn" onclick="orderProduct('15951', 'Cargador Q8100W 100W', 38)">
                        <i class="fab fa-whatsapp"></i> Pedir
                    </button>
                </div>
            </div>

            <div class="product-card fade-in" data-category="cargadores">
                <div class="product-image">
                    <i class="fas fa-plug"></i>
                </div>
                <div class="product-info">
                    <div class="product-code">Código: 15332</div>
                    <h3 class="product-title">Cargador H1209C PD 20W</h3>
                    <p class="product-specs">Compacto • Power Delivery • Ideal iPhone</p>
                    <div class="price-container">
                        <div class="price-row">
                            <span class="price-label">Precio Unitario:</span>
                            <span class="price">$5.00</span>
                        </div>
                        <div class="price-row">
                            <span class="price-label">Desde 20 unids:</span>
                            <span class="price mayorista">$4.50</span>
                        </div>
                    </div>
                    <button class="order-btn" onclick="orderProduct('15332', 'Cargador H1209C 20W', 5)">
                        <i class="fab fa-whatsapp"></i> Pedir
                    </button>
                </div>
            </div>

            <!-- CARGADORES AUTO -->
            <div class="product-card fade-in" data-category="auto">
                <div class="product-image">
                    <i class="fas fa-car"></i>
                    <span class="product-badge hot">TOP VENTAS</span>
                </div>
                <div class="product-info">
                    <div class="product-code">Código: 15789</div>
                    <h3 class="product-title">Cargador Auto C103 60W</h3>
                    <p class="product-specs">1 PD + 1 USB • QC4.0 • Incluye cable</p>
                    <div class="price-container">
                        <div class="price-row">
                            <span class="price-label">Precio Unitario:</span>
                            <span class="price">$8.00</span>
                        </div>
                        <div class="price-row">
                            <span class="price-label">Desde 20 unids:</span>
                            <span class="price mayorista">$7.20</span>
                        </div>
                    </div>
                    <button class="order-btn" onclick="orderProduct('15789', 'Cargador Auto C103 60W', 8)">
                        <i class="fab fa-whatsapp"></i> Pedir
                    </button>
                </div>
            </div>

            <div class="product-card fade-in" data-category="auto">
                <div class="product-image">
                    <i class="fas fa-car-battery"></i>
                </div>
                <div class="product-info">
                    <div class="product-code">Código: 15796</div>
                    <h3 class="product-title">Cargador Auto C101 100W</h3>
                    <p class="product-specs">Ultra rápido 100W • Para laptops en auto</p>
                    <div class="price-container">
                        <div class="price-row">
                            <span class="price-label">Precio Unitario:</span>
                            <span class="price">$24.00</span>
                        </div>
                        <div class="price-row">
                            <span class="price-label">Desde 20 unids:</span>
                            <span class="price mayorista">$21.60</span>
                        </div>
                    </div>
                    <button class="order-btn" onclick="orderProduct('15796', 'Cargador Auto C101 100W', 24)">
                        <i class="fab fa-whatsapp"></i> Pedir
                    </button>
                </div>
            </div>

            <!-- POWER BANKS -->
            <div class="product-card fade-in" data-category="powerbank">
                <div class="product-image">
                    <i class="fas fa-battery-full"></i>
                    <span class="product-badge">NUEVO</span>
                </div>
                <div class="product-info">
                    <div class="product-code">Código: 15341</div>
                    <h3 class="product-title">Power Bank PQ19 10000mAh</h3>
                    <p class="product-specs">PD + QC3.0 + SCP • Pantalla LED • 22.5W</p>
                    <div class="price-container">
                        <div class="price-row">
                            <span class="price-label">Precio Unitario:</span>
                            <span class="price">$25.00</span>
                        </div>
                        <div class="price-row">
                            <span class="price-label">Desde 20 unids:</span>
                            <span class="price mayorista">$22.50 <span class="savings">AHORRA $2.50</span></span>
                        </div>
                    </div>
                    <button class="order-btn" onclick="orderProduct('15341', 'Power Bank PQ19 10000mAh', 25)">
                        <i class="fab fa-whatsapp"></i> Pedir
                    </button>
                </div>
            </div>

            <div class="product-card fade-in" data-category="powerbank">
                <div class="product-image">
                    <i class="fas fa-battery-three-quarters"></i>
                </div>
                <div class="product-info">
                    <div class="product-code">Código: 15579</div>
                    <h3 class="product-title">Power Bank PQ27 20000mAh 65W</h3>
                    <p class="product-specs">PD3.0 • 65W potencia • Para laptops</p>
                    <div class="price-container">
                        <div class="price-row">
                            <span class="price-label">Precio Unitario:</span>
                            <span class="price">$55.00</span>
                        </div>
                        <div class="price-row">
                            <span class="price-label">Desde 20 unids:</span>
                            <span class="price mayorista">$49.50 <span class="savings">AHORRA $5.50</span></span>
                        </div>
                    </div>
                    <button class="order-btn" onclick="orderProduct('15579', 'Power Bank PQ27 20000mAh 65W', 55)">
                        <i class="fab fa-whatsapp"></i> Pedir
                    </button>
                </div>
            </div>

        </div>
    </section>

    <section class="contact-section" id="contacto">
        <h2 style="font-size: 2.5rem; margin-bottom: 1rem;">¿Listo para hacer tu pedido?</h2>
        <p style="font-size: 1.2rem; margin-bottom: 2rem;">Contáctanos directamente por WhatsApp</p>
        
        <div class="contact-grid">
            <div class="contact-card">
                <i class="fab fa-whatsapp"></i>
                <h3>WhatsApp</h3>
                <p class="phone-display">+593 99 846 9225</p>
                <a href="https://wa.me/593998469225" class="whatsapp-btn" target="_blank" style="margin-top: 1rem;">
                    <i class="fab fa-whatsapp"></i> Escribir Ahora
                </a>
            </div>
            <div class="contact-card">
                <i class="fas fa-truck"></i>
                <h3>Envíos</h3>
                <p>A todo Ecuador</p>
            </div>
            <div class="contact-card">
                <i class="fas fa-shield-alt"></i>
                <h3>Garantía</h3>
                <p>1 año en todos los productos</p>
            </div>
            <div class="contact-card">
                <i class="fas fa-percentage"></i>
                <h3>Mayoristas</h3>
                <p>10% descuento desde 20 unidades</p>
            </div>
        </div>
    </section>

    <footer>
        <div class="social-links">
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="#"><i class="fab fa-facebook"></i></a>
            <a href="#"><i class="fab fa-tiktok"></i></a>
        </div>
        <p style="margin-bottom: 0.5rem;"><strong>@alejandrosbooking</strong></p>
        <p style="opacity: 0.7; font-size: 0.9rem;">
            © 2026 Alejandro's Booking - Distribuidor Oficial LDNIO Ecuador
        </p>
    </footer>

    <script>
        function filterProducts(category) {
            const cards = document.querySelectorAll('.product-card');
            const buttons = document.querySelectorAll('.filter-btn');
            
            buttons.forEach(btn => btn.classList.remove('active'));
            event.target.classList.add('active');
            
            cards.forEach(card => {
                if (category === 'all' || card.dataset.category === category) {
                    card.style.display = 'block';
                } else {
                    card.style.display = 'none';
                }
            });
        }

        function orderProduct(code, name, price) {
            const message = `¡Hola Alejandro! Quiero ordenar:%0A%0A📱 ${name}%0A🔢 Código: ${code}%0A💰 Precio: $${price.toFixed(2)} c/u%0A%0ACantidad: `;
            window.open(`https://wa.me/593998469225?text=${message}`, '_blank');
        }
    </script>

</body>
</html>
