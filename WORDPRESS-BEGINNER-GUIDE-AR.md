# دليل تحويل Bagdad Reisgids إلى WordPress من الصفر

هذا الدليل موجه لشخص لم يستخدم WordPress من قبل. النتيجة المطلوبة هي موقع هولندي ديناميكي مطابق لنموذج **Bagdad Reisgids**: صفحة رئيسية، أرشيف الأماكن، صفحة لكل مكان، أرشيف التصنيفات وصفحة لكل تصنيف، صفحة Over/Praktisch، Privacy، Cookies، نتائج البحث، 404، Header وFooter.

## قبل البداية: الأدوات المستخدمة

المسار الأسهل للمبتدئ هو:

1. **LocalWP** لتشغيل WordPress على جهازك بدون شراء استضافة.
2. **WordPress** لإدارة المحتوى.
3. قالب **Hello Elementor**.
4. إضافة **Elementor** المجانية.
5. **Elementor Pro** لبناء Header وFooter والقوالب الديناميكية و404 والبحث.
6. **Advanced Custom Fields Pro (ACF Pro)** لإنشاء أنواع المحتوى والحقول وحقول Gallery وRelationship.

Elementor Pro وACF Pro إضافتان مدفوعتان. لا تحمّل نسخاً مقرصنة. البديل المجاني هو قالب WordPress مبرمج خصيصاً للمشروع؛ يحتاج ملفات PHP/CSS/JS جاهزة بدلاً من خطوات السحب والإفلات.

## 1. تثبيت LocalWP على Windows

1. افتح `https://localwp.com/`.
2. اضغط **Download for free** واختر **Windows**.
3. افتح ملف التثبيت الذي نزل إلى مجلد Downloads.
4. اختر التثبيت للمستخدم الحالي إذا سُئلت، ثم اضغط **Next > Install**.
5. افتح برنامج **Local**.
6. إذا ظهرت رسائل Windows Firewall عند إنشاء الموقع، اضغط **Allow access** حتى تعمل خدمات الويب وقاعدة البيانات.

## 2. إنشاء موقع WordPress محلي

1. داخل Local اضغط زر **+** أسفل الجهة اليسرى، أو **Create a new site** في وسط الشاشة.
2. اختر **Create a new site** ثم **Continue**.
3. في **Site name** اكتب: `Bagdad Reisgids`.
4. افتح **Advanced options** وتأكد أن الدومين المقترح قريب من `bagdad-reisgids.local`.
5. اضغط **Continue**.
6. اختر **Preferred** للبيئة، ثم **Continue**.
7. في **WordPress username** اكتب اسماً تحفظه، مثل `adminbagdad`.
8. اكتب كلمة مرور قوية واحفظها في مكان آمن.
9. في **WordPress email** اكتب بريدك الحقيقي.
10. اترك خيار Multisite على **No**، ثم اضغط **Add Site**.
11. انتظر حتى ينتهي الإنشاء. من شاشة الموقع في Local اضغط **Start site** إذا كان الموقع متوقفاً.
12. اضغط **WP Admin**. سيفتح رابط شبيه بـ `http://bagdad-reisgids.local/wp-admin/`.
13. سجل الدخول باسم المستخدم وكلمة المرور اللذين أنشأتهما.

زر **Open site** في Local يفتح واجهة الزائر، وزر **WP Admin** يفتح لوحة التحكم.

## 3. الإعدادات الأساسية في WordPress

توجد القائمة الرئيسية في العمود الأيسر من لوحة WordPress.

### 3.1 إعدادات الموقع

1. من اليسار افتح **Settings > General**.
2. اجعل **Site Title**: `Bagdad Reisgids`.
3. اجعل **Tagline**: `Ontdek Bagdad aan de Tigris`.
4. اجعل **Site Language**: `English (United States)` لتطابق أسماء القوائم في هذا الدليل. محتوى الموقع نفسه يبقى هولندياً.
5. اختر المنطقة الزمنية **Baghdad** أو `UTC+3`.
6. اضغط **Save Changes** في أسفل الصفحة.

### 3.2 الروابط الدائمة

1. افتح **Settings > Permalinks**.
2. اختر **Post name**.
3. اضغط **Save Changes** حتى لو كان الخيار محدداً مسبقاً.

