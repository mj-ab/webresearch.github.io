دلایلی برای عدم تمایل به استفاده از ORM ها وجود دارد که از جمله‌‌‌‌ی آن‌ها می‌توان به پیچیده بودن آن‌ها و داشتن انتزاعی ناقص از داده‌های ذخیره شده به صورت رابطه‌ای، اشاره کرد.پیچیدگی آن‌ها عمدتا به دلیل تعامل نادقیق و ساده‌ی آن‌ها با لایه‌ی پایین‌تر یعنی پایگاه داده‌ی رابطه‌ای باز می‌گردد. مشکل و مساله‌ی اصلی از این ناشی می‌شود که در ORM، هدف ایجاد همگامی بین دو نمایش کاملا متفاوت از داده است. یکی داده‌های داخل پایگاه داده‌ی رابطه‌ای و دیگری داده‌های موجود در حافظه. داده‌ساختارهای داخل حافظه‌ای، انعطاف بییشتری از مدل رابطه‌ای دارند و این مساله باعث رغبت بیشتر برنامه‌نویسان به استفاده از آن‌ها و در نتیجه ناچار بودن آن‌ها به استفاده از نگاشت بین این داده‌ساختارها با مدل داده‌ی رابطه‌ای است. اما این نگاشت به دلایلی همچون تفاوت در نحوه‌ی نمایش و ذخیره‌سازی دادهه، توانایی ایجاد تغییر در هر دو طرف نگاشت و دسترسی افراد برای اعمال تغییر همزمان در پایگاه داده،‌ دارای پیچیدگی‌هایی است. از آنجایی که اگر بخواهیم ORM را به کلی کنار بگذاریم، باید جایگزینی برای آن ارائه دهیم، دو راه حل وجود دارد: یکی تلاش برای حل مشکل و دیگری، پیشگیری از به وجود آمدن مشکل.\\


منتقدان ORM معتقد هستند ابزارهایی مانند \lr{Hibernate} ، ناکارآمد هستند و باید جایگزینی سبک‌‌تر به جای آن‌ها توسط خود آن‌ها ساخته و استفاده شود. ساختن ابزار‌های ORM توسط خود برنامه‌نویسان به جای استفاده از ابزارهای موجود، کاری دشوار و پیچیده است و وقتی عمل پس از مدتی از شروع فرآیند ساخت، شما به عنوان یک برنامه‌نویس احساس می‌کنید در یک باتلاق گیر کرده‌اید. اگرچه ابزارهای متن‌بازی همچون iBatis در از بین بردن مشکل نقش اساسی داشته‌اند، اما استفاده از آن‌ها هم چندان ساده نیست. مشکل اصلی اینجا است که این ابزارها عمدتا می‌توانند ۸۰٪ مشکلات را حل کنند در حالی که انتظارات بیشتری از آن‌ها وجود دارد. برنامه‌نویسان دوست دارند تا به مدل رابطه‌ای داده فکر نکنند و این‌کار را به ابزارهای ORM واگذار کنند. اما ۲۰ ٪ باقی‌مانده را کسی باید کنترل کند. اما همچنان استفاده از ابزار‌هایی که ۸۰٪ مساله را حل می‌کنند ارزشمند است و برای ۲۰ ٪ باقی‌مانده نیاز است تا به خوبی به مدل داده‌ی رابطه‌ای مسلط باشیم و طراحی مدل داده‌ای خود را به مدل رابطه‌ای نزدیک نماییم. نهایتا اگر نرم‌افزار ما سبک است یا مثلا فقط قرار است در آن اطلاعات از روی پایگاه داده خوانده شود می‌توان به نوشتن یک ابزار خودساخت فکر کرد اما در عمده‌ی موارد استفاده از ابزارهای موجود بهتر از وارد شدن به پیچیدگی ساخت ابزار‌های خود ساخت است. و اما روش دوم حل مشکل پیشگیری از به وجود آمدن مشکل است. برای این‌کار دو روش وجود دارد. یا مدل رابطه‌ای را در حافظه‌ استفاده کنیم و یا اینکه به کلی از این مدل در پایگاه داده استفاده نکنیم. روش اول به زبان ساده به این معنا‌ است که مانند ابزار‌های CRUD دهه‌ی ۹۰، به زبان رابطه‌ای برنامه‌نویسی کنیم. اما روش دوم را میتوان در پایگاه داده‌های NoSQL خلاصه کرد. اگر نرم‌افزاری داریم که به خوبی با این مدل کار می‌کند، پس بهتر است تا از دردسرهای نگاشت رابطه‌ای دوری کنیم. اما این روش فقط زمانی کارا است که تناسب بین نرم‌افزار و این مدل واقعا تناسب خوبی باشد در حالی که همه‌ی موارد اینگونه نیستند.
