<!DOCTYPE html>
<html lang="fa">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>کافینت آنلاین همیار</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: #f4f7f9;
      margin: 0;
      color: #333;
      direction: rtl;
    }
    header {
      background: #005f73;
      padding: 20px;
      text-align: center;
      color: white;
    }
    nav {
      background: #0a9396;
      display: flex;
      justify-content: center;
      gap: 30px;
      padding: 15px 0;
    }
    nav a {
      color: white;
      text-decoration: none;
      font-weight: bold;
      font-size: 18px;
    }
    nav a:hover {
      text-decoration: underline;
    }
    .container {
      max-width: 900px;
      margin: 30px auto;
      padding: 0 15px;
      background: white;
      border-radius: 8px;
      box-shadow: 0 0 12px rgba(0,0,0,0.1);
    }
    h1, h2 {
      color: #0a9396;
    }
    ul.services-list {
      list-style-type: square;
      padding-right: 20px;
    }
    form {
      display: flex;
      flex-direction: column;
      gap: 15px;
    }
    input, textarea {
      padding: 10px;
      border-radius: 5px;
      border: 1px solid #ccc;
      font-size: 16px;
      resize: vertical;
    }
    button {
      background-color: #005f73;
      color: white;
      padding: 12px;
      font-size: 18px;
      border: none;
      border-radius: 6px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
    button:hover {
      background-color: #0a9396;
    }
    footer {
      background: #005f73;
      color: white;
      text-align: center;
      padding: 15px 10px;
      margin-top: 40px;
    }
    .contact-info {
      font-size: 18px;
    }
  </style>
</head>
<body>
  <header>
    <h1>کافینت آنلاین همیار</h1>
    <p>خدمات آنلاین ثبت‌نام و امور دانشجویی و معلمین</p>
  </header>

  <nav>
    <a href="#home" onclick="showPage('home')">خانه</a>
    <a href="#services" onclick="showPage('services')">خدمات</a>
    <a href="#request" onclick="showPage('request')">ثبت درخواست</a>
    <a href="#contact" onclick="showPage('contact')">تماس با ما</a>
  </nav>

  <div class="container">
    <section id="home" class="page">
      <h2>به کافینت آنلاین همیار خوش آمدید</h2>
      <p>ارائه بهترین خدمات آنلاین شامل ثبت‌نام‌های اینترنتی، انجام تکالیف و مشاوره‌های آموزشی و مالی.</p>
    </section>

    <section id="services" class="page" style="display:none;">
      <h2>خدمات ما</h2>
      <ul class="services-list">
        <li>انجام کلیه ثبت نام های اینترنتی</li>
        <li>انجام دوره های ضمن خدمت برای معلمین</li>
        <li>ثبت نام سهام عدالت</li>
        <li>ثبت نام وام ازدواج و وام فرزندآوری</li>
        <li>ثبت گاز مایع برای خانوار</li>
        <li>انجام امور دانش آموزی و دانشجویی</li>
        <li>انجام آزمون های نهاد</li>
        <li>تکالیف دانشجویی</li>
        <li>ثبت نام کنکور و آزمون استخدامی</li>
      </ul>
    </section>

    <section id="request" class="page" style="display:none;">
      <h2>ثبت درخواست</h2>
      <form id="requestForm">
        <input type="text" name="name" placeholder="نام و نام خانوادگی" required />
        <input type="email" name="email" placeholder="ایمیل" required />
        <textarea name="request" rows="5" placeholder="درخواست خود را وارد کنید" required></textarea>
        <button type="submit">ارسال درخواست</button>
      </form>
      <p style="margin-top: 15px; color: #555;">
        در صورت عدم پاسخگویی، لطفاً در واتساپ پیام دهید به شماره:  
        <a href="https://wa.me/09157330757" target="_blank" style="color:#0a9396; font-weight:bold;">۰۹۱۵۷۳۳۰۷۵۷</a>
      </p>
      <p id="responseMessage" style="color: green; font-weight: bold;"></p>
    </section>

    <section id="contact" class="page" style="display:none;">
      <h2>تماس با ما</h2>
      <p class="contact-info">
        شماره واتساپ: <a href="https://wa.me/09157330757" target="_blank" style="color:#0a9396;">۰۹۱۵۷۳۳۰۷۵۷</a><br />
        ایمیل: info@hamyarcafinet.ir<br />
        آدرس: تهران، خیابان انقلاب، پلاک ۱۲۳
      </p>
    </section>
  </div>

  <footer>
    <p>© 2025 کافینت آنلاین همیار. همه حقوق محفوظ است.</p>
  </footer>

  <script>
    function showPage(pageId) {
      const pages = document.querySelectorAll('.page');
      pages.forEach(page => {
        page.style.display = page.id === pageId ? 'block' : 'none';
      });
    }
    // نمایش صفحه خانه به صورت پیش فرض
    showPage('home');

    // ارسال فرم ثبت درخواست (در اینجا فقط نمایش پیام تشکر)
    document.getElementById('requestForm').addEventListener('submit', function(e) {
      e.preventDefault();
      // در حالت واقعی باید اینجا درخواست به سرور ارسال شود
      document.getElementById('responseMessage').textContent = 'درخواست شما با موفقیت ارسال شد. به زودی با شما تماس می‌گیریم.';
      this.reset();
    });
  </script>
</body>
</html>
