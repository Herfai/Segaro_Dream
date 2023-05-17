# ضرورت اصلاح مدل اقتصادی 
ببینید دوستان ، مدل اقتصادی v2ray اشتباهه ، چون منفعت vpn ساز نادیده گرفته شده . کانفیگ رایگانی که میسازیم تغییر نام داده میشه و توسط سودجوها فروخته میشه. از طرف دیگر ، پرداخت نقدی مشکلاتی نظیر افشای هویت vpn ساز داره ، همچنین ممکنه vpn ساز بعد از دریافت پول ، کانفیگ را قطع کنه یا فیلتر بشه و خریدار متضرر بشه.

این معایب باعث شده تا همه سرور شخصی بسازند ، و این باعث اتلاف وقت و هزینه بسیاری از مردم شده چرا که ایپی سرورها مسدود میشود ،  تمام ظرفیت سرور  زیر بار نمیرود و ...

# راه حل چیست:
اصلاح مدل اقتصادی v2ray
وقتی پاول دروف ایده پراکسی تلگرام را میداد ،  با نبوغی که داشت ، تبلیغات را برای تامین منفعت پراکسی ساز در پروتکل mtproto گنجاند. این باعث شد که میلیون ها پراکسی توسط خود مردم ساخته و پخش شود و اکنون تلگرام تنها پلتفرمی است که در مقابل شدیدترین فیلترینگ سر پا است. 

# ایده ما چیست:
کپی از پاول دروف + مکانیزم پایش کانفیگ

پس ما باید اپ v2ray را اصلاح کنیم بنحوی که vpn ساز بتواند روی اپ تبلیغ داشته باشد (تبلیغ در حد متعارف مثلا یک نوتیف نه بیشتر)

# چه مزایایی دارد:
۱. اولا منفعت vpn ساز تامین میشود و انگیزه دارد تا کانفیگ های متعدد بسازد
۲. افراد بی بضاعت بدون هزینه میتوانند از v2ray  استفاده کنند
۳. کلاینت v2ray  کانفیگ چرخشی خواهد داشت یعنی همیشه تعدادی کانفیگ فعال در لیست خواهد داشت.
۴.کلاینت ها میتوانند سالم یا معیوب بودن کانفیگ را به IRCF گزارش کنند و IRCF با پایش آنها ، بطور اتوماتیک برای هر شهر و اپراتور کانفیگ های سالم را دسته بندی و به کلاینت ها بدهد.

این مکانیزم ، سیستم فیلترینگ را به زانو در خواهد آورد. همانطوری که تلگرام چنین کرد و البته در تلگرام انتخاب پراکسی دستی است اما در سیستم ما با کمک IRCF پایش و ارسال کانفیگ هم اتوماتیک خواهد شد.

# چه معایبی دارد : 
کارکرد این سیستم ، نیازمند ساختن ده ها هزار کانفیگ در روز است و این تنها زمانی میسر میشود که vpn سازها انگیزه کافی داشته باشند یعنی بتوانند تبلیغ کنند. 
محتوای تبلیغ چندان قابل کنترل نخواهد بود و مشابه پراکسی های تلگرام ، تبلیغ هر چیزی از کانال مستهجن تا سایت قمار ممکن است بصورت نوتیف روی گوشی کاربر برود. شاید بتوان چند کلمه کلیدی را فیلتر کرد یا به کاربر هشدار داد که کانفیگ حاوی تبلیغ است.


.....................
کدنویسی این پروژه چندان سنگین نیست ولی بخاطر بکارگیری ایده پاول دروف در تامین منفعت vpn ساز و رایگان شدن v2ray برای مردم ، تاثیر بزرگی خواهد گذاشت و به اعتقاد بنده حداقل ۲۰ میلیون نفر را به نت آزاد متصل و GFW را کاملا بی اثر خواهد ساخت.

...................
ممکن است بپرسید اگر GFW تمام کانفیگ ها را فیلتر کند چه ؟
پاسخ: مگر پروکسی های تلگرام را فیلتر نمیکند؟ و ما دستمان در v2ray بازتر است. با تکنولوژی کلودفلر و سایر CDN ها ، یک سرور میتواند با میلیون ها ایپی کار کند و کانفیگ های متعدد به راحتی توسط vpn ساز ساخته و به شبکه تزریق شود. همچنین با تکنولوژی فرگمنت ، با دامنه فیلتر شده هم کانفیگ کار میکند (حداقل تا امروز). با داشتن تکنولوژی ریلیتی و انواع دیگر پروتکل ها دستمان بمراتب از mtproto بازتر خواهد بود.