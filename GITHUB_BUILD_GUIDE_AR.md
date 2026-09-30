# تشغيل المشروع من Chrome وبناء APK

## الخيار الأسهل: GitHub Actions

1. أنشئ مستودعًا جديدًا على GitHub من Chrome.
2. ارفع محتويات مجلد MathEditor إلى المستودع، بحيث يظهر في الجذر:
   - `settings.gradle`
   - `build.gradle`
   - `app/`
   - `.github/workflows/build-apk.yml`
3. افتح تبويب Actions.
4. اختر `Build Android APK`.
5. اضغط `Run workflow` إذا لم يبدأ البناء تلقائيًا.
6. بعد انتهاء المهمة افتح آخر تشغيل ناجح.
7. في أسفل الصفحة ستجد Artifacts.
8. حمّل `MathEditor-debug-apk`.
9. فك ضغط ملف الـArtifact، وستجد APK جاهزًا للتثبيت على هاتف Android.

## ملاحظة
GitHub Actions يستخدم Java 17 وGradle 8.7 وAndroid SDK 35 تلقائيًا، لذلك لا تحتاج إلى Android Studio أو SDK على جهازك لهذه الطريقة.

## Codespaces
يوجد أيضًا `.devcontainer/devcontainer.json` لتشغيل بيئة تطوير سحابية من المتصفح. بعد فتح Codespace يمكن استخدام الطرفية لبناء المشروع.