### 3.3 الصفحة الرئيسية

سننشئ الصفحات أولاً، ثم نعود إلى **Settings > Reading** لاختيار الصفحة الرئيسية.

## 4. تثبيت القالب والإضافات

### 4.1 قالب Hello Elementor

1. من اليسار افتح **Appearance > Themes**.
2. اضغط **Add New Theme** أعلى الصفحة.
3. اكتب `Hello Elementor` في مربع البحث أعلى اليمين.
4. على بطاقة القالب اضغط **Install** ثم **Activate**.

### 4.2 Elementor المجاني

1. افتح **Plugins > Add New Plugin**.
2. اكتب `Elementor Website Builder` في البحث أعلى اليمين.
3. اضغط **Install Now** ثم **Activate**.
4. يمكنك تخطي معالج إعداد Elementor؛ سنضبط التصميم يدوياً.

### 4.3 Elementor Pro

1. اشترِ Elementor Pro من الموقع الرسمي ونزّل ملف ZIP.
2. داخل WordPress افتح **Plugins > Add New Plugin**.
3. اضغط **Upload Plugin** أعلى الصفحة.
4. اضغط **Choose File** واختر ملف Elementor Pro ZIP.
5. اضغط **Install Now** ثم **Activate Plugin**.
6. افتح **Plugins > Installed Plugins** وابحث عن Elementor Pro، ثم اضغط **Connect & Activate** واربط الرخصة.

يجب أن تبقى إضافتا **Elementor** و**Elementor Pro** مفعّلتين معاً.

### 4.4 ACF Pro

1. نزّل ملف ACF Pro ZIP من حسابك الرسمي.
2. افتح **Plugins > Add New Plugin > Upload Plugin**.
3. اختر ملف ZIP، ثم **Install Now > Activate Plugin**.
4. سيظهر عنصر **ACF** في القائمة اليسرى.

## 5. إنشاء Content Model

أنشئ الأنواع بهذا الترتيب: Destination، Place، Review، ثم Taxonomy باسم Place Category.

### 5.1 نوع المحتوى Destination

1. افتح **ACF > Post Types** من اليسار.
2. اضغط **Add New Post Type**.
3. اكتب:
   - **Plural Label:** `Destinations`
   - **Singular Label:** `Destination`
   - **Post Type Key:** `destination`
4. شغّل **Advanced Configuration**.
5. ضمن **Supports** فعّل: Title، Editor، Featured Image.
6. ضمن **URLs** فعّل **Archive**.
7. تأكد أن **Public** و**Show in UI** و**Show in REST API** مفعلة.
8. اضغط **Save Changes** أعلى اليمين.

### 5.2 نوع المحتوى Place

كرر الخطوات واستخدم:

- **Plural Label:** `Places`
- **Singular Label:** `Place`
- **Post Type Key:** `place`
- **Archive:** مفعّل
- **Supports:** Title، Editor، Excerpt، Featured Image
- **Show in REST API:** مفعّل

### 5.3 نوع المحتوى Review

كرر الخطوات واستخدم:

- **Plural Label:** `Reviews`
- **Singular Label:** `Review`
- **Post Type Key:** `review`
- **Archive:** غير مطلوب
- **Supports:** Title فقط
- **Public:** يمكن إبقاؤه مفعلاً أثناء المشروع، أو تعطيل **Publicly Queryable** إذا لن تكون لكل Review صفحة مستقلة.

### 5.4 تصنيف Place Category

1. افتح **ACF > Taxonomies**.
2. اضغط **Add New Taxonomy**.
3. اكتب:
   - **Plural Label:** `Place Categories`
   - **Singular Label:** `Place Category`
   - **Taxonomy Key:** `place_category`
4. عند **Post Types** اختر `Place`.
5. فعّل **Hierarchical** حتى يعمل مثل Categories.
6. فعّل **Public** و**Show in REST API** و**Archive** إن ظهر الخيار.
7. اضغط **Save Changes**.

## 6. إنشاء حقول ACF

كل مجموعة تُنشأ من **ACF > Field Groups > Add New**. بعد إضافة الحقول، انزل إلى قسم **Location Rules** أسفل الشاشة لتحديد مكان ظهور المجموعة، ثم اضغط **Save Changes**.

