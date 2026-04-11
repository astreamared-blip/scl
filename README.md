<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SCL | مختبرك المصغر</title>
    <style>
        :root {
            --primary-green: #689f38; /* الأخضر الأساسي من الشعار */
            --dark-green: #33691e;
            --dark-overlay: rgba(0, 0, 0, 0.7); /* طبقة داكنة للشفافية فوق الصور */
            --text-color: #333;
            --white: #ffffff;
            --border-light: rgba(104, 159, 56, 0.3); /* لون الخط الأخضر الضعيف للحدود */
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background-color: var(--white);
            color: var(--text-color);
        }

        /* تنسيق عام للحواشي */
        .container {
            width: 85%;
            margin: 0 auto;
            max-width: 1200px;
        }

        /* الهيدر مع الخط الأخضر الضعيف أسفل الخيارات */
        header {
            background-color: var(--white);
            padding: 20px 0;
            border-bottom: 1px solid var(--border-light); /* خط أخضر نحيف أسفل الخيارات */
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 32px;
            font-weight: bold;
            color: #777;
            letter-spacing: 2px;
        }

        .logo span {
            color: var(--primary-green);
        }

        nav a {
            margin-right: 30px;
            text-decoration: none;
            color: var(--text-color);
            font-weight: 500;
            font-size: 15px;
            transition: 0.3s;
            padding-bottom: 5px;
        }

        nav a:hover {
            color: var(--primary-green);
        }

        /* Hero Section (خلفية العلماء) */
        .hero {
            position: relative;
            text-align: center;
            padding: 150px 0;
            color: var(--white);
            background-image: linear-gradient(var(--dark-overlay), var(--dark-overlay)), 
                              url('https://images.unsplash.com/photo-1576086213369-97a306d36557?q=80&w=2000');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            font-weight: 800;
        }

        .hero p {
            font-size: 1.4rem;
            max-width: 700px;
            margin: 0 auto;
            opacity: 0.9;
        }

        /* --- قسم الرئيسية ومختبراتنا (البطاقات الثلاث) --- */
        .features {
            padding: 80px 0;
            position: relative;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }

        .card {
            background: #fff;
            padding: 40px;
            border-radius: 10px;
            text-align: center;
            transition: 0.3s;
            border: 1px solid #f0f0f0;
        }

        .card:hover {
            box-shadow: 0 10px 20px rgba(0,0,0,0.05);
            transform: translateY(-5px);
        }

        .card h3 {
            color: var(--primary-green);
            margin-bottom: 15px;
            font-size: 1.8rem;
        }

        .card p {
            color: #777;
            line-height: 1.7;
            font-size: 1.1rem;
        }

        /* --- الخط الطويل الأخضر النحيف تحت قسم البطاقات --- */
        .full-width-divider {
            width: 100%;
            height: 1px;
            background-color: var(--border-light); /* خط أخضر نحيف وطويل */
            margin-bottom: 0; /* ليلتصق بقسم CTA */
        }

        /* --- قسم اتخاذ الإجراء / المساعدات (خلفية المعدات) --- */
        /* هذا هو القسم الذي تم إعادة الصورة إليه وإصلاحه */
        .cta-section {
            padding: 100px 0;
            text-align: center;
            color: var(--white);
            /* تم إصلاح الرابط هنا وإعادة تفعيل الخلفية */
            background-image: linear-gradient(rgba(0,0,0,0.8), rgba(0,0,0,0.8)), 
                              url('https://images.unsplash.com/photo-1603126857599-f6e157fa2fe6?q=80&w=2000');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            border-bottom: 1px solid var(--border-light); /* خط أخضر نحيف أسفل القسم */
        }

        .cta-section h2 {
            font-size: 2.5rem;
            margin-bottom: 15px;
        }

        .cta-section p {
            font-size: 1.2rem;
            opacity: 0.9;
            margin-bottom: 30px;
        }

        .cta-button {
            display: inline-block;
            padding: 18px 50px;
            background-color: var(--primary-green);
            color: white;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            font-size: 1.2rem;
            transition: 0.3s;
        }

        .cta-button:hover {
            background-color: var(--dark-green);
            box-shadow: 0 5px 25px rgba(104, 159, 56, 0.4);
        }

        /* فوتر بسيط */
        footer {
            text-align: center;
            padding: 40px;
            background-color: #333;
            color: #aaa;
            font-size: 0.9rem;
        }
    </style>
</head>
<body>

    <header>
        <div class="container header-content">
            <div class="logo">S<span>CL</span></div>
            <nav>
                <a href="#">الرئيسية</a>
                <a href="#">مختبراتنا</a>
                <a href="#">الابتكار</a>
                <a href="#">تواصل معنا</a>
            </nav>
        </div>
    </header>

    <section class="hero">
        <div class="container">
            <h1>مستقبل الكيمياء بين يديك</h1>
            <p>حلول مبتكرة لتجارب علمية احترافية بحقيبة ذكية تجمع بين الدقة، الأمان، وسهولة الاستخدام عالمياً.</p>
        </div>
    </section>

    <section class="features">
        <div class="container features-grid">
            <div class="card">
                <h3>صديق للبيئة</h3>
                <p>تقنيات متطورة ومواد مستدامة لتقليل الهدر الكيميائي والحفاظ على بيئة تعليمية وبحثية نظيفة.</p>
            </div>
            <div class="card">
                <h3>دقة عالمية</h3>
                <p>معدات ومواد كيميائية مطابقة للمقاييس الدولية لضمان نتائج تجارب دقيقة، موثوقة، وآمنة تماماً.</p>
            </div>
            <div class="card">
                <h3>سهولة الاستخدام</h3>
                <p>تصميم محمول وعصري يسمح لك بحمل مختبرك الخاص والبدء في تجاربك بضغطة زر في أي مكان.</p>
            </div>
        </div>
    </section>

    <div class="full-width-divider"></div>

    <section class="cta-section">
        <div class="container">
            <h2>انضم إلى عالم الابتكار مع SCL</h2>
            <p>نحن هنا لمساعدتك في رحلتك العلمية. ابدأ تجربتك الآن.</p>
            <a href="#" class="cta-button">اطلب حقيبتك الآن</a>
        </div>
    </section>

    <footer>
        <p>© 2026 SCL Global | جميع الحقوق محفوظة لشركة المختبر الذكي</p>
    </footer>

</body>
</html>
