# 📈 پیش‌بینی جهت حرکت قیمت بیت‌کوین با الگوریتم‌های یادگیری ماشین

در این پروژه با استفاده از الگوریتم‌های کلاسیک یادگیری ماشین، سعی شده تا **جهت حرکت قیمت بیت‌کوین (صعود یا نزول)** در روز آینده پیش‌بینی شود. این مدل‌سازی بر اساس ویژگی‌هایی استخراج‌شده از قیمت‌های گذشته انجام می‌گیرد و می‌تواند به عنوان یک ابزار کمکی در تصمیم‌گیری‌های سرمایه‌گذاری و تحلیل بازارهای مالی مورد استفاده قرار گیرد.

---

## 💡 هدف پروژه

هدف اصلی این پروژه، تحلیل و پیش‌بینی حرکت قیمتی بیت‌کوین با استفاده از داده‌های تاریخی آن و الگوریتم‌های یادگیری ماشین است. به‌جای پیش‌بینی دقیق مقدار قیمت، این مدل تنها پیش‌بینی می‌کند که آیا قیمت روز آینده **افزایش** خواهد یافت یا **کاهش** خواهد یافت.

---

## 🎯 کاربردهای این پروژه

1. **تحلیل بازار رمزارزها**:
   - کمک به تحلیل‌گران برای درک روندهای احتمالی آینده بازار.
   - ابزار تصمیم‌سازی در کنار تحلیل تکنیکال.

2. **معاملات الگوریتمی (Algorithmic Trading)**:
   - استفاده به عنوان بخشی از استراتژی خرید و فروش خودکار رمزارزها.

3. **آموزش و پژوهش**:
   - نمونه‌ای کاربردی برای آموزش یادگیری ماشین در زمینه مالی.
   - پروژه‌ای تحقیقاتی برای تحلیل تأثیر ویژگی‌های مختلف در پیش‌بینی روند قیمتی.

4. **ارزیابی مدل‌ها در داده‌های مالی**:
   - بررسی عملکرد مدل‌هایی مثل Logistic Regression، Decision Tree، و KNN در داده‌های واقعی و نویزی بازار رمزارزها.

---

## 📊 مراحل انجام پروژه

1. **بارگذاری داده‌ها**: داده‌ها از فایل `bitcoin.csv` بارگذاری می‌شوند. این داده شامل قیمت باز، بسته، بیشینه، کمینه و سایر اطلاعات مربوط به بیت‌کوین است.

2. **تحلیل اولیه داده‌ها (EDA)**:
   - بررسی ویژگی‌های آماری، نوع داده‌ها و نمودارهای اولیه برای درک بهتر داده.

3. **ایجاد ویژگی‌های جدید (Feature Engineering)**:
   - ویژگی `open-close`: تفاوت بین قیمت باز و بسته.
   - ویژگی `low-high`: تفاوت بین بیشترین و کمترین قیمت روز.
   - ویژگی `is_quarter_end`: بررسی اینکه آیا روز مربوطه پایان سه‌ماهه است یا خیر.

4. **تعریف برچسب هدف (Target)**:
   - اگر قیمت بسته شدن روز آینده از امروز بیشتر باشد → برچسب ۱ (افزایش)
   - در غیر این صورت → برچسب ۰ (کاهش)

5. **پیش‌پردازش و نرمال‌سازی داده‌ها**:
   - استانداردسازی ویژگی‌ها با استفاده از `StandardScaler`.

6. **تقسیم داده‌ها به آموزش و تست**:
   - با استفاده از `train_test_split`، داده‌ها به نسبت 85/15 برای آموزش و اعتبارسنجی تقسیم می‌شوند.

7. **آموزش مدل‌ها**:
   - سه مدل اصلی روی داده‌ها آموزش می‌بینند:
     - Logistic Regression
     - Decision Tree Classifier
     - K-Nearest Neighbors (KNN)

8. **ارزیابی عملکرد مدل‌ها**:
   - دقت مدل‌ها با معیار **ROC AUC Score** بررسی می‌شود تا کارایی مدل‌ها در پیش‌بینی دقیق برچسب‌ها ارزیابی گردد.

---

## 🧪 نتایج اولیه

| مدل                     | دقت آموزش (AUC) | دقت اعتبارسنجی (AUC) |
|-------------------------|------------------|------------------------|
| Logistic Regression     | 0.85 (مثال)      | 0.82 (مثال)            |
| Decision Tree Classifier| 0.93 (مثال)      | 0.74 (مثال)            |
| KNN                     | 0.81 (مثال)      | 0.78 (مثال)            |

> 🔎 توجه: این نتایج بسته به داده‌ها و اجرای مجدد ممکن است کمی متفاوت باشد.

---

## ⚙️ نحوه اجرا

1. کلون کردن مخزن:
   ```bash
   git clone https://github.com/username/bitcoin-price-prediction.git
   cd bitcoin-price-prediction


   📚 پیش‌نیازها
Python 3.8+

Jupyter Notebook


✅ پیشنهاد برای توسعه‌های آتی


استفاده از الگوریتم‌های پیشرفته مانند:

Random Forest

XGBoost

Support Vector Machines

بهبود انتخاب ویژگی‌ها با استفاده از تکنیک‌هایی مانند SelectKBest یا PCA.

پیاده‌سازی مدل‌های مبتنی بر سری‌های زمانی (مانند LSTM).

ارزیابی مدل‌ها با معیارهایی مانند F1-score و Confusion Matrix.

📜 مجوز
این پروژه تحت مجوز MIT منتشر می‌شود. استفاده آزاد است به شرط درج منبع و احترام به حقوق نویسنده.

✨ نویسنده
نام: Mahboubeh

- 📧 ایمیل: [niayeshmirshekar92@gmail.com](mailto:niayeshmirshekar92@gmail.com)
- 💼 لینکدین: [Mahboubeh Mirshekar](https://www.linkedin.com/in/mahbubeh-mirshekar-999640170)
- اینستاگرام: airobo.project
  کانال تلگرام:airobo_project

---

<p align="center">
  🌟 اگر به همکاری روی پروژه‌های هوش مصنوعی علاقه‌مند هستی، خوشحال می‌شم در ارتباط باشیم!
</p>