استخدم أسماء الحقول الإنجليزية كما هي. لا تغيّر **Field Name** بعد إدخال المحتوى.

### 6.1 مجموعة Destination Fields

اسم المجموعة: `Destination Fields`

أنشئ الحقول التالية بزر **+ Add Field**:

| Field Label | Field Name | Field Type |
|---|---|---|
| Description | `description` | Text Area |
| Hero Image | `hero_image` | Image |
| Getting There | `getting_there` | Text Area |
| Getting Around | `getting_around` | Text Area |
| Best Time to Visit | `best_time_to_visit` | Text Area |
| Language & Currency | `language_currency` | Text Area |
| Accommodation | `accommodation` | Text Area |
| Health & Safety | `health_safety` | Text Area |
| Address / Region | `address_region` | Text |
| Latitude | `latitude` | Text |
| Longitude | `longitude` | Text |
| Official Tourism Website | `official_tourism_website` | URL |
| Tourist Information Office | `tourist_information_office` | Text Area |
| Emergency Contacts | `emergency_contacts` | Text Area |
| Featured Places | `featured_places` | Relationship |

في حقل **Featured Places** اجعل **Filter by Post Type = Place**، وحدد Maximum Posts = 3.

Location Rule:

`Post Type` **is equal to** `Destination`.

### 6.2 مجموعة Place Fields

اسم المجموعة: `Place Fields`

| Field Label | Field Name | Field Type |
|---|---|---|
| Description | `description` | Text Area |
| Main Image | `main_image` | Image |
| Gallery | `gallery` | Gallery |
| Opening Hours | `opening_hours` | Text |
| Entry Fee | `entry_fee` | Text |
| Accessibility | `accessibility` | Text Area |
| Address | `address` | Text |
| Related Places | `related_places` | Relationship |

في **Related Places** اجعل Filter by Post Type = Place. اختر Return Format المناسب لـElementor، ويفضل **Post Object**.

Location Rule:

`Post Type` **is equal to** `Place`.

لا تنشئ حقلاً منفصلاً لـCategory داخل هذه المجموعة. استخدم **Place Category** من العمود الأيمن في محرر Place حتى تكون العلاقة Taxonomy حقيقية.

### 6.3 مجموعة Review Fields

اسم المجموعة: `Review Fields`

| Field Label | Field Name | Field Type |
|---|---|---|
| Visitor Name | `visitor_name` | Text |
| Rating | `rating` | Number |
| Comment | `comment` | Text Area |
| Review Date | `review_date` | Date Picker |
| Place | `place` | Post Object |

إعداد Rating: Minimum = 1، Maximum = 5، Step = 1.

إعداد Place: Filter by Post Type = Place، Multiple = No.

Location Rule:

`Post Type` **is equal to** `Review`.

### 6.4 مجموعة حقول التصنيف

اسم المجموعة: `Place Category Fields`

| Field Label | Field Name | Field Type |
|---|---|---|
| Image | `category_image` | Image |
| Icon | `category_icon` | Select |

خيارات Icon:

```text
landmark : Landmark
museum : Museum
architecture : Architecture
tree : Park / Nature
```

Location Rule:

`Taxonomy Term` **is equal to** `Place Category`.

## 7. رفع الصور مع Metadata

الصور موجودة في مجلد المشروع:

`bagdad-reisgids/dist/assets/`

1. افتح **Media > Add New Media File**.
2. اسحب الصور التسع إلى منطقة الرفع.
3. افتح **Media > Library**.
4. اضغط أول صورة. تظهر نافذة التفاصيل، وحقول البيانات تكون عادة في الجهة اليمنى.
5. املأ **Alternative Text** بالنص الموجود في `content.json` أو Part 2.
6. املأ **Caption**.
7. أضف اسم المصور وحقوق CC BY-SA 4.0 ورابط المصدر داخل **Description**.
8. كرر ذلك لكل صورة.

لا تحذف اسم المصور أو رابط المصدر؛ هذه المعلومات جزء من Media Asset في Part 1 وPart 2.

## 8. إدخال التصنيفات الأربعة

