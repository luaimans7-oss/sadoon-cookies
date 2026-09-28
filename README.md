<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>سعدون كوكيز | Sadoon Cookies</title>

    <!-- Google Fonts: Readex Pro (حديث وأنيق جداً) -->
    <link href="https://fonts.googleapis.com/css2?family=Readex+Pro:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        :root {
            --primary: #1e1411; /* بني قهوة عميق */
            --accent: #d39e68; /* كراميل ناعم */
            --accent-light: #f5e9dc; /* كراميل خفيف جداً */
            --bg: #fbf8f5; /* خلفية كريمية ناعمة */
            --surface: #ffffff; /* أبيض للبطاقات */
            --text: #2c221e; /* نص داكن ناعم */
            --text-muted: #7c6f68; /* نص فرعي رمادي دافئ */
            --radius: 20px; /* انحناءات عصرية */
            --shadow: 0 10px 30px rgba(30, 20, 17, 0.05);
            --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            background: var(--bg);
            color: var(--text);
            font-family: 'Readex Pro', sans-serif;
            line-height: 1.7;
            overflow-x: hidden;
        }

        /* Header & Navigation */
        header {
            background: rgba(251, 248, 245, 0.9);
            backdrop-filter: blur(12px);
            padding: 18px 8%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
            border-bottom: 1px solid rgba(211, 158, 104, 0.2);
        }

        .logo {
            font-size: 22px;
            font-weight: 700;
            color: var(--primary);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo-icon {
            width: 38px;
            height: 38px;
            background: var(--accent);
            color: white;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 18px;
        }

        nav {
            display: flex;
            align-items: center;
            gap: 15px;
            background: rgba(255, 255, 255, 0.8);
            padding: 6px 12px;
            border-radius: 50px;
            border: 1px solid rgba(0, 0, 0, 0.05);
        }

            nav a {
                color: var(--text-muted);
                text-decoration: none;
                font-size: 14px;
                font-weight: 500;
                padding: 8px 18px;
                border-radius: 30px;
                transition: var(--transition);
                cursor: pointer;
            }

                nav a.active, nav a:hover {
                    color: var(--primary);
                    background: var(--accent-light);
                    font-weight: 600;
                }

        .lang-btn {
            background: var(--primary);
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 30px;
            cursor: pointer;
            font-family: 'Readex Pro', sans-serif;
            font-size: 13px;
            font-weight: 500;
            transition: var(--transition);
        }

            .lang-btn:hover {
                background: var(--accent);
            }

        /* Page Switch Management */
        .page {
            display: none;
            animation: fadeInUp 0.4s ease-out;
        }

            .page.active-page {
                display: block;
            }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Hero Section */
        .hero {
            padding: 90px 8% 60px;
            display: grid;
            grid-template-columns: 1.2fr 0.8fr;
            gap: 40px;
            align-items: center;
        }

        .hero-text h1 {
            font-size: 46px;
            font-weight: 700;
            color: var(--primary);
            line-height: 1.25;
            margin-bottom: 15px;
        }

            .hero-text h1 span {
                color: var(--accent);
            }

        .hero-badge {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: var(--accent-light);
            color: var(--primary);
            padding: 6px 16px;
            border-radius: 30px;
            font-size: 13px;
            font-weight: 600;
            margin-bottom: 20px;
        }

        .hero-text p {
            font-size: 16px;
            color: var(--text-muted);
            margin-bottom: 30px;
            max-width: 520px;
        }

        .btn-group {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }

        .btn-main {
            background: var(--primary);
            color: white;
            padding: 14px 32px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 15px;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            transition: var(--transition);
            border: none;
            cursor: pointer;
        }

            .btn-main:hover {
                background: var(--accent);
                transform: translateY(-2px);
                box-shadow: 0 10px 20px rgba(211, 158, 104, 0.3);
            }

        .btn-sub {
            background: var(--surface);
            color: var(--primary);
            padding: 14px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 15px;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            border: 1px solid rgba(0, 0, 0, 0.08);
            transition: var(--transition);
        }

            .btn-sub:hover {
                background: var(--accent-light);
            }

        .hero-img-box {
            position: relative;
        }

            .hero-img-box img {
                width: 100%;
                border-radius: 28px;
                box-shadow: var(--shadow);
                object-fit: cover;
                height: 420px;
            }

        /* Common Section Elements */
        section {
            padding: 60px 8%;
        }

        .section-title {
            text-align: center;
            margin-bottom: 45px;
        }

            .section-title h2 {
                font-size: 32px;
                color: var(--primary);
                font-weight: 700;
                margin-bottom: 8px;
            }

            .section-title p {
                color: var(--text-muted);
                font-size: 15px;
            }

        /* Info Cards Grid */
        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 20px;
        }

        .info-card {
            background: var(--surface);
            padding: 28px 24px;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            border: 1px solid rgba(0,0,0,0.03);
            transition: var(--transition);
        }

            .info-card:hover {
                transform: translateY(-5px);
            }

            .info-card i {
                font-size: 26px;
                color: var(--accent);
                margin-bottom: 15px;
            }

            .info-card h3 {
                font-size: 18px;
                color: var(--primary);
                margin-bottom: 6px;
            }

            .info-card p {
                font-size: 14px;
                color: var(--text-muted);
            }

        /* Menu Grid */
        .menu-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
        }

        .menu-card {
            background: var(--surface);
            border-radius: var(--radius);
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
            border: 1px solid rgba(0,0,0,0.03);
            display: flex;
            flex-direction: column;
        }

            .menu-card:hover {
                transform: translateY(-6px);
                box-shadow: 0 15px 35px rgba(30, 20, 17, 0.08);
            }

            .menu-card img {
                width: 100%;
                height: 200px;
                object-fit: cover;
            }

        .menu-card-body {
            padding: 22px;
            display: flex;
            flex-direction: column;
            flex-grow: 1;
        }

        .menu-card-head {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 10px;
        }

            .menu-card-head h3 {
                font-size: 17px;
                font-weight: 600;
                color: var(--primary);
            }

        .price-tag {
            background: var(--accent-light);
            color: var(--primary);
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 13px;
            font-weight: 700;
        }

        .menu-card-body p {
            color: var(--text-muted);
            font-size: 13px;
            line-height: 1.6;
        }

        /* Reviews Section */
        .reviews-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
        }

        .review-card {
            background: var(--surface);
            padding: 28px;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            border: 1px solid rgba(0,0,0,0.03);
        }

        .stars {
            color: #f59e0b;
            margin-bottom: 12px;
            font-size: 14px;
        }

        .review-card p {
            font-size: 14px;
            color: var(--text);
            margin-bottom: 20px;
        }

        .reviewer {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .avatar {
            width: 40px;
            height: 40px;
            background: var(--accent-light);
            color: var(--primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            font-size: 15px;
        }

        .reviewer span {
            font-size: 14px;
            font-weight: 600;
            color: var(--primary);
        }

        /* About Card */
        .about-box {
            background: var(--surface);
            padding: 50px 40px;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            text-align: center;
            max-width: 800px;
            margin: 0 auto;
        }

            .about-box p {
                color: var(--text-muted);
                font-size: 16px;
                line-height: 1.9;
            }

        /* Contact Card */
        .contact-box {
            background: var(--surface);
            padding: 40px;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            max-width: 750px;
            margin: 0 auto;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 14px;
            color: var(--text);
        }

            .contact-item i {
                color: var(--accent);
                font-size: 18px;
            }

        /* Footer */
        footer {
            text-align: center;
            padding: 30px;
            color: var(--text-muted);
            font-size: 13px;
            border-top: 1px solid rgba(0,0,0,0.05);
            margin-top: 40px;
        }

            footer span {
                color: var(--primary);
                font-weight: 600;
            }

        /* Responsive */
        @media (max-width: 900px) {
            .hero {
                grid-template-columns: 1fr;
                text-align: center;
                padding-top: 40px;
            }

            .hero-text p {
                margin-left: auto;
                margin-right: auto;
            }

            .btn-group {
                justify-content: center;
            }

            header {
                flex-direction: column;
                gap: 15px;
            }

            nav {
                flex-wrap: wrap;
                justify-content: center;
            }
        }
    </style>
</head>
<body>

    <!-- Header Section -->
    <header>
        <div class="logo">
            <div class="logo-icon"><i class="fa-solid fa-cookie"></i></div>
            <span id="logo-text">سعدون كوكيز</span>
        </div>

        <nav>
            <a class="nav-link active" onclick="showPage('home')" id="nav-home">الرئيسية</a>
            <a class="nav-link" onclick="showPage('menu')" id="nav-menu">القائمة</a>
            <a class="nav-link" onclick="showPage('reviews')" id="nav-reviews">التقييمات</a>
            <a class="nav-link" onclick="showPage('about')" id="nav-about">عن الكافيه</a>
            <a class="nav-link" onclick="showPage('contact')" id="nav-contact">التواصل</a>
        </nav>

        <button class="lang-btn" onclick="toggleLanguage()">
            <span id="lang-text">English</span>
        </button>
    </header>

    <!-- HOME PAGE -->
    <div id="page-home" class="page active-page">
        <section class="hero">
            <div class="hero-text">
                <div class="hero-badge">
                    <i class="fa-solid fa-star"></i> <span id="hero-rating">4.7 من 70 تقييم</span>
                </div>
                <h1>طعم الكوكيز الطازج <span>والقهوة المختصة</span></h1>
                <p id="hero-desc">استمتع بتجربة فريدة في العامرات مع أفضل أنواع الكوكيز المخبوز يومياً والمشروبات الخاصة.</p>

                <div class="btn-group">
                    <button class="btn-main" onclick="showPage('menu')" id="btn-view-menu">
                        <i class="fa-solid fa-utensils"></i> استعرض القائمة
                    </button>
                    <a class="btn-sub" href="tel:92909050" id="btn-call">
                        <i class="fa-solid fa-phone"></i> اتصل بنا
                    </a>
                </div>
            </div>

            <div class="hero-img-box">
                <img src="https://images.unsplash.com/photo-1499636136210-6f4ee915583e?auto=format&fit=crop&w=800&q=80" alt="سعدون كوكيز">
            </div>
        </section>

        <section>
            <div class="section-title">
                <h2 id="info-title">معلومات عن الكافيه</h2>
                <p id="info-subtitle">تفاصيل الخدمة والموقع لزيارتك القادمة</p>
            </div>

            <div class="info-grid">
                <div class="info-card">
                    <i class="fa-solid fa-star"></i>
                    <h3 id="info-rating-label">التقييم</h3>
                    <p>4.7 من أصل 5 (70 تقييم)</p>
                </div>
                <div class="info-card">
                    <i class="fa-solid fa-location-dot"></i>
                    <h3 id="info-location-label">الموقع</h3>
                    <p id="info-loc">العامرات، مسقط</p>
                </div>
                <div class="info-card">
                    <i class="fa-solid fa-tag"></i>
                    <h3 id="info-price-label">مستوى الأسعار</h3>
                    <p>OMR 0 - 2 للفرد</p>
                </div>
                <div class="info-card">
                    <i class="fa-solid fa-clock"></i>
                    <h3 id="info-hours-label">ساعات العمل</h3>
                    <p id="info-hours">مفتوح يومياً حتى 12 منتصف الليل</p>
                </div>
            </div>
        </section>
    </div>

    <!-- MENU PAGE -->
    <div id="page-menu" class="page">
        <section>
            <div class="section-title">
                <h2 id="menu-title">قائمة المشروبات والكوكيز</h2>
                <p id="menu-subtitle">منيو متنوع يلبي ذوقك من المخبوزات والقهوة</p>
            </div>

            <div class="menu-grid">
                <div class="menu-card">
                    <img src="https://images.unsplash.com/photo-1558961363-fa8fdf82db35?auto=format&fit=crop&w=800&q=80" alt="كيندر كوكيز">
                    <div class="menu-card-body">
                        <div class="menu-card-head">
                            <h3>كيندر كوكيز</h3>
                            <span class="price-tag">0.800 OMR</span>
                        </div>
                        <p>كوكيز طازج محشو بشوكولاتة الكيندر الغنية واللذيذة.</p>
                    </div>
                </div>

                <div class="menu-card">
                    <img src="https://images.unsplash.com/photo-1517256064527-09c73fc73e38?auto=format&fit=crop&w=800&q=80" alt="سبانيش لاتيه">
                    <div class="menu-card-body">
                        <div class="menu-card-head">
                            <h3>سبانيش لاتيه مميز</h3>
                            <span class="price-tag">1.500 OMR</span>
                        </div>
                        <p>مزيج رائع من الإسبريسو والحليب المكثف بارد أو ساخن.</p>
                    </div>
                </div>

                <div class="menu-card">
                    <img src="https://images.unsplash.com/photo-1606313564200-e75d5e30476c?auto=format&fit=crop&w=800&q=80" alt="كيكة الشوكولاتة">
                    <div class="menu-card-body">
                        <div class="menu-card-head">
                            <h3>كيكة الشوكولاتة</h3>
                            <span class="price-tag">1.200 OMR</span>
                        </div>
                        <p>كيك شوكولاتة غني وقوام هش ورائع جداً للتحلية.</p>
                    </div>
                </div>

                <div class="menu-card">
                    <img src="https://images.unsplash.com/photo-1556679343-c7306c1976bc?auto=format&fit=crop&w=800&q=80" alt="أيس تي">
                    <div class="menu-card-body">
                        <div class="menu-card-head">
                            <h3>شاي مثلج (Ice Tea)</h3>
                            <span class="price-tag">1.000 OMR</span>
                        </div>
                        <p>مشروب الشاي المثلج المنعش بنكهات مميزة وخفيفة.</p>
                    </div>
                </div>

                <div class="menu-card">
                    <img src="https://images.unsplash.com/photo-1534778101976-62847782c213?auto=format&fit=crop&w=800&q=80" alt="لاتيه">
                    <div class="menu-card-body">
                        <div class="menu-card-head">
                            <h3>لاتيه كلاسيك</h3>
                            <span class="price-tag">1.200 OMR</span>
                        </div>
                        <p>قهوة الإسبريسو مع الحليب المبخر والرغوة الناعمة.</p>
                    </div>
                </div>

                <div class="menu-card">
                    <img src="https://images.unsplash.com/photo-1509440159596-0249088772ff?auto=format&fit=crop&w=800&q=80" alt="بوكس كوكيز">
                    <div class="menu-card-body">
                        <div class="menu-card-head">
                            <h3>بوكس كوكيز مشكل</h3>
                            <span class="price-tag">2.000 OMR</span>
                        </div>
                        <p>مجموعة متنوعة من أفضل أنواع الكوكيز للمشاركة.</p>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- REVIEWS PAGE -->
    <div id="page-reviews" class="page">
        <section>
            <div class="section-title">
                <h2 id="reviews-title">آراء الزوار</h2>
                <p id="reviews-subtitle">انطباعات وتجارب زبائننا الكرام</p>
            </div>

            <div class="reviews-grid">
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <p>"أفضل كيكة شوكولاتة وشاي مثلج في العامرات! الكوكيز عندهم هش وطازج جداً."</p>
                    <div class="reviewer">
                        <div class="avatar">P</div>
                        <span>Prince Junaid</span>
                    </div>
                </div>

                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <p>"السبانيش لاتيه مميز جداً والخدمة سريعة وراقية."</p>
                    <div class="reviewer">
                        <div class="avatar">M</div>
                        <span>Mahmood Alsayeghi</span>
                    </div>
                </div>

                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <p>"المكان هادئ ولطيف، الكيندر كوكيز يفوز والمشروبات ممتازة."</p>
                    <div class="reviewer">
                        <div class="avatar">P</div>
                        <span>Positive Video</span>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- ABOUT PAGE -->
    <div id="page-about" class="page">
        <section>
            <div class="section-title">
                <h2 id="about-title">عن سعدون كوكيز</h2>
            </div>

            <div class="about-box">
                <p id="about-desc">
                    يقدم سعدون كوكيز في العامرات تجربة ممتازة لعشاق الكوكيز الطازج والقهوة.
                    نحرص على تحضير منتجاتنا يومياً باستخدام مكونات عالية الجودة، وتوفير خيارات التناول الداخلي،
                    الطلب السفري، والتوصيل المباشر عبر تطبيق طلبات.
                </p>
            </div>
        </section>
    </div>

    <!-- CONTACT PAGE -->
    <div id="page-contact" class="page">
        <section>
            <div class="section-title">
                <h2 id="contact-title">التواصل والموقع</h2>
                <p id="contact-subtitle">يسعدنا استقبالكم وزيارتكم في أي وقت</p>
            </div>

            <div class="contact-box">
                <div class="contact-grid">
                    <div class="contact-item"><i class="fa-solid fa-location-dot"></i> <span id="c-loc">العامرات، مسقط</span></div>
                    <div class="contact-item"><i class="fa-solid fa-phone"></i> <span>9290 9050</span></div>
                    <div class="contact-item"><i class="fa-solid fa-clock"></i> <span id="c-time">حتى 12:00 منتصف الليل</span></div>
                    <div class="contact-item"><i class="fa-solid fa-chair"></i> <span id="c-dine">جلسات داخلية متوفرة</span></div>
                    <div class="contact-item"><i class="fa-solid fa-bag-shopping"></i> <span id="c-drive">طلب سفري</span></div>
                    <div class="contact-item"><i class="fa-solid fa-motorcycle"></i> <span id="c-del">التوصيل عبر طلبات</span></div>
                </div>

                <div class="btn-group" style="justify-content: center;">
                    <a class="btn-main" href="tel:92909050" id="c-btn-call"><i class="fa-solid fa-phone"></i> اتصل الآن</a>
                    <a class="btn-sub" href="https://www.google.com/maps/search/?api=1&query=Sadoon+Cookies+Al+Amarat" target="_blank" id="c-btn-map">
                        <i class="fa-solid fa-map-location-dot"></i> الموقع على الخريطة
                    </a>
                </div>
            </div>
        </section>
    </div>

    <!-- Footer -->
    <footer>
        <p>© 2026 <span>سعدون كوكيز</span> - <span id="footer-rights">جميع الحقوق محفوظة</span></p>
    </footer>

    <!-- Script for Page Switch & Language -->
    <script>
        let currentLang = 'ar';

        const translations = {
            ar: {
                logoText: "سعدون كوكيز",
                navHome: "الرئيسية",
                navMenu: "القائمة",
                navReviews: "التقييمات",
                navAbout: "عن الكافيه",
                navContact: "التواصل",
                langBtn: "English",

                heroRating: "4.7 من 70 تقييم",
                heroDesc: "استمتع بتجربة فريدة في العامرات مع أفضل أنواع الكوكيز المخبوز يومياً والمشروبات الخاصة.",
                btnMenu: "استعرض القائمة",
                btnCall: "اتصل بنا",

                infoTitle: "معلومات عن الكافيه",
                infoSubtitle: "تفاصيل الخدمة والموقع لزيارتك القادمة",
                infoRatingLabel: "التقييم",
                infoLocationLabel: "الموقع",
                infoLoc: "العامرات، مسقط",
                infoPriceLabel: "مستوى الأسعار",
                infoHoursLabel: "ساعات العمل",
                infoHours: "مفتوح يومياً حتى 12 منتصف الليل",

                menuTitle: "قائمة المشروبات والكوكيز",
                menuSubtitle: "منيو متنوع يلبي ذوقك من المخبوزات والقهوة",

                reviewsTitle: "آراء الزوار",
                reviewsSubtitle: "انطباعات وتجارب زبائننا الكرام",

                aboutTitle: "عن سعدون كوكيز",
                aboutDesc: "يقدم سعدون كوكيز في العامرات تجربة ممتازة لعشاق الكوكيز الطازج والقهوة. نحرص على تحضير منتجاتنا يومياً باستخدام مكونات عالية الجودة، وتوفير خيارات التناول الداخلي، الطلب السفري، والتوصيل المباشر عبر تطبيق طلبات.",

                contactTitle: "التواصل والموقع",
                contactSubtitle: "يسعدنا استقبالكم وزيارتكم في أي وقت",
                cLoc: "العامرات، مسقط",
                cTime: "حتى 12:00 منتصف الليل",
                cDine: "جلسات داخلية متوفرة",
                cDrive: "طلب سفري",
                cDel: "التوصيل عبر طلبات",
                cBtnCall: "اتصل الآن",
                cBtnMap: "الموقع على الخريطة",
                footerRights: "جميع الحقوق محفوظة"
            },
            en: {
                logoText: "Sadoon Cookies",
                navHome: "Home",
                navMenu: "Menu",
                navReviews: "Reviews",
                navAbout: "About Us",
                navContact: "Contact",
                langBtn: "العربية",

                heroRating: "4.7 from 70 reviews",
                heroDesc: "Enjoy a unique experience in Al Amarat with fresh daily baked cookies and special drinks.",
                btnMenu: "Explore Menu",
                btnCall: "Call Us",

                infoTitle: "Cafe Information",
                infoSubtitle: "Service details and location for your next visit",
                infoRatingLabel: "Rating",
                infoLocationLabel: "Location",
                infoLoc: "Al Amarat, Muscat",
                infoPriceLabel: "Price Level",
                infoHoursLabel: "Opening Hours",
                infoHours: "Open daily until 12:00 AM",

                menuTitle: "Drinks & Cookies Menu",
                menuSubtitle: "A variety of drinks and fresh baked goods for your taste",

                reviewsTitle: "Customer Reviews",
                reviewsSubtitle: "Impressions and feedback from our guests",

                aboutTitle: "About Sadoon Cookies",
                aboutDesc: "Sadoon Cookies in Al Amarat offers a great experience for fresh cookies and coffee lovers. We prepare our products daily with high-quality ingredients, offering dine-in, takeaway, and delivery via Talabat.",

                contactTitle: "Contact & Location",
                contactSubtitle: "We are delighted to welcome your visit anytime",
                cLoc: "Al Amarat, Muscat",
                cTime: "Until 12:00 AM",
                cDine: "Dine-in Available",
                cDrive: "Takeaway",
                cDel: "Delivery via Talabat",
                cBtnCall: "Call Now",
                cBtnMap: "Google Maps Location",
                footerRights: "All rights reserved"
            }
        };

        function showPage(pageId) {
            document.querySelectorAll('.page').forEach(page => page.classList.remove('active-page'));
            document.querySelectorAll('.nav-link').forEach(link => link.classList.remove('active'));

            document.getElementById('page-' + pageId).classList.add('active-page');
            document.getElementById('nav-' + pageId).classList.add('active');
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        function toggleLanguage() {
            currentLang = currentLang === 'ar' ? 'en' : 'ar';
            document.documentElement.dir = currentLang === 'ar' ? 'rtl' : 'ltr';
            document.documentElement.lang = currentLang;

            const t = translations[currentLang];

            document.getElementById('logo-text').innerText = t.logoText;
            document.getElementById('nav-home').innerText = t.navHome;
            document.getElementById('nav-menu').innerText = t.navMenu;
            document.getElementById('nav-reviews').innerText = t.navReviews;
            document.getElementById('nav-about').innerText = t.navAbout;
            document.getElementById('nav-contact').innerText = t.navContact;
            document.getElementById('lang-text').innerText = t.langBtn;

            document.getElementById('hero-rating').innerText = t.heroRating;
            document.getElementById('hero-desc').innerText = t.heroDesc;
            document.getElementById('btn-view-menu').innerHTML = `<i class="fa-solid fa-utensils"></i> ${t.btnMenu}`;
            document.getElementById('btn-call').innerHTML = `<i class="fa-solid fa-phone"></i> ${t.btnCall}`;

            document.getElementById('info-title').innerText = t.infoTitle;
            document.getElementById('info-subtitle').innerText = t.infoSubtitle;
            document.getElementById('info-rating-label').innerText = t.infoRatingLabel;
            document.getElementById('info-location-label').innerText = t.infoLocationLabel;
            document.getElementById('info-loc').innerText = t.infoLoc;
            document.getElementById('info-price-label').innerText = t.infoPriceLabel;
            document.getElementById('info-hours-label').innerText = t.infoHoursLabel;
            document.getElementById('info-hours').innerText = t.infoHours;

            document.getElementById('menu-title').innerText = t.menuTitle;
            document.getElementById('menu-subtitle').innerText = t.menuSubtitle;

            document.getElementById('reviews-title').innerText = t.reviewsTitle;
            document.getElementById('reviews-subtitle').innerText = t.reviewsSubtitle;

            document.getElementById('about-title').innerText = t.aboutTitle;
            document.getElementById('about-desc').innerText = t.aboutDesc;

            document.getElementById('contact-title').innerText = t.contactTitle;
            document.getElementById('contact-subtitle').innerText = t.contactSubtitle;
            document.getElementById('c-loc').innerText = t.cLoc;
            document.getElementById('c-time').innerText = t.cTime;
            document.getElementById('c-dine').innerText = t.cDine;
            document.getElementById('c-drive').innerText = t.cDrive;
            document.getElementById('c-del').innerText = t.cDel;
            document.getElementById('c-btn-call').innerHTML = `<i class="fa-solid fa-phone"></i> ${t.cBtnCall}`;
            document.getElementById('c-btn-map').innerHTML = `<i class="fa-solid fa-map-location-dot"></i> ${t.cBtnMap}`;
            document.getElementById('footer-rights').innerText = t.footerRights;
        }
    </script>
</body>
</html>

var builder = WebApplication.CreateBuilder(args);

// إضافة الخدمات الأساسية للـ Controllers والـ CORS
builder.Services.AddControllers();
builder.Services.AddCors(options =>
{
    options.AddPolicy("AllowAll", policy =>
    {
        policy.AllowAnyOrigin()
              .AllowAnyHeader()
              .AllowAnyMethod();
    });
});

var app = builder.Build();

// تفعيل الملفات الثابتة (لخدمة صفحة HTML والأيقونات والصور)
app.UseDefaultFiles(); // لفتح index.html تلقائياً عند فتح الموقع
app.UseStaticFiles();

app.UseRouting();
app.UseCors("AllowAll");
app.UseAuthorization();

app.MapControllers();

app.Run();
