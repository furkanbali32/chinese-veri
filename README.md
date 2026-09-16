# chinese-veri

"Hanzi Defteri · 字迹" uygulamasının **bulaşıcı lisanslı üç veri
dosyası**. Bu depo bir kütüphane değil; tek işi Arphic Public License,
CC BY-SA 4.0 ve CC BY-NC-SA 3.0'ın *"türetilmiş hâli erişilebilir olsun"* şartını
karşılamak.

Kaynak, lisans ve sınırların tamamı: [NOTICE](NOTICE) ·
lisans metinleri: [licenses/](licenses/)

| dosya | ne | lisans |
|---|---|---|
| `veri/strokes.js` | 1.187 karakterin vuruş verisi (SVG yolları + medians) | Arphic Public License |
| `veri/en.js` | 6.116 kelimenin İngilizce anlamı | CC BY-SA 4.0 (+ 582 kayıt LGPL 3.0) |
| `veri/grammar.js` | 311 gramer kalıbı (HSK 1-4), 3.662 örnek cümle | CC BY-NC-SA 3.0 — **ticari kullanım yok** |

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

### `veri/grammar.js` — 2026-07-18 / 2026-07-20, atıf 2026-09-16

Üstkaynak: **AllSet Learning Chinese Grammar Wiki**
(https://resources.allsetlearning.com/chinese/grammar/), © 2011-2026
AllSet Learning, CC BY-NC-SA 3.0; `krmanik/Chinese-Grammar` derlemesi
üzerinden.

Yapılan değişiklikler:

1. **Alan seçimi.** Her kalıptan başlık, yapı, kullanım etiketleri ve
   örnek cümleler (Çince, pinyin, İngilizce) alındı.
2. **Eklenen alanlar.** Elle yazılmış kısa Türkçe başlık (`tr`), kimlik
   (`id`) ve HSK 3.0 seviyesi (`lv`).

⚠ Pinyin alanı kaynaktan olduğu gibi geldi ve bilinen okunuş hataları
taşıyor (ör. 都 → dū); düzeltilmedi.



Serbestsiniz — lisansların koşullarına uyduğunuz sürece. `strokes.js`
için Arphic PL, `en.js` için CC BY-SA 4.0, `grammar.js` için CC BY-NC-SA 3.0
geçerli; üçü de türetilmiş hâlin aynı lisansla erişilebilir kalmasını
istiyor. `grammar.js` **ticari amaçla kullanılamaz** — AllSet Learning'e
göre reklamdan gelir getiren site ve uygulamalar da buna dahil.

`veri/en.js` iki lisansı karıştırdığı için (bkz. NOTICE) ayrıştırılmış
hâline ihtiyacınız varsa, kayıt başına kaynak bilgisi uygulamanın
üretecinden yeniden türetilebilir.
