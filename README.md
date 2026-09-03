# MaxiFy — Compare Accounts (B2CORE iframe embed)

صفحة مقارنة الحسابات المخصصة للعرض داخل غرفة العميل (B2CORE) عبر Custom Behavior = Iframe.

## الرفع على GitHub Pages

```bash
git init
git add .
git commit -m "compare accounts embed"
git branch -M main
git remote add origin https://github.com/qaiserwh/maxify-compare.git
git push -u origin main
```

بعدها: Settings → Pages → Source = `main` / root.

الرابط يطلع:
```
https://qaiserwh.github.io/maxify-compare/
```

حطه بحقل **External URL** بصفحة السب منيو.

## البارامترات

| البارامتر | القيم | الافتراضي |
|---|---|---|
| `lang` | `ar` \| `en` | `ar` |
| `theme` | `dark` \| `light` | يتبع نظام التشغيل |
| `account` | `standard` \| `zero` \| `fy` \| `ea` | فارغ |
| `ui` | `clean` (يخفي شريط الاختبار) | ظاهر |

أمثلة:

```
.../?lang=ar&theme=dark&account=standard
.../?lang=en&theme=light&account=zero
.../?ui=clean&lang=ar
```

## قبل النشر النهائي

1. شغّل `diag.html` كـ External URL وشوف شنو B2CORE يمرر بالـ query. إذا يمرر theme/lang، اربطهن مباشرة.
2. لو ما يمرر شي، افتح تكت لـ B2Broker يطلب دعم placeholders بالـ iframe URL.
3. أضف `?ui=clean` بالنشر النهائي حتى ينخفي شريط الاختبار.
4. أي تعديل بالأرقام يصير بمصفوفة `PLANS` بأعلى السكربت فقط.

## نقطة مفتوحة

جدول المقارنة على الموقع يذكر رافعة EA = **1:100**، بينما كارت EA بنفس الصفحة يذكر **1:300**.
الملف الحالي يعتمد 1:100 (قيمة الجدول). يحتاج حسم مع التسويق والديلينج.