1. افتح **Places > Place Categories** من القائمة اليسرى.
2. توجد حقول الإضافة في الجهة اليسرى، وقائمة التصنيفات في الجهة اليمنى.
3. أضف التصنيفات واحداً واحداً:

| Name | Slug | Image | Icon |
|---|---|---|---|
| Geschiedenis en erfgoed | `geschiedenis-en-erfgoed` | Media 02 | landmark |
| Musea en cultuur | `musea-en-cultuur` | Media 05 | museum |
| Religie en architectuur | `religie-en-architectuur` | Media 07 | architecture |
| Parken en rivierleven | `parken-en-rivierleven` | Media 06 | tree |

انسخ Description لكل تصنيف من `dist/content.json`، واختر Image وIcon، ثم اضغط **Add New Place Category**.

## 9. إدخال الأماكن الثمانية

1. افتح **Places > Add New Place**.
2. اكتب الاسم في أعلى المحرر.
3. من إعدادات العنصر في الجهة اليمنى افتح **Summary** وعدّل Slug عند الحاجة.
4. الصق الوصف في حقل Description.
5. اختر Main Image وGallery.
6. أدخل Opening Hours وEntry Fee وAccessibility وAddress.
7. من مربع **Place Categories** في الجهة اليمنى اختر التصنيف أو التصنيفين الصحيحين.
8. اختر Related Places.
9. استخدم الصورة نفسها أيضاً كـ **Featured Image** إذا احتاجتها بطاقات Elementor.
10. اضغط **Publish** أعلى اليمين، ثم أكد **Publish** مرة ثانية.

أدخل الأماكن بهذا الترتيب:

| Place | Slug | Category |
|---|---|---|
| Al Mustansiriya Madrasa | `al-mustansiriya-madrasa` | Geschiedenis en erfgoed + Religie en architectuur |
| Al Mutanabbi straat | `al-mutanabbi-straat` | Musea en cultuur |
| Al Qishla | `al-qishla` | Geschiedenis en erfgoed |
| Het Bagdadmuseum | `bagdadmuseum` | Musea en cultuur |
| Al Zawraa Park | `al-zawraa-park` | Parken en rivierleven |
| Al Kadhimiya moskee | `al-kadhimiya-moskee` | Religie en architectuur |
| Het Iraaks Museum | `iraaks-museum` | Musea en cultuur |
| Het Abbasidisch Paleis | `abbasidisch-paleis` | Geschiedenis en erfgoed + Religie en architectuur |

انسخ بقية القيم حرفياً من `dist/content.json`. لا تضف أسعاراً أو مواعيد أو حقائق غير موجودة في الملف.

## 10. إدخال Destination وReviews

### Destination

1. افتح **Destinations > Add New Destination**.
2. العنوان: `Bagdad`، والـSlug: `bagdad`.
3. أدخل جميع القيم من `dist/content.json`.
4. في **Featured Places** اختر:
   - Al Mustansiriya Madrasa
   - Al Mutanabbi straat
   - Het Iraaks Museum
5. اضغط **Publish**.

### Reviews

1. افتح **Reviews > Add New Review**.
2. استخدم عنواناً إدارياً مثل `Review – Noor A. – Al Mustansiriya Madrasa`.
3. أدخل Visitor Name وRating وComment وReview Date.
4. اختر Place الصحيح.
5. اضغط **Publish**.
6. كرر الإجراء للـReviews الأربعة الموجودة في `dist/content.json`.

هذه Reviews اختبارية من الملف وليست آراء زوار حقيقية؛ حافظ على توضيح ذلك في الواجهة.

## 11. إنشاء الصفحات الثابتة

من **Pages > Add New Page** أنشئ الصفحات التالية. اكتب العنوان، اضبط Slug من الشريط الجانبي الأيمن، ثم اضغط Publish:

| Title | Slug |
|---|---|
| Home | `home` |
| Plaatsen | `plaatsen` |
| Categorieën | `categorieen` |
| Over Bagdad | `over-bagdad` |
| Praktisch | `praktisch` |
| Privacyverklaring | `privacy` |
| Cookiebeleid | `cookies` |

بعد إنشاء Home:

1. افتح **Settings > Reading**.
2. عند **Your homepage displays** اختر **A static page**.
3. اختر `Home` في قائمة Homepage.
4. اضغط **Save Changes**.

