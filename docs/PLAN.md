# PaperAnniversaryGift.com — GEO/SEO Site Planı

> Amaç: Yıldönümü hediyesi arayan kişilere hem Google'da hem AI asistanlarında (ChatGPT,
> Perplexity, Gemini, Google AI Overviews, Claude) görünmek ve trafiği Etsy'deki dijital
> "Love Map" ürününe yönlendirmek.

---

## 0. Karar Özeti (TL;DR)

| Konu | Karar |
|---|---|
| Stack | **Astro 5** (statik) + Tailwind CSS 4 + MDX içerik |
| Hosting | **Cloudflare Pages** (ücretsiz, sınırsız bandwidth, edge, kolay domain) |
| Repo | `alisahinboun/Lovemapwebsite`, branch `claude/paper-anniversary-gift-seo-y897gd` |
| Dil | Sadece **İngilizce (en-US)** — hedef pazar ABD/UK/CA/AU |
| CMS | Yok. İçerik repo'da markdown. Ekleme/düzenleme git üzerinden |
| Dönüşüm | Etsy'ye UTM'li çıkış linkleri + e-posta listesi (ücretsiz örnek karşılığı) |
| Analitik | GSC + Bing Webmaster + GA4 (veya Cloudflare Web Analytics) + UTM |
| İlk yayın | ~14 sayfa ile 2 hafta, sonra haftada 2-3 sayfa |

---

## 1. Stratejik Çerçeve

### 1.1 Neden ayrı bir site?
Etsy içi arama (Etsy SEO) ayrı bir oyun. Google ve AI asistanları Etsy listing'lerini
nadiren doğrudan önerir; onun yerine **rehber içerikleri** ve **markaları** alıntılar.
"Best paper anniversary gifts for husband" diye sorulduğunda AI, bir listicle veya
kategori sayfası okuyup oradan marka ismi verir. Bizim hedefimiz o alıntılanan
kaynak olmak.

### 1.2 İki katmanlı hedef
1. **Klasik SEO:** Google organik + Google AI Overviews (AI Overviews kaynaklarının
   büyük kısmı ilk 10 organik sonuçtan geliyor → organik sıralama hâlâ ön koşul).
2. **GEO (Generative Engine Optimization):** ChatGPT / Perplexity / Copilot alıntıları.
   Bunlar farklı sinyallerle çalışır: marka bahsi (brand mention), üçüncü taraf
   listicle'larda geçmek, alıntılanabilir istatistik, tablo, entity tutarlılığı,
   içerik tazeliği. Backlink'ten çok "kaç yerde adın geçiyor" önemli.

### 1.3 Rekabet manzarası (araştırma bulgusu)
Alanda güçlü oyuncular var:
- `paper-anniversary.com` — **Paper Anniversary® by Anna V.** (tescilli marka, güçlü otorite)
- `mrkyourmoment.com` — çok sayıda anniversary map print sayfası, iyi yapılanmış
- `papier.com`, `uncommongoods.com`, `paperlust.co`, `theknot.com`, `brides.com` — büyük
  yayıncı/perakendeci; "1st anniversary gift ideas" gibi head keyword'lerde hâkim
- Etsy market sayfaları (`etsy.com/market/anniversary_map`) — Google'da sıralanıyor

**Sonuç:** Head keyword'lerde ("1st anniversary gift ideas") kısa vadede kazanamayız.
Strateji **long-tail + niş dikey + programatik küme** üzerinden ilerlemek, otorite
biriktikçe yukarı tırmanmak.

### 1.4 ⚠️ KRİTİK RİSK: Marka/Trademark
`Paper Anniversary®` ABD'de aynı kategoride (yıldönümü hediyesi) tescilli görünüyor.
`PaperAnniversaryGift.com` domaini **jenerik tanımlayıcı kullanım** olarak savunulabilir
ama:
- Site adını/logosunu "Paper Anniversary Gift" olarak **marka gibi** kullanmak
  (logo, tagline, "by us") risk yaratır.
- Etsy shop'un adı ile bu domain'in adı çakışırsa karışıklık iddiası güçlenir.

**Önerim:** Domain'i tut, ama **marka kimliğini ayrı kur.**
- Marka adı: **LoveMap** (veya senin Etsy shop adın) — logo, Organization schema,
  e-posta, sosyal hesaplar hep bu isimle.
