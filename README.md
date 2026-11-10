# Speed Rush ⚡

لعبة سباق لا نهائية للهواتف، بواجهة عربية واستجابة للمس والتحكم بالسحب أو الأزرار، وسيارات قابلة للفتح وعملات وأفضل نتيجة محفوظة محلياً.

## تشغيل اللعبة

```bash
npm ci
npm run dev
```

افتح عنوان الخادم المعروض. يمكن استخدام الأسهم أو A / D على لوحة المفاتيح أيضاً.

## بناء الويب

```bash
npm run build
```

الناتج في `dist/`. اللعبة تعمل دون خدمة خلفية، وتخزن تقدمها على الجهاز في Local Storage. الأصوات مركبة محلياً عبر Web Audio API، ولا تعتمد اللعبة على موارد خارجية.

## Android APK

مشروع Android الأصلي موجود في `android/` باستخدام Capacitor. يتطلب البناء JDK 17 وAndroid SDK (Platform 35 وBuild Tools) مع ضبط `ANDROID_HOME` و`JAVA_HOME`:

```bash
npm ci
npm run android:apk
```

سيكون ملف التثبيت في `android/app/build/outputs/apk/debug/app-debug.apk`. للبناء عبر Android Studio، افتح مجلد `android/` بعد تنفيذ `npm run android:sync` ثم اختر Build APK(s).

**ملاحظة:** لم يمكن إخراج ملف APK داخل بيئة العمل الحالية لعدم توفر JDK وAndroid SDK. المشروع والمصادر وملفات Gradle جاهزة للبناء على جهاز مهيأ بأدوات Android.

## iPhone

واجهة الويب متكيفة مع شاشات iPhone ومناطق الأمان. لإنتاج تطبيق iOS أصلي، على macOS مع Xcode نفّذ `npx cap add ios` ثم `npm run build && npx cap sync ios` وافتح مشروع iOS في Xcode.