## 12. إعداد تصميم الموقع العام

افتح صفحة Home واضغط **Edit with Elementor**. من أعلى محرر Elementor اضغط شعار Elementor ثم **Site Settings**.

### الألوان العالمية

استخدم:

- Primary dark teal: `#0F3B4D`
- Dark green: `#083C32`
- Gold: `#C9A96A`
- Warm ivory: `#EFE7D6`
- Page background: `#F8F6F2`
- Brown accent: `#8C6F47`
- Main text: `#1E2927`

### الخطوط

- Headings: `Playfair Display`
- Body: `Inter`

### القياسات

- Content Width: `1200px`
- Desktop section padding: أعلى وأسفل 80px، يمين ويسار 32px.
- Tablet: 48px و24px.
- Mobile: 36px و18px.
- Border radius للبطاقات: 12px.
- الصور: Object Fit = Cover.

اضغط **Save Changes**.

## 13. إنشاء Header

1. ارجع إلى لوحة التحكم.
2. افتح **Elementor > Theme Builder**.
3. في بطاقة **Header** اضغط علامة **+** في الجهة اليمنى.
4. أغلق مكتبة القوالب إذا أردت البدء من الصفر.
5. أضف Container أفقي يحتوي:
   - Site Logo أو Heading مكتوب فيه `Bagdad` في اليسار.
   - Menu في الوسط/اليمين.
   - Search icon في أقصى اليمين.
6. اجعل الخلفية `#083C32` أو شفافة فوق الـHero، والنص أبيض.
7. اجعل الشعار Playfair Display والروابط Inter.
8. من إعدادات الـContainer اجعل **Position = Sticky** وTop = 0، وZ-index = 100.
9. راجع وضع Mobile من أيقونة Responsive أعلى المحرر، واستخدم قائمة Hamburger.
10. اضغط **Publish > Add Condition > Include > Entire Site > Save & Close**.

## 14. إنشاء قائمة التنقل

لأن Hello Elementor قالب كلاسيكي/هجين، استخدم غالباً:

1. **Appearance > Menus**.
2. اضغط **Create a new menu**.
3. اسم القائمة: `Hoofdmenu`.
4. أضف بالترتيب:
   - Home
   - Categorieën
   - Plaatsen
   - Praktisch
   - Over Bagdad
5. اسحب العناصر أعلى أو أسفل لترتيبها.
6. فعّل موضع **Primary Menu** إذا ظهر.
7. اضغط **Save Menu**.

إذا لم يظهر **Appearance > Menus** استخدم **Appearance > Editor > Navigation**، أو اختر القائمة مباشرة داخل Widget الـMenu في Header.

## 15. إنشاء Footer

1. افتح **Elementor > Theme Builder**.
2. عند **Footer** اضغط **+**.
3. أنشئ Footer بخلفية `#083C32` ونص فاتح.
4. العمود الأول: Bagdad Reisgids ووصف قصير من المحتوى الموجود.
5. العمود الثاني: Home، Plaatsen، Categorieën، Over Bagdad.
6. العمود الثالث: Praktisch، Privacyverklaring، Cookiebeleid، Beeldcredits إذا أنشأتها.
7. أضف سطراً لحقوق الصور وروابط المصادر.
8. اضغط **Publish > Include > Entire Site**.

## 16. تصميم Home

افتح **Pages > Home > Edit with Elementor** وابنِ الأقسام بهذا الترتيب:

1. **Hero**: صورة Media 01 كخلفية كاملة العرض، Overlay داكن، العنوان `Bagdad aan de Tigris`، النص الموجود في Part 2، وزر `Bekijk alle plaatsen`.
2. **Categorieën**: عنوان `Kies wat je wilt ontdekken` وأربع بطاقات مقوّسة. اربط كل بطاقة بأرشيف Place Category المناسب.
3. **Over Bagdad**: قسم نصفه صورة ونصفه خلفية خضراء داكنة، عنوان `Een stad met vele lagen` وزر إلى Over Bagdad.
4. **Featured Places**: Loop Grid يعرض ثلاثة أماكن. الأفضل استخدام Query يدوي يختار Featured Places الثلاثة، أو اختيارها بالاسم.
5. **Praktisch CTA**: `Stel een haalbare dagroute samen` وزر إلى Praktisch.
6. **Newsletter mockup**: ضع النموذج كعرض تجريبي فقط، واكتب أنه لا يرسل ولا يحفظ بيانات إلى أن يتم إعداد البريد والخصوصية فعلياً.

