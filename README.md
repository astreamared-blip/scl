<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SCL | جهاز التفاعلات الكيميائية الآلي</title>
    <style>
        :root {
            --primary-green: #689f38; /* الأخضر الأساسي المطابق للشعار */
            --dark-green: #35581c;
            --gray-color: #777777; /* اللون الرمادي لحرف الـ S */
            --light-bg: #f8faf7;
            --dark-overlay: rgba(0, 0, 0, 0.75);
            --text-color: #2c3e50;
            --text-muted: #5a6c7d;
            --white: #ffffff;
            --border-light: rgba(104, 159, 56, 0.2);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--white);
            color: var(--text-color);
            line-height: 1.7;
        }

        .container {
            width: 88%;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* --- Header --- */
        header {
            background-color: var(--white);
            padding: 20px 0;
            border-bottom: 1px solid var(--border-light);
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.02);
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 32px;
            font-weight: 800;
            color: var(--gray-color); /* حرف S رمادي */
            letter-spacing: 2px;
        }

        .logo span {
            color: var(--primary-green); /* حروف CL خضراء */
        }

        nav a {
            margin-right: 25px;
            text-decoration: none;
            color: var(--text-color);
            font-weight: 600;
            font-size: 0.95rem;
            transition: 0.3s;
        }

        nav a:hover {
            color: var(--primary-green);
        }

        /* --- Hero Section --- */
        .hero {
            position: relative;
            text-align: center;
            padding: 140px 0;
            color: var(--white);
            background-image: linear-gradient(var(--dark-overlay), var(--dark-overlay)), 
                              url('https://images.unsplash.com/photo-1532187863486-abf9dbad1b69?q=80&w=2000');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
        }

        .hero h1 {
            font-size: 3.2rem;
            margin-bottom: 20px;
            font-weight: 800;
        }

        .hero p {
            font-size: 1.3rem;
            max-width: 780px;
            margin: 0 auto;
            opacity: 0.95;
            font-weight: 300;
        }

        /* --- Showcase / Device Section --- */
        .device-intro {
            padding: 90px 0;
            background-color: var(--light-bg);
            border-bottom: 1px solid var(--border-light);
        }

        .grid-2 {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .device-text h2 {
            font-size: 2.3rem;
            color: var(--dark-green);
            margin-bottom: 20px;
        }

        .device-text p {
            color: var(--text-muted);
            font-size: 1.15rem;
            margin-bottom: 20px;
        }

        .device-img img {
            width: 100%;
            height: 380px;
            object-fit: cover;
            border-radius: 12px;
            box-shadow: 0 15px 35px rgba(0,0,0,0.08);
            border: 1px solid var(--border-light);
        }

        /* --- Features Section --- */
        .features {
            padding: 90px 0;
        }

        .section-title {
            text-align: center;
            font-size: 2.2rem;
            color: var(--dark-green);
            margin-bottom: 50px;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 35px;
        }

        .card {
            background: #fff;
            padding: 35px 30px;
            border-radius: 10px;
            text-align: center;
            transition: 0.3s;
            border: 1px solid #eef2eb;
            box-shadow: 0 5px 15px rgba(0,0,0,0.02);
        }

        .card:hover {
            box-shadow: 0 12px 25px rgba(104, 159, 56, 0.08);
            transform: translateY(-5px);
            border-color: var(--border-light);
        }

        .card h3 {
            color: var(--primary-green);
            margin-bottom: 15px;
            font-size: 1.6rem;
        }

        .card p {
            color: var(--text-muted);
            line-height: 1.7;
            font-size: 1.05rem;
        }

        .full-width-divider {
            width: 100%;
            height: 1px;
            background-color: var(--border-light);
        }

        /* --- CTA Section --- */
        .cta-section {
            padding: 100px 0;
            text-align: center;
            color: var(--white);
            background-image: linear-gradient(rgba(0,0,0,0.8), rgba(0,0,0,0.8)), 
                              url('https://images.unsplash.com/photo-1579154204601-01588f351e67?q=80&w=2000');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            border-bottom: 1px solid var(--border-light);
        }

        .cta-section h2 {
            font-size: 2.4rem;
            margin-bottom: 15px;
        }

        .cta-section p {
            font-size: 1.2rem;
            opacity: 0.9;
            margin-bottom: 25px;
        }

        .email-box {
            display: inline-block;
            background-color: rgba(255, 255, 255, 0.12);
            padding: 15px 35px;
            border-radius: 8px;
            border: 1px solid rgba(255, 255, 255, 0.25);
            margin-top: 10px;
            backdrop-filter: blur(5px);
        }

        .email-box a {
            color: #ffffff;
            font-weight: bold;
            font-size: 1.2rem;
            text-decoration: none;
            letter-spacing: 0.5px;
            transition: 0.3s;
        }

        .email-box a:hover {
            color: #d1e7c4;
        }

        /* --- Footer --- */
        footer {
            text-align: center;
            padding: 35px;
            background-color: #222c20;
            color: #a3b899;
            font-size: 0.9rem;
        }

        footer a {
            color: #d1e7c4;
            text-decoration: none;
        }

        @media (max-width: 768px) {
            .grid-2 {
                grid-template-columns: 1fr;
            }
            .hero h1 {
                font-size: 2.2rem;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="container header-content">
            <div class="logo">S<span>CL</span></div>
            <nav>
                <a href="#">الرئيسية</a>
                <a href="#about">عن SCL</a>
                <a href="#features">المميزات</a>
                <a href="#contact">تواصل معنا</a>
            </nav>
        </div>
    </header>

    <section class="hero">
        <div class="container">
            <h1>أتمتة التفاعلات الكيميائية الذكية</h1>
            <p>منصة جهاز SCL لإجراء وتطوير التجارب العلمية والكيميائية تلقائياً بدقة موثوقة وأمان تام.</p>
        </div>
    </section>

    <section id="about" class="device-intro">
        <div class="container grid-2">
            <div class="device-text">
                <h2>ما هو جهاز SCL؟</h2>
                <p>نظام ذكي ومحمول مصمم لإجراء التفاعلات الكيميائية المؤتمتة بدون الحاجة للتدخل المباشر. يقوم الجهاز بضبط المقادير، ومراقبة حرارة ومعايير التفاعل تلقائياً لضمان أعلى درجات السلامة والدقة البحثية.</p>
                <p>يمثل SCL حلولاً آمنة للمختبرات والمؤسسات التعليمية لتقليل المخاطر البشرية والحد من الهدر الكيميائي.</p>
            </div>
            <div class="device-img">
                <img src="https://images.unsplash.com/photo-1581093588401-fbb62a02f120?q=80&w=1000" alt="SCL Chemistry Automation">
            </div>
        </div>
    </section>

    <section id="features" class="features">
        <div class="container">
            <h2 class="section-title">خصائص وتقنيات جهاز SCL</h2>
            <div class="features-grid">
                <div class="card">
                    <h3>أتمتة كاملة للتجربة</h3>
                    <p>برمجة التفاعلات وإجراؤها أوتوماتيكياً وتسجيل القراءات بدقة متناهية دون تعرض الباحث للمواد الخطرة.</p>
                </div>
                <div class="card">
                    <h3>صديق للبيئة</h3>
                    <p>تقنيات تقليل الهدر واستخدام الكميات الميكرونية المستهدفة للحفاظ على بيئة بحثية نظيفة وآمنة.</p>
                </div>
                <div class="card">
                    <h3>دقة معيارية عالية</h3>
                    <p>معدات ومستشعرات مطابقة للمقاييس العلمية الدولية لضمان نتائج تجارب موثوقة وقابلة للتكرار.</p>
                </div>
            </div>
        </div>
    </section>

    <div class="full-width-divider"></div>

    <section id="contact" class="cta-section">
        <div class="container">
            <h2>التواصل والاستفسارات الأكاديمية</h2>
            <p>للمزيد من المعلومات أو للاستفسار عن تقنيات وأبحاث جهاز SCL يسعدنا تواصلكم عبر البريد الإلكتروني:</p>
            <div class="email-box">
                <a href="mailto:astreamared@gmail.com">astreamared@gmail.com</a>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>© 2026 SCL Global | جميع الحقوق محفوظة لـ SCL</p>
            <p style="margin-top: 5px;"><a href="mailto:astreamared@gmail.com">astreamared@gmail.com</a></p>
        </div>
    </footer>

</body>
</html>
