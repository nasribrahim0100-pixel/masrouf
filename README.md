# المصروف — تطبيق أندرويد

## الطريقة 1: من غير ما تسطّب حاجة (GitHub بيبني الـ APK)
1. اعمل حساب على github.com لو مش عندك.
2. اعمل Repository جديد (New repository) — سمّيه مثلًا masrouf.
3. ارفع كل محتويات الفولدر ده (Add file ← Upload files).
   - مهم: فولدر `.github` لازم يترفع. لو الموقع ما رفعوش، اعمل ملف جديد
     باسم `.github/workflows/build-apk.yml` وانسخ فيه محتوى الملف.
4. ادخل على تبويب **Actions** — هتلاقي "Build APK" شغال (حوالي 5 دقايق).
   لو مش شغال: اختار Build APK ← Run workflow.
5. لما يخلص (✔ أخضر)، افتحه وانزل لتحت عند **Artifacts** ونزّل `Masrouf-APK`.
6. فك الضغط هتلاقي `Masrouf.apk` — ابعته للموبايل وسطّبه.

## الطريقة 2: Android Studio
1. سطّب Node.js و Android Studio.
2. افتح Terminal في الفولدر ده واكتب:
   ```
   npm install
   npx cap sync android
   npx cap open android
   ```
3. من Android Studio: Build ← Build App Bundle(s) / APK(s) ← Build APK(s).

## لو عدّلت في التطبيق
الكود كله في فولدر `www` (الملف الأساسي `www/index.html`).
بعد أي تعديل: `npx cap sync android` (أو ارفع التعديل على GitHub وهيبني تاني لوحده).