- Domain sadece "konu domaini" olarak kullanılsın: site başlığı
  *"Paper Anniversary Gift Guide by LoveMap"* değil, **"LoveMap — Paper Anniversary Gifts"**.
- Hiçbir yerde `®` veya "Paper Anniversary" tek başına marka gibi geçmesin.
- Yayına almadan önce USPTO TESS'te `paper anniversary` aramasını yapıp sonucu gör.
  Gerekirse 1 saatlik bir IP avukatı danışmanlığı en ucuz sigorta.

---

## 2. Anahtar Kelime Mimarisi

### 2.1 Küme 1 — Ürün / Ticari niyet (dönüşüm sayfaları)
Yüksek niyet, düşük hacim, düşük rekabet. **En kârlı taraf.**

- paper anniversary gift for husband
- paper anniversary gift for wife
- 1st anniversary gift for him / for her
- personalized love map print
- relationship map print
- our love story map
- custom couple timeline map
- printable anniversary gift (instant download)
- last minute anniversary gift printable / digital
- long distance relationship map gift
- where we met map print
- anniversary gift digital download

### 2.2 Küme 2 — Bilgi amaçlı (trafik + AI alıntı motoru)
- what is the paper anniversary / why is paper the 1st anniversary gift
- 1st anniversary gift ideas (head — uzun vade)
- traditional vs modern anniversary gifts by year
- paper anniversary gift etiquette / what to write in a 1st anniversary card
- how to frame a printable gift / best paper to print art at home
- best print sizes for wall art (A2 / 18x24 / 24x36 karşılaştırma)

### 2.3 Küme 3 — Programatik küme (ölçek)
**A) Yıla göre:** 1st → 75th anniversary = ~30 sayfa (1-20 yıl tek tek, sonra 25/30/40/50/60/75)
Her sayfa: geleneksel malzeme, modern karşılığı, çiçek, taş, renk + 8-12 hediye fikri +
bizim ürün varyantı. Bu **gerçek değer** üretir, thin content değil.

**B) Malzemeye göre:** paper, cotton, leather, fruit/flowers, wood, candy/iron, wool,
bronze, pottery, tin... = ~20 sayfa

**C) Alıcı personasına göre:** for husband / wife / boyfriend / girlfriend / parents /
in-laws / best friend / long distance / newlyweds = ~10 sayfa

> ⚠️ Kural: Programatik sayfaların **her biri** en az 600 kelime özgün metin + kendi
> görselleri + kendi FAQ'ı taşımalı. Sadece template'e değişken basmak Google'ın
> "scaled content abuse" politikasına girer.

### 2.4 Küme 4 — Ücretsiz araçlar (link + alıntı mıknatısı)
Bunlar backlink ve AI alıntısı çekmenin en hızlı yolu:
1. **Anniversary Year Gift Finder** — yıl gir → geleneksel/modern/çiçek/taş/renk çıkar
2. **Coordinates Finder** — adres/şehir gir → enlem-boylam (map ürünleri için)
3. **Print Size Calculator** — dosya çözünürlüğü gir → hangi boyuta net basılır
4. **Anniversary Date Countdown / "How long have we been together"** hesaplayıcı

Hepsi client-side JS, sunucu gerekmez, statik sitede çalışır.

### 2.5 Küme 5 — Özgün veri (GEO'nun gizli silahı)
AI motorları **alıntılanabilir istatistik** arıyor. Kendi verimizi üretelim:

- **"2026 Anniversary Gift Report"**: 300-500 kişilik anket (Prolific/Google Surveys,
  ~$150-300) → "%X of couples spend under $50 on their 1st anniversary",
  "%Y prefer personalized over generic gifts"
- **Etsy pazar analizi**: 500 "anniversary map" listing'inin fiyat dağılımı, ortalama
  teslim süresi, en çok kullanılan tag'ler → tamamen bizim verimiz, kimsede yok
- Her yıl güncelle → tazelik sinyali

Bu tek başına, 20 tane listicle'dan daha fazla AI alıntısı getirir.

---

## 3. Site Mimarisi