لكل زر: من تبويب Content اختر الرابط الداخلي، ثم من Style طبّق اللون الذهبي والحواف المستديرة.

## 17. قالب صفحة Place الواحدة

1. افتح **Elementor > Theme Builder**.
2. عند **Single Post** اضغط **+**.
3. اختر النوع `Single Post` وسمّ القالب `Single Place`.
4. من إعدادات Preview اختر Post Type = Place ثم اختر Al Mustansiriya Madrasa لتشاهد بيانات حقيقية أثناء التصميم.
5. أضف Post Title وPost Terms.
6. أضف Image widget. بجانب اختيار الصورة اضغط أيقونة **Dynamic Tags**، ثم **ACF Image Field** واختر `main_image`.
7. أضف Text Editor، Dynamic Tags > ACF Field > `description`.
8. أنشئ صندوق المعلومات الجانبي وأضف حقول opening_hours وentry_fee وaccessibility وaddress بالطريقة نفسها.
9. أضف Gallery مرتبطة بحقل `gallery`. إذا لم يظهر Gallery كـDynamic Tag، استخدم ACF shortcode أو Gallery widget بمحتوى الصفحة، أو اطلب مني تجهيز Shortcode صغير لهذا الحقل.
10. أضف Related Places باستخدام Loop Grid/Posts Query مرتبطاً بالعلاقة. هذه النقطة قد تحتاج Query ID وكوداً صغيراً لأن Elementor لا يعرض كل حقول Relationship مباشرة.
11. أضف قسم Reviews. ربط Reviews بالـPlace الحالي يحتاج Query مخصصاً؛ أسهل حل عملي أن أجهز لك الكود القصير بعد بناء القالب.
12. اضغط **Publish > Add Condition > Include > Places > All**.

## 18. قالب أرشيف Places والتصنيفات

1. افتح **Elementor > Theme Builder > Archive > +**.
2. سمّه `Places Archive`.
3. أضف Archive Title ووصفاً قصيراً وLoop Grid.
4. صمم Loop Item يحتوي Featured Image، Post Terms، Post Title، Excerpt وزر `Bekijk plaats`.
5. اضغط **Publish > Include > Places Archive**.
6. أنشئ Archive آخر باسم `Place Category Archive`.
7. استخدم Archive Title وArchive Description وLoop Grid نفسه.
8. طبّق Condition على **Place Category Archives**.

للفلترة حسب التصنيف والبحث داخل Places كما في النموذج، ستحتاج FacetWP أو Search & Filter Pro أو كود JavaScript/PHP مخصص. لا تثبّت إضافة عشوائية قبل التأكد من متطلبات Part 3.

## 19. صفحات Over/Praktisch وPrivacy وCookies

1. افتح كل صفحة واضغط **Edit with Elementor**.
2. انسخ النص الهولندي حرفياً من Part 2 أو `dist/content.json`.
3. في Praktisch استخدم Accordion لعناوين Vervoer، Klimaat، Taal en geld، Kleding، Veiligheid، Gezondheid.
4. في Privacy وCookies ضع النصوص الموردة ولا تدّع استخدام Analytics أو Marketing cookies إذا لم يتم تركيبها فعلياً.
5. أضف روابط Privacy وCookies في Footer.

## 20. Search وNo Results و404

### Search Results

1. افتح **Elementor > Theme Builder > Search Results** إذا ظهر كنوع مستقل، أو أنشئ Archive Template.
2. أضف Search Form وArchive Title وLoop Grid.
3. أضف رسالة No Results: `Geen resultaten gevonden` مع زر إلى Places.
4. طبّق Condition على Search Results.

### 404

1. افتح **Elementor > Theme Builder > 404 Page > +**.
2. أضف الرقم `404`، والنص `Deze pagina bestaat niet`.
3. أضف زرين: `Terug naar home` و`Bekijk alle plaatsen`.
4. اضغط Publish. قالب 404 لا يحتاج عادة Condition إضافياً.

## 21. Responsive

