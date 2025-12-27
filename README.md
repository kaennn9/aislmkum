# aislmkum

مكتبة بيانات إسلامية جاهزة:
- أذكار
- آيات
- قرآن
- تلاوات

## الاستخدام
```js
const aislmkum = require('aislmkum');

const azkar = aislmkum.azkar.morning();
const ayat = aislmkum.ayat.protection();
const surahs = aislmkum.quran.surahs();

---

# 3️⃣ `src/index.js` (مدخل المكتبة)

```js
const path = require('path');
const load = require('./utils/loadJson');

module.exports = {
  azkar: {
    morning: () => load('azkar/morning'),
    evening: () => load('azkar/evening'),
    sleep: () => load('azkar/sleep'),
    prayer: () => load('azkar/prayer'),
    general: () => load('azkar/general')
  },

  ayat: {
    protection: () => load('ayat/protection'),
    patience: () => load('ayat/patience'),
    rizq: () => load('ayat/rizq'),
    forgiveness: () => load('ayat/forgiveness')
  },

  quran: {
    surahs: () => load('quran/surahs'),
    juz: () => load('quran/juz'),
    hizb: () => load('quran/hizb'),
    pages: () => load('quran/pages')
  },

  tilawat: {
    reciters: () => load('tilawat/reciters'),
    murattal: () => load('tilawat/murattal'),
    mujawwad: () => load('tilawat/mujawwad'),
    audioMap: () => load('tilawat/audio_map')
  },

  meta: {
    languages: () => load('meta/languages'),
    translations: () => load('meta/translations'),
    sources: () => load('meta/sources')
  }
};
