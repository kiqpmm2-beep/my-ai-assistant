# المساعد الذكي الخاص بي

مساعد شخصي ذكي مبني باستخدام FastAPI و OpenAI.

## المميزات
- واجهة ويب تفاعلية
- حماية بمفتاح API خاص
- دعم كامل للغة العربية
- تشغيل سهل باستخدام Docker

## متطلبات التشغيل
- Python 3.9+
- Docker (اختياري)
- مفتاح API من OpenAI (اختياري)

## التشغيل المحلي

1. استنسخ المستودع:
```bash
git clone https://github.com/kiqpmm2-beep/my-ai-assistant.git
cd my-ai-assistant
```

2. قم بإنشاء وتفعيل البيئة الافتراضية:
```bash
python -m venv venv
source venv/bin/activate  # على Linux/macOS
# أو
venv\Scripts\activate  # على Windows
```

3. ثبت المتطلبات:
```bash
pip install -r requirements.txt
```

4. قم بتكوين المتغيرات البيئية:
```bash
export API_KEY_HASH="your-api-key-hash"
export OPENAI_API_KEY="your-openai-key"  # اختياري
```

5. شغل التطبيق:
```bash
uvicorn app:app --host 0.0.0.0 --port 8000
```

## التشغيل باستخدام Docker

1. ابنِ الصورة:
```bash
docker build -t my-ai-assistant .
```

2. شغل الحاوية:
```bash
docker run -p 8000:8000 \
  -e API_KEY_HASH="your-api-key-hash" \
  -e OPENAI_API_KEY="your-openai-key" \
  my-ai-assistant
```

## النشر على Render

1. انشئ حساباً على Render.com
2. اربط هذا المستودع
3. أضف متغيرات البيئة المطلوبة
4. اضغط Deploy

## الأمان
- جميع الطلبات تتطلب مفتاح API صالح
- يتم تخزين هاش المفتاح فقط، وليس المفتاح نفسه
- جميع الاتصالات مشفرة عبر HTTPS

## المساهمة
مرحباً بمساهماتك! يرجى إنشاء fork للمستودع وتقديم pull request.