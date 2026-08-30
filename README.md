# v0.4 — Supabase

هذه النسخة تنقل بيانات العقارات من الكود إلى قاعدة بيانات Supabase.

## الملفات
- index.html: الموقع العام
- admin.html: لوحة الإدارة
- config.js: بيانات الاتصال بـ Supabase
- schema.sql: إنشاء جدول العقارات وسياسات الأمان
- manifest.webmanifest: إعداد PWA

## الإعداد المختصر
1. أنشئ مشروعًا في Supabase.
2. افتح SQL Editor وشغّل محتوى schema.sql.
3. من Project Settings / API انسخ:
   - Project URL
   - anon أو publishable key
4. ضع القيمتين في config.js.
5. في Authentication فعّل Email login.
6. ارفع الملفات الأربعة إلى GitHub.
7. الموقع العام: /hello-app/
8. لوحة الإدارة: /hello-app/admin.html

## الأمان
لا تضع service_role key في GitHub أو JavaScript.
الموقع يستخدم Row Level Security بحيث العامة يرون العقارات المنشورة فقط،
والمستخدم المسجل يستطيع تعديل وحذف العقارات التي أنشأها هو فقط.
