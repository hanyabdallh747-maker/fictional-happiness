# ZERO TO ONE — موقع تسجيل الإيفنت (YLY · Season 8)

موقع تسجيل إيفنت **Zero to One** — 1 ديسمبر 2026، كرياتيفا طنطا.
نسخة **ستاتيك** جاهزة لـ GitHub Pages: التسجيل يروح لردود Google Form مباشرة (من غير سيرفر).

---

## 1) ارفعه على GitHub (3 خطوات)

**خطوة 1 — اعمل الريبو**
1. افتح <https://github.com/new>
2. اسم الريبو (مثلاً `zero-to-one`)، اختر **Public**، دوس **Create repository**.

**خطوة 2 — ارفع الملفات**
1. في صفحة الريبو دوس **Add file → Upload files**.
2. فك ضغط الـ zip ده، و**اسحب كل اللي جوه المجلد** (الملفات دي):
   ```
   index.html
   assets/logo.jpg
   css/styles.css
   js/app.js
   js/config.js
   ```
3. ⚠️ **مهم:** `index.html` لازم يبقى في **جذر الريبو** (مش جوه فولدر)، وإلا الـ Pages مش هيلاقيه.
4. دوس **Commit changes**.

**خطوة 3 — شغّل GitHub Pages**
1. من الريبو: **Settings → Pages** (من القايمة الجانبية).
2. **Source**: اختار **Deploy from a branch** → الفرع **main** → الفرع الفرعي **/ (root)** → **Save**.
3. استنى دقيقة-دقيقتين، وافتح:
   ```
   https://<اسم-حسابك-على-جيت-هاب>.github.io/zero-to-one/
   ```

---

## 2) أو حوّله لموقع على Google Sites (أسرع، من غير رفع)

1. افتح <https://sites.google.com> → اعمل موقع جديد.
2. **Insert → Embed → Embed URL**، وحط الرابط:
   ```
   https://i26pc81skqnto.space.mcode.io/
   ```
3. من **⋯ (الثلاث نقاط)** → **Full width** عشان ياخد عرض الصفحة، والخلاص دوس **Publish**.

> ملاحظة: في Google Sites الموقع بيتحط جوّه `iframe`، فبيشتغل بس لو الـ embed طلع صغير، فعّل **Full width**.
> لو مش عايز الـ iframe، حط زرار **View site** في صفحة الموقع بيوصله الناس على طول.

---

## 3) تعديل بيانات الإيفنت

كله في ملف واحد: **`js/config.js`**

```js
eventNameDisplay: 'ZERO TO ONE',   // اسم الإيفنت على الموقع
dateISO: '2026-12-01',             // تاريخ الإيفنت (بيتلفّ لوحده)
dateLabel: '1 ديسمبر 2026',
location: 'كرياتيفا طنطا',         // المكان
org: 'YLY — Youth Leading Youth · Season 8',
logo: 'assets/logo.jpg',           // الشعار
```

- **تغيير الشعار:** حط صورتك في `assets/` وحدّد مسارها في `logo`.
- **تغيير حقل في الفورم:** عدّل `FORM_SCHEMA` في نفس الملف — الواجهة بس بتتحدث.
- كل المسارات **نسبية**، فالموقع بيشتغل في أي فولدر فرعي من غير ما تلمس حاجة.

---

## 4) التسجيل بيوصل فين؟

كل التسجيلات بتروح لردود **Google Form** بتاع الإيفنت (مش لأي حد تاني).
للتصدير: في الفورم → تبويب **Responses → Link → Create Google Sheet**.
النسخة دي ما فيهاش لوحة تحكم ولا سيرفر — لو محتاج لوحة تحكم وتصدير Excel مباشرة، شوف نسخة `HTC-Node.zip` (بتشتغل على استضافة بتشغّل Node).

---

## 5) الملفات

```
.
├── index.html          # صفحة التسجيل
├── assets/logo.jpg     # شعار YLY
├── css/styles.css      # التصميم (عربي RTL)
├── js/app.js           # منطق النموذج + الإرسال
├── js/config.js        # بيانات الإيفنت + ربط حقول الفورم
└── .nojekyll           # عشان Jekyll ما يتدخلش
```
