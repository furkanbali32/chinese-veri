# chinese-veri

"Hanzi Defteri · 字迹" uygulamasının **bulaşıcı lisanslı iki veri
dosyası**. Bu depo bir kütüphane değil; tek işi Arphic Public License ve
CC BY-SA 4.0'ın *"türetilmiş hâli erişilebilir olsun"* şartını
karşılamak.

Kaynak, lisans ve sınırların tamamı: [NOTICE](NOTICE) ·
lisans metinleri: [licenses/](licenses/)

| dosya | ne | lisans |
|---|---|---|
| `veri/strokes.js` | 1.187 karakterin vuruş verisi (SVG yolları + medians) | Arphic Public License |
| `veri/en.js` | 6.116 kelimenin İngilizce anlamı | CC BY-SA 4.0 (+ 582 kayıt LGPL 3.0) |

---

## Arphic PL §2(a) — nasıl ve ne zaman değiştirildi

> *"You must insert a prominent notice in each modified file stating how
> and when you changed that file."*

### `veri/strokes.js` — 2026-09-04

Üstkaynak: Arphic PL KaitiM GB / AR PL UKai TrueType fontları
(Copyright © 1999 Arphic Technology Co., Ltd.), `skishore/makemeahanzi`
projesinin `graphics.txt` dosyası üzerinden.

Yapılan değişiklikler:

1. **Biçim dönüşümü.** Satır başına bir JSON nesnesi olan `graphics.txt`
   biçimi, tek bir JavaScript nesne sabitine (`export const HWDATA`)
   dönüştürüldü. Veri içeriği (yol dizgeleri ve median dizileri)
   değiştirilmedi.
2. **Alt kümeleme.** Yalnız HSK 3.0 (2021) resmî listesinde geçen 1.187
   karakter tutuldu; kalan karakterler çıkarıldı.
3. **Alan seçimi.** Her karakterden yalnız `strokes` ve `medians`
   alanları alındı.

Glif çizimlerine, koordinatlara veya vuruş sırasına **hiçbir müdahale
yapılmadı** — dönüşüm biçimsel ve seçicidir.

⚠ Kaynak tespiti bayt bayt doğrulanmadı; ayrıntı [NOTICE](NOTICE)'te.

### `veri/en.js` — 2026-09-04

Üstkaynak: CC-CEDICT (MDBG), `drkameleon/complete-hsk-vocabulary`
derlemesi üzerinden; ve 582 tek karakterlik kayıtta
`skishore/makemeahanzi` `dictionary.txt` (Unihan + CJKlib türevi).

Yapılan değişiklikler:

1. **Okunuşa göre anlam seçimi.** Çok okunuşlu kayıtlarda, sözlüğümüzün
   pinyin alanına karşılık gelen okunuşun anlamı seçildi.
2. **Sözlükbilim notlarının elenmesi.** `variant of…`, `see…`,
   `used in…`, `abbr. for…`, `bound form…`, `surname…` ile başlayan
   karşılıklar atıldı.
3. **Kısaltma ve biçimlendirme.** Karşılıklar kısaltıldı, ayraç `;`
   olarak birleştirildi, İngilizce metnin içindeki Çince karakterler
   temizlendi.
4. **Alt kümeleme.** Yalnız uygulamanın sözlüğündeki 6.116 kelime.

Anlamlar İngilizce'den İngilizce'ye alındı; çeviri yapılmadı.

---

## Bu dosyaları kullanmak isteyenler

Serbestsiniz — lisansların koşullarına uyduğunuz sürece. `strokes.js`
için Arphic PL, `en.js` için CC BY-SA 4.0 geçerli; ikisi de
türetilmiş hâlin aynı lisansla erişilebilir kalmasını istiyor.

`veri/en.js` iki lisansı karıştırdığı için (bkz. NOTICE) ayrıştırılmış
hâline ihtiyacınız varsa, kayıt başına kaynak bilgisi uygulamanın
üretecinden yeniden türetilebilir.