```
/                                   Ana sayfa (ürün + değer önerisi + hub linkleri)
/love-map/                          Ana ürün sayfası (Product schema, Etsy CTA)
  /love-map/for-husband/            Persona varyantı
  /love-map/for-wife/
  /love-map/long-distance/
/gifts/                             Hub: tüm hediye rehberleri
  /gifts/paper-anniversary/         Küme 1+2 pillar sayfası (en önemli sayfa)
  /gifts/paper-anniversary-for-him/
  /gifts/paper-anniversary-for-her/
  /gifts/printable-anniversary-gifts/
  /gifts/last-minute-anniversary-gifts/
/anniversary/                       Hub: yıla göre
  /anniversary/1st-year/ ... /75th-year/
/materials/                         Hub: malzemeye göre
  /materials/paper/ /cotton/ /leather/ ...
/guides/
  /guides/what-is-paper-anniversary/
  /guides/traditional-vs-modern-anniversary-gifts/
  /guides/how-to-print-digital-art-at-home/
  /guides/best-frames-for-printable-art/
  /guides/what-to-write-in-anniversary-card/
/tools/
  /tools/anniversary-gift-finder/
  /tools/coordinates-finder/
  /tools/print-size-calculator/
/research/
  /research/anniversary-gift-report-2026/
/about/                             E-E-A-T: gerçek kişi, foto, hikâye, iletişim
/contact/
/privacy/  /terms/                  Yasal (GDPR/CCPA, e-posta topluyorsak zorunlu)
```

**İç linkleme kuralı:** Her rehber sayfası → ilgili ürün sayfasına en az 2 kontekstüel
link. Her ürün sayfası → 3 ilgili rehbere. Hub sayfaları tüm alt sayfalara.

---

## 4. Sayfa Şablonu (GEO-optimize)

Her içerik sayfası şu iskeletle yazılacak — bu iskelet AI'ın içeriği "çıkarmasını"
(extraction) kolaylaştırır:

1. **H1** — hedef keyword doğal biçimde
2. **Answer block (40-60 kelime)** — H1'in hemen altında, kutu içinde, soruyu doğrudan
   yanıtlar. AI'ın kopyalayıp alıntılayacağı blok bu. `<p class="answer">` + schema
3. **Hızlı özet / TL;DR** — 3-5 madde
4. **Karşılaştırma tablosu** — AI'lar tabloları çok seviyor (fiyat, malzeme, teslim süresi)
5. **Gövde** — H2/H3 ile bölümlenmiş, her H2 tek bir alt soruyu yanıtlar, paragraflar
   40-80 kelime (uzun blok yerine)
6. **Özgün veri/alıntı** — kendi istatistiğimiz veya deneyimimiz
7. **FAQ (5-8 soru)** — FAQPage schema ile
8. **Son güncelleme tarihi** — görünür + `dateModified`
9. **Yazar kutusu** — gerçek isim, foto, kısa bio (E-E-A-T)
10. **CTA** — Etsy'ye UTM'li link + e-posta yakalama

### Yazım kuralları
- İlk cümlede cevap. "Giriş paragrafı" yazma.
- Sayısal ve spesifik ol: "$18" > "affordable", "24x36 inches" > "large"
- Tanımlayıcı cümleler kur: *"A paper anniversary gift is a present given on the first
  wedding anniversary..."* — AI bu kalıptaki cümleleri alıntılar
- Marka adını (LoveMap) düzenli ama doğal geçir — entity tutarlılığı
- Fluff, "in today's world", "when it comes to" gibi kalıpları sıfırla

---

## 5. Teknik SEO / GEO Uygulaması

### 5.1 Statik ve hızlı
- Astro → sıfır JS default. Sadece araç sayfalarında island hydration.
- Görseller: `astro:assets` ile AVIF + WebP, responsive `srcset`, `loading="lazy"`
  (LCP görseli hariç), açık `width`/`height` (CLS=0)
