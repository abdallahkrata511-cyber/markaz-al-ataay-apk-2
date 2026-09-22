# مركز العطايا لتوزيع المواد الغذائية

نسخة مهيأة للبناء كتطبيق Android عبر Capacitor 8 وGitHub Actions.

## أهم الإصلاحات
- Package ID ثابت: `com.abdullahataya.fooddistribution`.
- عدم خلط Capacitor 6 مع 8.
- SQLite محلي على Android عبر `@capacitor-community/sqlite` مع ترحيل بيانات localStorage القديمة إلى SQLite عند أول تشغيل.
- سعر بيع ثابت لكل منتج مع اختيار SYP/USD.
- دعم تثبيت فاتورة بالدولار بسعر صرف تاريخي محفوظ داخل الفاتورة.
- منع بيع كمية أكبر من المخزون عند إنشاء فاتورة جديدة.
- حفظ تكلفة المنتج وقت البيع داخل بند الفاتورة.
- طباعة حرارية Native على Android عبر Bluetooth Classic SPP للطابعات المقترنة، مع ESC/POS خام.
- PDF حقيقي عبر Capacitor Filesystem + Share.
- GitHub Actions يبني `AlAtaya-debug.apk` تلقائياً.

## بناء APK

1. ارفع الملفات إلى مستودع GitHub.
2. اجعل الفرع `main`.
3. افتح تبويب Actions وشغّل `Build Android APK`.
4. بعد نجاح البناء ستجد `AlAtaya-debug.apk` في Artifacts.

## ملاحظة الطابعة

يجب إقران الطابعة أولاً من إعدادات Bluetooth في Android. عند شراء الطابعة لاحقاً، يفضّل اختبارها فعلياً لأن بعض الطابعات تستخدم BLE بدلاً من Bluetooth Classic SPP.