داخل Elementor استخدم أيقونة Responsive أعلى المحرر وانتقل بين Desktop وTablet وMobile.

افحص في كل صفحة:

- لا يوجد تمرير أفقي.
- عنوان Hero لا يخرج خارج الشاشة.
- البطاقات: 3 أعمدة Desktop، عمودان Tablet، عمود واحد Mobile.
- القائمة تتحول إلى Hamburger في Mobile.
- الأزرار لا تتلاصق.
- حجم النص الأساسي 16px على الأقل.
- الصور لا تتمدد أو تنضغط؛ استخدم Object Fit = Cover.
- الـAlt Text موجود لكل صورة.

## 22. الاختبار النهائي

1. افتح الموقع من زر **Open Site** في Local.
2. جرّب جميع عناصر القائمة.
3. افتح الأماكن الثمانية والتصنيفات الأربعة.
4. جرّب البحث بكلمة موجودة وكلمة غير موجودة.
5. افتح رابطاً خاطئاً مثل `/abc123` للتأكد من 404.
6. افحص Privacy وCookies وFooter.
7. افتح أدوات المطور في المتصفح بـF12 واختر حجم هاتف، ثم Tablet.
8. افتح **Settings > Permalinks** واضغط Save Changes مرة أخرى إذا ظهرت 404 في صفحات Place.
9. لا تفعّل نموذج Review حقيقياً قبل إعداد الحماية من Spam وسياسة الخصوصية والتخزين.

## 23. نقل الموقع من Local إلى الإنترنت

بعد إكمال الاختبار تحتاج استضافة WordPress ودومين. GitHub Pages لا يشغّل WordPress/PHP؛ الرابط الحالي مناسب للنموذج Static فقط.

الطريقة الأسهل:

1. اشترِ استضافة تدعم WordPress وSSL وقاعدة MySQL.
2. ثبّت إضافة نقل موثوقة مثل **All-in-One WP Migration** أو استخدم أداة النقل التي توفرها شركة الاستضافة.
3. صدّر الموقع من Local.
4. أنشئ WordPress فارغاً على الاستضافة واستورد النسخة.
5. افتح **Settings > General** وتأكد أن WordPress Address وSite Address يستخدمان الدومين الحقيقي مع HTTPS.
6. افتح **Settings > Permalinks** واضغط Save Changes.
7. من Elementor افتح **Elementor > Tools > Replace URL** عند الحاجة لاستبدال رابط `.local` بالدومين الحقيقي.
8. امسح Cache وافحص الصفحات والنماذج والصور.

## 24. قائمة التسليم المطابقة للمشروع

- Destination واحد: Bagdad.
- 4 Place Categories.
- 8 Places.
- 4 Reviews اختبارية.
- 9 Media Assets مع Alt text وCaption وPhotographer وSource URL وLicense.
- Home.
- Places archive وSingle Place.
- Categories overview وTaxonomy archive.
- Over Bagdad وPraktisch.
- Privacy وCookies.
- Search وNo Results.
- 404.
- Header وFooter.
- Responsive على Desktop وTablet وMobile.
- عدم اختراع محتوى خارج Part 1 وPart 2 وPart 3.

## مراجع الواجهات الرسمية

- LocalWP: https://localwp.com/help-docs/getting-started/installing-local/
- WordPress Pages: https://wordpress.org/documentation/article/create-pages/
- WordPress Menus: https://wordpress.org/documentation/article/appearance-menus-screen/
- ACF Post Types: https://www.advancedcustomfields.com/resources/registering-a-custom-post-type/
- ACF Post Types and Taxonomies: https://www.advancedcustomfields.com/resources/post-types-and-taxonomies/
- ACF Taxonomy Fields: https://www.advancedcustomfields.com/resources/adding-fields-taxonomy-term/
- Elementor installation: https://elementor.com/help/get-started-with-the-elementor-plugin/
- Elementor Pro installation: https://elementor.com/help/installing-elementor-pro/
- Elementor Header: https://elementor.com/help/header-site-part/
- Elementor ACF integration: https://elementor.com/help/elementor-acf/
- Elementor Single template: https://elementor.com/help/single-post-site-part/
- Elementor Archive template: https://elementor.com/help/create-archive-template/