- Font: sadece 2 ağırlık, `font-display: swap`, self-hosted (Google Fonts'a bağlanma)
- Hedef: LCP < 1.8s, INP < 100ms, CLS < 0.05, mobil PSI > 95

### 5.2 Schema.org (JSON-LD) — hepsi zorunlu
| Sayfa tipi | Schema |
|---|---|
| Global | `Organization` (logo, sameAs: Etsy/Pinterest/IG), `WebSite` + `SearchAction` |
| Ürün | `Product` + `Offer` (fiyat, currency, availability) + `AggregateRating` (sadece gerçek Etsy yorumları varsa!) |
| Rehber | `Article` / `BlogPosting` (author, datePublished, dateModified) |
| Listicle | `ItemList` + her item `Product`/`Thing` |
| FAQ | `FAQPage` |
| Nasıl yapılır | `HowTo` |
| Her sayfa | `BreadcrumbList` |
| About | `Person` (author entity) |

> ⚠️ `AggregateRating`'i uydurma. Google manual action verir. Etsy yorumlarını
> gerçekten sitede gösteriyorsan (alıntı + link ile) kullan.

### 5.3 Crawler erişimi — GEO için kritik
`robots.txt` içinde AI crawler'larını **açıkça izinle**:
```
User-agent: GPTBot            # ChatGPT training
User-agent: OAI-SearchBot     # ChatGPT search — bu olmadan ChatGPT'de görünmezsin
User-agent: ChatGPT-User
User-agent: ClaudeBot
User-agent: Claude-SearchBot
User-agent: PerplexityBot
User-agent: Google-Extended   # Gemini/AI Overviews
User-agent: Bingbot           # Copilot + ChatGPT'nin web indeksi
User-agent: Applebot-Extended
User-agent: Amazonbot
User-agent: meta-externalagent
Allow: /
```
Cloudflare'ın **"Block AI Scrapers"** ayarını **kapat** — açık kalırsa GEO çalışmaz.
(Cloudflare bunu bazı planlarda default açıyor; kontrol et.)

### 5.4 llms.txt
Kökte `/llms.txt` — sitenin makine-okunur haritası: ne satıyoruz, ana sayfalar,
markdown karşılıkları. Ayrıca her sayfanın `.md` versiyonunu üret (`/gifts/paper-anniversary.md`)
— Astro build hook'u ile otomatik. Henüz resmi standart değil ama maliyeti sıfır,
Perplexity/Claude tarafında işe yarıyor.

### 5.5 Indexleme
- `sitemap.xml` (Astro sitemap integration) + `sitemap-index`
- **Bing Webmaster Tools'a kaydol** — ChatGPT'nin web araması Bing indeksine dayanıyor.
  Çoğu kişi bunu atlıyor; GEO için Google kadar önemli.
- **IndexNow** — Cloudflare Pages deploy hook'u ile her yayında ping
- Canonical, hreflang gerekmiyor (tek dil), `og:` + `twitter:` meta tam

### 5.6 Erişilebilirlik
Semantik HTML, alt text (görsel içeriğini gerçekten anlat — AI görsel alt'larını okur),
kontrast AA, klavye navigasyonu. Hem SEO hem GEO hem doğru iş.

---

## 6. Off-site: Marka Bahsi Kampanyası (GEO'nun %50'si)

AI'lar sadece senin siteni okumaz — **başkalarının senin hakkında yazdığını** okur.
Sıralı görev listesi:

1. **Listicle'lara girmek (en yüksek ROI).**
   "best paper anniversary gifts" için ilk 20 sonucu çıkar → her birine kişisel
   e-posta: ürün örneği ücretsiz + yüksek çözünürlüklü görsel + hazır 2 cümlelik
   açıklama. Hedef: 3 ay içinde 8-10 listicle'da geçmek. AI bu listeleri okuyup
   marka ismi veriyor.
2. **Reddit** — r/relationships, r/GiftIdeas, r/weddingplanning, r/AskMen, r/AskWomen.
   Spam değil: gerçekten yardım eden yorumlar, ürünü ancak sorulunca söyle.
   Reddit, AI motorlarının en çok alıntıladığı kaynaklardan biri.
3. **Quora** — "what's a good 1st anniversary gift" tipi sorulara detaylı yanıt
4. **Pinterest** — bu niş için birincil trafik kanalı. Her sayfa için 3-5 dikey pin
   (1000x1500), zengin pin schema. Anniversary/wedding içeriği Pinterest'te patlar.
5. **YouTube Shorts / TikTok / IG Reels** — "unboxing"/"printing at home" 15-30 sn
   videolar. Google video sonuçlarında ve AI'da video alıntısı artıyor.
6. **Entity tutarlılığı** — Etsy shop, Pinterest, Instagram, site, Google Business
   (varsa) hepsinde **aynı** marka adı, aynı açıklama, aynı logo, karşılıklı linkler
   (`sameAs`). AI'ın "bu aynı varlık" demesi için gerekli.
7. **Digital PR** — Küme 5'teki anket raporunu wedding blog'larına pitch et.
   Veri, link kazanmanın en kolay yolu.

---

## 7. Dönüşüm Tasarımı

### 7.1 Etsy'ye yönlendirme
- Her CTA'da UTM: `?utm_source=pag&utm_medium=web&utm_campaign=<sayfa-slug>`
  → Etsy Shop Stats'te hangi sayfanın sattığını görürsün
- CTA metni jenerik olmasın: "Get the Love Map on Etsy — instant download, $XX"
- Ürün sayfasında gerçek mockup galerisi (4-6 görsel), fiyat, teslim süresi,
  dosya formatları, boyutlar, örnek Etsy yorumları → tıklamadan önce güven

### 7.2 E-posta listesi (Etsy bağımlılığını kırar)
- Lead magnet: **ücretsiz basılabilir bir şey** — "Anniversary Card Template Pack"
  veya "Printable Love Coupons" (düşük efor, yüksek algılanan değer)
- Araç: Buttondown veya MailerLite (ücretsiz kademe), Cloudflare Worker ile form
- Otomasyon: 3 e-postalık welcome dizisi → 3. e-postada ürün + %10 kod
- Uzun vade: kendi satış kanalı (Gumroad/Lemon Squeezy) → Etsy komisyonunu (6.5% +
  listing + reklam) kes. Site trafiğini kendi ödeme sayfana yönlendirebilirsin.

### 7.3 Ölçüm
- Google Search Console + **Bing Webmaster Tools**
- GA4 (veya privacy-friendly: Cloudflare Web Analytics / Plausible)
- Event'ler: `etsy_click`, `email_signup`, `tool_used`, scroll depth
- **AI görünürlük takibi:** 25-30 hedef prompt'luk bir tablo tut
  ("what's a good paper anniversary gift for my husband?" vb.), ayda 1 kez
  ChatGPT/Perplexity/Gemini/Claude'da elle sor, marka geçiyor mu kaydet.
  Ücretli alternatif: Profound, Peec AI, Otterly (ayda ~$50-100) — ilk 3 ay
  gerekmez, elle yeter.

---

## 8. Yol Haritası

### Faz 0 — Hazırlık (1-2 gün)
- [ ] Domain al/DNS'i Cloudflare'a taşı
- [ ] **Trademark kontrolü** (USPTO TESS) + marka adı kararı
- [ ] Etsy listing detaylarını topla (başlık, fiyat, dosyalar, mockup'lar, yorumlar)
- [ ] Marka kimliği: isim, logo, 2 font, 4-5 renk paleti
- [ ] GSC + Bing Webmaster + analitik hesapları

### Faz 1 — İskelet + ilk 14 sayfa (1-2 hafta)
- [ ] Astro projesi, Tailwind, tipografi sistemi, layout'lar
- [ ] Schema/SEO component'leri (tek yerden yönetilen `<Seo>` component)
- [ ] robots.txt, sitemap, llms.txt, IndexNow hook
- [ ] Sayfalar: Ana sayfa, `/love-map/`, `/gifts/paper-anniversary/` (pillar),
      for-him, for-her, printable, last-minute, what-is-paper-anniversary,
      traditional-vs-modern, how-to-print, best-frames, about, contact, privacy
- [ ] Cloudflare Pages'e deploy, Core Web Vitals doğrulama
- **Çıktı:** indexlenebilir, hızlı, 14 sayfalık gerçek site

### Faz 2 — Araçlar + programatik küme (2-3 hafta)
- [ ] 3 ücretsiz araç (gift finder, coordinates, print size)
- [ ] `/anniversary/1st..75th` — 30 sayfa (her biri özgün metin + FAQ)
- [ ] `/materials/*` — 12-20 sayfa
- [ ] Ürün persona varyantları (for-husband, for-wife, long-distance)
- [ ] Pinterest hesabı + ilk 50 pin
- **Çıktı:** ~60 sayfa, uzun kuyruk trafiği başlar

### Faz 3 — Otorite + GEO itmesi (4-8. hafta)
- [ ] Anket → `/research/anniversary-gift-report-2026/`
- [ ] 20 listicle outreach'i
- [ ] Reddit/Quora katılımı (haftada 3-4 gerçek yanıt)
- [ ] E-posta lead magnet + welcome dizisi
- [ ] AI prompt takip tablosunun ilk ölçümü
- **Çıktı:** ilk AI alıntıları, ilk backlink'ler

### Faz 4 — İterasyon (sürekli)
- Haftada 2-3 yeni sayfa (GSC "impressions var, click yok" sorgularından)
- Ayda 1: en iyi 10 sayfayı güncelle (`dateModified` tazeliği)
- Sezonluk itme: Ocak-Şubat (Sevgililer), Mayıs-Haziran, Eylül-Ekim (yıldönümü pikleri)
- Ürün genişletme: her yeni Etsy varyantı için ayrı landing page

---

## 9. Beklentiler ve Riskler

### Gerçekçi zaman çizelgesi
| Süre | Beklenti |
|---|---|
| 0-4 hafta | Indexleme, günlük 0-20 ziyaret. Hiç satış olmayabilir — normal |
| 2-3 ay | Long-tail sıralamalar, günlük 50-150 ziyaret, ilk AI alıntıları |
| 4-6 ay | Günlük 300-800 ziyaret, düzenli Etsy tıklamaları, orta rekabetli keyword'lerde ilk sayfa |
| 9-12 ay | Head keyword'lerde ilk sayfa mücadelesi, günlük 1500+ potansiyeli |

Yeni domain için "sandbox" etkisi gerçek. İlk 3 ay sabır gerektirir.

### Riskler ve azaltımlar
| Risk | Azaltım |
|---|---|
| **Trademark ihtilafı** (Paper Anniversary®) | Marka kimliğini ayır, domaini tanımlayıcı kullan, hukuki kontrol |
| **EMD + thin content** = Google cezası | Her sayfa özgün ve derin; programatik sayfalar template değil |
| **Etsy bağımlılığı** (hesap kapanırsa trafik boşa gider) | E-posta listesi + kendi ödeme kanalı (Faz 3+) |
| **AI Overviews'un tıklamayı yemesi** | Marka bahsi stratejisi: tıklama olmasa da isim geçsin. Bottom-funnel ürün sayfalarına yatırım |
| **Google core update** | Tek keyword'e değil, geniş konu kümesine yayıl |
| **Sezonluk dalgalanma** | Hem yıldönümü hem doğum günü/Sevgililer/düğün kümelerini kapsa |
| **Affiliate/reklam olmadan monetizasyon sadece 1 ürün** | 3-5 dijital ürün varyantı üret (fiyat basamakları: $8 / $18 / $35 bundle) |

---

## 10. Senden İhtiyacım Olanlar

Etsy'ye erişim bu ortamda bloklu, o yüzden şunları bana yazman/yüklemen lazım:

1. **Ürün detayları:** tam listing başlığı, fiyat, dosya formatları (PDF/PNG/JPG?),
   boyutlar, teslim şekli (anında indirme mi, kişiselleştirme sonrası mı?),
   kişiselleştirme için müşteriden ne istiyorsun
2. **Etsy shop adı** ve shop URL'si
3. **Mockup/ürün görselleri** — repo'ya koyabileceğim yüksek çözünürlüklü dosyalar
4. **Mevcut yorumlar** — sayı, ortalama puan, 3-4 alıntılanabilir yorum metni
5. **Marka adı kararı** — LoveMap mi, Etsy shop adın mı, başka bir şey mi?
6. **Domain durumu:** PaperAnniversaryGift.com alındı mı? DNS nerede?
7. **Yazar kimliği (E-E-A-T):** sitede gerçek isim + foto + kısa hikâye kullanabilir
   miyiz? ("Ben ve eşim ilk yıldönümümüzde..." tipi gerçek hikâye dönüşümü ciddi artırır)
8. **Bütçe:** anket ($150-300), AI takip aracı ($50-100/ay), Pinterest zamanlama aracı
   — hangilerine açıksın? Hepsi opsiyonel, sıfır bütçeyle de başlanır
9. **Başka ürünler var mı?** (varyant/bundle stratejisi için)

---

## 11. İlk Commit'te Ne Yapacağım (onay verirsen)

1. Astro + Tailwind + MDX iskeleti, TypeScript strict
2. `<Seo>` + `<Schema>` component'leri (tüm JSON-LD tek yerden)
3. Layout: header/footer/breadcrumb/CTA/answer-block/FAQ/comparison-table component'leri
4. robots.txt, sitemap, llms.txt, `.md` mirror üreteci
5. Ana sayfa + `/gifts/paper-anniversary/` pillar sayfası (tam içerikli, örnek olsun)
6. Cloudflare Pages config + deploy talimatları (`docs/DEPLOY.md`)
7. Lighthouse/CWV doğrulaması

Sonrasında sayfa sayfa içerik üretimine geçeriz.
