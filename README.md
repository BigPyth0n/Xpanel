# Xpanel
تمامی تجربیات با این پنل رو در زیر بروزرسانی میکنم
آخرین نصب پنل ورژن v3.9.6 میباشد
1 - یک سرور مجازی ترکیه با ای پی تمیز درست کردم با اوبنتو 20.4 و آپدیت و اپگرید کردم
apt update && apt upgrade -y

2 - سپس با دستور زیر پنل رو نصب کردم
bash <(curl -Ls https://raw.githubusercontent.com/xpanel-cp/XPanel-SSH-User-Management/master/install.sh --ipv4)
نکته : لازم به ذکر است برای ارتباط بهتر سرور و پنل و بقیه موارد تمامی پروت های خواسته شده در تمامی مراحل نصب و از پورت های کلود فلر استفاده کردم

3 - سپس یک زیر دامنه در کلود فلر ایجاد کردم تا بتونم با دستور زیر گواهی دامنه رو هم ایجاد کنم
bash <(curl -Ls https://raw.githubusercontent.com/xpanel-cp/XPanel-SSH-User-Management/master/install.sh --ipv4)

4 - سپس با دستور xpanel در ترمینال لینوکس و انتخاب گزینه آخر یعنی نصب  Sing-box شروع به نصب هسته در سرور کردم بعد از دانلود خطا نشون میده که سینگ باکس نصب نیست و ما گزینه 1 رو میزنیم تا نصب بشه بعد از بین گزینه های مربوط به سرتیفیکیت گزینه 1 یا همون self-singned  رو انتخاب میکنیم و در این مرحله که مربوط به انتخاب پورت ها هست گزینه 3 رو انتخاب میکنیم تا برای تک تک موارد بصورت دستی شروع کنیم به تعیین پورت ها البته لازم به ذکر است بهتره پورتهای کلود فلر رو انتخاب کنیم که در مراحل قبل ازشون استفاده نکردیم
2052
2053
2082
2083
2086
2087
2095
2096
8880
8443
حالا دیگه در این سرور کاری نداریم و بر میگردیم به رابط کاربری و از گزینه کاربران>SING-BOX>افزودن کاربر رو میزنیم و از پروتکل ها گزینه Tuic رو انتخاب میکنیم و یک یوزر جدید میسازیم.

5 - برای استفاده از این کانفیگ در ویندوز من از NekoRay استفاده کردم و کانفیگ کپی شده رو توی لیست پیست کردم ولی قبل از اجرا از تب Performance , Basic Setting و تب Core گزینه sign-box رو انتخاب کردم و اوکی کردم و در صفحه اول هر دو گزینه tun mode و system proxy رو تیک زدم و روی کانفیگ اینتر کردم تا انتخاب و شروع به رد کردن پروکسی بکنه.

6 - برای استفاده از این کانفیگ Tuic در اندروید نرم افزار hiddify ایرانی بهتر عمل کرد دانلود و نصب کردم و کانفیگ رو اسکن و استارت زدم.

نکته : در کلود فلر پروکسی رو نیر فعال کردم و ssl رو هم روی full گذاشتم

خطا برای نصب نشدن php8.1 از رپوزیتوری خودم برای بروزرسانی مخازن و اضافه کردن مخزن نصب php8.1 کمک گرفتم و برای دوتا خطای نصب نشدن دیگه این دستورات رو هم میتونم بصورت دستی قبل از نصب xpanel اضافه کنم:

sudo apt install -y npm

sudo apt install -y nethogs

برای رفع خطای hostbame:
==> hostname
مثلا این نام رو برگردوند
y5eqrty7.vm

sudo nano /etc/hosts
بعد این خطوط رو به این فایل اضافه میکینم
127.0.0.1   localhost
127.0.1.1   fv123wqh.vm

برای اطمینان آخر سر هم این دستور رو میزنیم البته با اون نام دامنه ای که سیستم بهم داده
==> sudo hostnamectl set-hostname y5eqrty7.vm





