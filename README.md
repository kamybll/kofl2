<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>صفحة بيع المنتج</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f9f9f9;
            margin: 0;
            padding: 0;
            direction: rtl;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        header {
            background-color: #2c3e50;
            color: white;
            padding: 20px 0;
            text-align: center;
        }
        .product-section {
            display: flex;
            flex-wrap: wrap;
            margin: 30px 0;
            gap: 30px;
        }
        .product-image {
            flex: 1;
            min-width: 300px;
        }
        .product-image img {
            width: 100%;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        .product-info {
            flex: 1;
            min-width: 300px;
        }
        .product-title {
            color: #2c3e50;
            font-size: 28px;
            margin-top: 0;
        }
        .product-price {
            font-size: 24px;
            color: #e74c3c;
            font-weight: bold;
            margin: 20px 0;
        }
        .product-description {
            margin-bottom: 20px;
        }
        .order-form {
            background-color: white;
            padding: 25px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            margin-top: 30px;
        }
        .form-title {
            margin-top: 0;
            color: #2c3e50;
            text-align: center;
        }
        .form-group {
            margin-bottom: 15px;
        }
        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        input, select, textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 16px;
        }
        button {
            background-color: #27ae60;
            color: white;
            border: none;
            padding: 12px 20px;
            font-size: 18px;
            border-radius: 4px;
            cursor: pointer;
            width: 100%;
            transition: background-color 0.3s;
        }
        button:hover {
            background-color: #2ecc71;
        }
        .features {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin: 30px 0;
        }
        .feature {
            flex: 1;
            min-width: 200px;
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            text-align: center;
        }
        .feature-icon {
            font-size: 40px;
            color: #3498db;
            margin-bottom: 15px;
        }
        footer {
            background-color: #2c3e50;
            color: white;
            text-align: center;
            padding: 20px 0;
            margin-top: 30px;
        }
        /* نافذة الشكر المنبثقة */
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.5);
        }
        .modal-content {
            background-color: white;
            margin: 15% auto;
            padding: 30px;
            border-radius: 8px;
            width: 80%;
            max-width: 500px;
            text-align: center;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
            position: relative;
        }
        .close {
            position: absolute;
            top: 10px;
            left: 10px;
            font-size: 24px;
            cursor: pointer;
        }
        @media (max-width: 768px) {
            .product-section {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>مرحبا بكم</h1>
            <h1>حيث الجودة تفوق السعر</h1>
        </div>
    </header>

    <div class="container">
        <section class="product-section">
<div class="product-image">
    <!-- الصورة الرئيسية -->
    <img src="https://i.imgur.com/IpMCgKy.jpeg" alt="قفل الثلاجة" id="mainProductImage" style="width:100%; border-radius:8px;">
    
    <!-- معرض الصور المصغرة -->
    <div class="product-gallery">
        <img src="https://i.imgur.com/Tuksumq.jpeg" onclick="changeMainImage(this.src, 'الوصف 1')">
        <img src="https://i.imgur.com/DpkM1md.jpeg" onclick="changeMainImage(this.src, 'الوصف 2')">
        <img src="https://i.imgur.com/MaQgbxt.png" onclick="changeMainImage(this.src, 'الوصف 3')">
    </div>
</div>

<style>
.product-gallery {
    display: flex;
    gap: 10px;
    margin-top: 15px;
    flex-wrap: wrap;
}
.product-gallery img {
    width: 80px;
    height: 80px;
    object-fit: cover;
    cursor: pointer;
    border: 2px solid #ddd;
    border-radius: 4px;
    transition: all 0.3s ease;
}
.product-gallery img:hover {
    border-color: #27ae60;
    transform: scale(1.05);
}
</style>

<script>
function changeMainImage(imgSrc, altText) {
    document.getElementById('mainProductImage').src = imgSrc;
    document.getElementById('mainProductImage').alt = altText;
}
</script>
            <div class="product-info">
                <h2 class="product-title">قفل الثلاجة</h2>
<div class="product-info">
    <h2 class="product-title">احمِ محتويات ثلاجتك بذكاء وسهولة</h2>
    
    <div class="product-price-container">
        <div class="original-price">السعر الأصلي: 1600 دج</div>
        <div class="discounted-price">السعر الخاص: <h2>1150 دج</h2></div>
        <div class="discount-badge">زوج بـ 1800 دج + هدية</div>
        <div class="countdown-timer"> <h2 id="countdown"></h2></div>
    </div>
    
    <div class="product-description">
        <p>هل تعاني من عبث الأطفال بثلاجتك؟ أو تخشى أن يُترك الباب مفتوحًا، مما يؤدي إلى تلف الأطعمة وزيادة فاتورة الكهرباء؟ قفل الثلاجة الذكي هو الحل الأمثل الذي يضمن لك سلامة أطفالك، وحماية محتويات ثلاجتك، وتوفير الطاقة بكل سهولة!.</p>
        <p> مصمم خصيصًا ليلائم جميع أنواع الثلاجات، هذا القفل يتميز بمتانة عالية وسهولة في التركيب، مما يجعله اختيارًا مثاليًا للعائلات والأماكن التجارية مثل المطاعم والفنادق.</p>
    </div>
</div>

        <section class="features">
            <div class="feature">
                <div class="feature-icon">✓</div>
                <h3>ميزة 1</h3>
                <p>حماية مضمونة للأطفال 👶

يمنع الصغار من فتح الثلاجة دون إذن، مما يحميهم من العبث بالأطعمة أو تناول أشياء قد تكون خطرة مثل الأدوية أو المواد الحادة.</p>
            </div>
            <div class="feature">
                <div class="feature-icon">✓</div>
                <h3>ميزة 2</h3>
                <p>تصميم قوي وسهل التركيب 🛠️

مصنوع من بلاستيك متين ومقاوم للكسر، مع آلية غلق قوية تتحمل الاستخدام اليومي. يمكنك تركيبه في دقائق بدون حفر أو تعقيدات!</p>
            </div>
            <div class="feature">
                <div class="feature-icon">✓</div>
                <h3>ميزة 3</h3>
                <p>إغلاق محكم يوفر الطاقة ويحافظ على الطعام ❄️

يضمن إغلاق الثلاجة بإحكام، مما يمنع تسرب الهواء البارد ويحافظ على برودة الأطعمة لفترة أطول، كما يقلل من استهلاك الكهرباء!</p>
            </div>
        </section>

<form id="orderForm">
    <div class="form-group">
        <label for="name">الاسم الكامل:</label>
        <input type="text" id="name" name="name" required>
    </div>
    <div class="form-group">
        <label for="phone">رقم الهاتف:</label>
        <input type="tel" id="phone" name="phone" required>
    </div>
    <div class="form-group">
        <label for="wilaya">الولاية:</label>
        <select id="wilaya" name="wilaya" required>
            <option value="">اختر ولايتك</option>
            <option value="أدرار">أدرار</option>
                        <option value="الشلف">الشلف</option>
                        <option value="الأغواط">الأغواط</option>
                        <option value="أم البواقي">أم البواقي</option>
                        <option value="باتنة">باتنة</option>
                        <option value="بجاية">بجاية</option>
                        <option value="بسكرة">بسكرة</option>
                        <option value="بشار">بشار</option>
                        <option value="البليدة">البليدة</option>
                        <option value="البويرة">البويرة</option>
                        <option value="تمنراست">تمنراست</option>
                        <option value="تبسة">تبسة</option>
                        <option value="تلمسان">تلمسان</option>
                        <option value="تيارت">تيارت</option>
                        <option value="تيزي وزو">تيزي وزو</option>
                        <option value="الجزائر">الجزائر</option>
                        <option value="الجلفة">الجلفة</option>
                        <option value="جيجل">جيجل</option>
                        <option value="سطيف">سطيف</option>
                        <option value="سعيدة">سعيدة</option>
                        <option value="سكيكدة">سكيكدة</option>
                        <option value="سيدي بلعباس">سيدي بلعباس</option>
                        <option value="عنابة">عنابة</option>
                        <option value="قالمة">قالمة</option>
                        <option value="قسنطينة">قسنطينة</option>
                        <option value="المدية">المدية</option>
                        <option value="مستغانم">مستغانم</option>
                        <option value="المسيلة">المسيلة</option>
                        <option value="معسكر">معسكر</option>
                        <option value="ورقلة">ورقلة</option>
                        <option value="وهران">وهران</option>
                        <option value="البيض">البيض</option>
                        <option value="إيليزي">إيليزي</option>
                        <option value="برج بوعريريج">برج بوعريريج</option>
                        <option value="بومرداس">بومرداس</option>
                        <option value="الطارف">الطارف</option>
                        <option value="تندوف">تندوف</option>
                        <option value="تيسمسيلت">تيسمسيلت</option>
                        <option value="الوادي">الوادي</option>
                        <option value="خنشلة">خنشلة</option>
                        <option value="سوق أهراس">سوق أهراس</option>
                        <option value="تيبازة">تيبازة</option>
                        <option value="ميلة">ميلة</option>
                        <option value="عين الدفلى">عين الدفلى</option>
                        <option value="النعامة">النعامة</option>
                        <option value="عين تموشنت">عين تموشنت</option>
                        <option value="غرداية">غرداية</option>
                        <option value="غليزان">غليزان</option>
 </select>
    </div>
    <div class="form-group">
        <label for="quantity">الكمية المطلوبة:</label>
        <input type="number" id="quantity" name="quantity" min="1" value="1" required>
    </div>
    <button type="submit">إرسال الطلب</button>
</form>
        </section>
    </div>

    <footer>
        <div class="container">
            <p>جميع الحقوق محفوظة &copy; 2023</p>
        </div>
    </footer>

    <!-- نافذة الشكر المنبثقة -->
    <div id="thankYouModal" class="modal">
        <div class="modal-content">
            <span class="close">&times;</span>
            <h2>شكرًا لك!</h2>
            <p>تم استلام طلبك بنجاح وسنتصل بك قريبًا لتأكيد التفاصيل.</p>
            <p>رقم الطلب: <span id="orderNumber"></span></p>
        </div>
    </div>

   <script>
    // إرسال النموذج إلى التلغرام
    const form = document.getElementById('orderForm');
    const modal = document.getElementById('thankYouModal');
    const closeBtn = document.querySelector('.close');
    const orderNumberSpan = document.getElementById('orderNumber');

    form.addEventListener('submit', async function(e) {
        e.preventDefault();
        
        // إنشاء رقم طلب عشوائي
        const orderNumber = 'ORD-' + Math.floor(Math.random() * 1000000);
        orderNumberSpan.textContent = orderNumber;
        
        // جمع بيانات النموذج
        const formData = new FormData(form);
        let message = `🛒 *طلب جديد* 🛒\n\n`;
        
        // إضافة البيانات إلى الرسالة بشكل منظم
        message += `📛 *الاسم:* ${formData.get('name')}\n`;
        message += `📞 *الهاتف:* ${formData.get('phone')}\n`;
        message += `📍 *الولاية:* ${formData.get('wilaya')}\n`;
        message += `🏠 *العنوان:* ${formData.get('address')}\n`;
        message += `🔢 *الكمية:* ${formData.get('quantity')}\n`;
        
        message += `\n🆔 *رقم الطلب:* ${orderNumber}`;
        
        // إرسال البيانات إلى بوت التلغرام
        const telegramBotToken = '8167868166:AAGyh5czzDzt_cZuSt-osSQXA_oKoi9hhCQ';
        const chatId = '@kofltalaja'; // استبدل هذا بقناة التلغرام أو المحادثة
        const telegramUrl = `https://api.telegram.org/bot${telegramBotToken}/sendMessage`;
        
        try {
            const response = await fetch(telegramUrl, {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify({
                    chat_id: chatId,
                    text: message,
                    parse_mode: 'Markdown' // لجعل النص منسقاً
                })
            });
            
            const data = await response.json();
            
            if(data.ok) {
                console.log('تم الإرسال إلى التلغرام بنجاح:', data);
                modal.style.display = 'block';
                form.reset();
            } else {
                console.error('فشل الإرسال إلى التلغرام:', data);
                alert('حدث خطأ أثناء إرسال الطلب. يرجى المحاولة مرة أخرى.');
            }
        } catch (error) {
            console.error('حدث خطأ:', error);
            alert('حدث خطأ في الاتصال. يرجى التحقق من اتصال الإنترنت والمحاولة مرة أخرى.');
        }
    });
    
    // إغلاق النافذة المنبثقة
    closeBtn.addEventListener('click', function() {
        modal.style.display = 'none';
    });
    
    window.addEventListener('click', function(e) {
        if (e.target === modal) {
            modal.style.display = 'none';
        }
    });
</script>
  
