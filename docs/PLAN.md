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
| Repo | `alisahinboun/Lovemapwebsite`, branch `claude/paper-anniversary-gift-seo-kuetsr` |
| Marka | **byAliden** (Ali, İstanbul — Etsy Star Seller, 5 yıl, 530 satış) |
| Ürün | Made-to-order dijital illüstrasyon, **$47.17** (liste $62.90) — impulse değil, **premium** |
| Dönüşüm modeli | Yüksek AOV + düşük hacim. Günde 3 satış = aylık ~$4.200 ciro |
| Dil | Sadece **İngilizce (en-US)** — hedef pazar ABD/UK/CA/AU |
| CMS | Yok. İçerik repo'da markdown. Ekleme/düzenleme git üzerinden |
| Dönüşüm | Etsy'ye UTM'li çıkış linkleri + e-posta listesi (ücretsiz örnek karşılığı) |
| Analitik | GSC + Bing Webmaster + GA4 (veya Cloudflare Web Analytics) + UTM |
| İlk yayın | ~14 sayfa ile 2 hafta, sonra haftada 2-3 sayfa |

---

## 0.5 Ürün Gerçekleri (listing verisinden, 8 Eylül 2026)

Bunlar tahmin değil, listing'in kendisinden. Sitedeki her sayfa bu gerçeklere göre yazılacak.

| Alan | Değer |
|---|---|
| Listing başlığı | *Paper Anniversary Gift for Husband & Wife: Hello Will You I Do Timeline, Personalized Map* |
| Fiyat | **$47.17** (indirimli) / $62.90 liste — 25% off, 3 Ekim'e kadar |
| Rozetler | **Bestseller** · **Star Seller** · "2 people bought this in the last 24 hours" |
| Sosyal kanıt | **4.9 ★ / 119 yorum** bu listing'de, %97 tavsiye · **2.637 favori** · shop 4.9 (145) / 530 satış |
| Teslim | **Made-to-order digital download** — anında indirme *değil*. Yorumlara göre ilk taslak **24 saat**, teslim **1-2 iş günü** |
| Format | 300 DPI PDF · 50×70 cm · 16x20 / 18x24 / A3 / A2 ölçeklenebilir |
| Stil | Minimalist **"Japandi"** esintili, siyah-beyaz line art |
| Kişiselleştirme | İsimler + **5-8 milestone** (yer/olay + tarih) |
| Satıcı | Ali · İstanbul · Etsy'de 5 yıl · birkaç saat içinde yanıt |
| Lisans | Kişisel kullanım, ticari satış yok, çizim başladıktan sonra iade yok |

### Diğer listing'ler (fiyat merdiveni zaten var!)
| Ürün | Fiyat | Rolü |
|---|---|---|
| Custom Travel Map Print — Mountain Wall Art | **$15.00** | Giriş seviyesi / upsell yemi |
| Personalized **Website** — Hello Will You I Do | **$30.90** | ⭐ **Sitenin gizli kozu** — aşağıda |
| Love Map (bu ürün) | **$47.17** | Ana ürün |
| Love Map varyantı | **$64.90** | Premium basamak |

### ⚠️ Bu veriler planı üç yerde değiştiriyor

**1. Bu bir "printable" ürünü değil, bir hizmet.** $47'lık made-to-order özel illüstrasyon,
$8'lık instant download'dan tamamen farklı bir satın alma. Ziyaretçi tıklamadan önce
*"bu adam benim hikâyemi gerçekten çizecek mi?"* sorusunu yanıtlamak zorundayız. Yani site
bir katalog değil, bir **portfolyo + süreç anlatımı** olmalı: gerçek müşteri sonuçları,
öncesi/sonrası, "24 saatte ilk taslak" vaadi, revizyon politikası.
→ `last minute` ve `instant download` keyword'lerini **birincil vaat olarak kullanmıyoruz**;
   dürüst çerçeve: *"Delivered in 24-48 hours — no shipping, no waiting for the post."*

**2. Yüksek AOV oyunu tersine çeviriyor.** $47 ürün + %3-5 dönüşümle günde
**30-50 ziyaretçi** ayda ~$2.000 ciro demek. Yani "günde 1.500 ziyaretçi" hedefine gerek yok;
**doğru 50 ziyaretçi** yeter. Bu, stratejiyi head keyword yarışından tamamen uzaklaştırıp
yüksek niyetli long-tail'e kilitler. İyi haber.

**3. `Personalized Website` ürünü ($30.90) bu projenin en büyük fırsatı.**
Bir *web sitesi* satıyorsun ve bir *web sitesi* kuruyoruz. Yani:
- Sitede **canlı, gezilebilir bir demo** koyabiliriz (`/demo/hello-will-you-i-do/`) —
  örnek bir çiftin timeline'ı, gerçekten çalışan bir sayfa
- Bu demo hem dönüşüm aracı hem **link/alıntı mıknatısı**: AI'lar ve blog'lar
  "çalışan örneği olan" sayfaları alıntılamayı sever
- Ayrıca `wedding website`, `digital love story page`, `anniversary website for husband`
  gibi tamamen ayrı ve daha az rekabetli bir keyword evreni açar

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

### 1.3 Rekabet manzarası (Eylül 2026'da doğrulandı)

**Katman A — Büyük yayıncı/perakendeci (head keyword'lerde hâkim):**
`theknot.com`, `brides.com`, `uncommongoods.com`, `paperlust.co`, `papier.com`.
"1st anniversary gift ideas" gibi baş kelimelerde kısa vadede bunlarla yarışamayız.

**Katman B — Niş marka siteleri (asıl rakip *ve* asıl kanıt):**
`paperanniversaryideas.com` (`/for-him` gibi persona sayfaları), `amourprint.com`
(`/pages/best-paper-anniversary-gift-ideas`), `unwilted.com/blogs/...`,
`paper-anniversary.com` (**Paper Anniversary® by Anna V.** — marka riski, §1.4).

**Katman C — Doğrudan ürün rakipleri (love map / where-we-met):**
`positiveprints.com` (where-we-met-map, where-it-all-began-map),
`mrkyourmoment.com` (anniversary-map-print, coordinate map, circle map — çok iyi
yapılanmış koleksiyon mimarisi), `pixelsphotoart.com`, `journeyprintshop.com`.
Ayrıca Etsy market sayfaları (`etsy.com/market/paper_anniversary_gift_for_him`)
Google'da 1. sırada çıkıyor — yani **Etsy listing'in değil, Etsy'nin kategori sayfası
sıralanıyor**; senin listing'in oradan trafik almıyor.

**🔑 En önemli bulgu:** Bu sorguyu AI destekli aramada test ettiğimde, verilen cevap
büyük markaları değil **küçük niş marka sitelerini** (amourprint, unwilted,
paperanniversaryideas) kaynak gösterdi ve fiyat/malzeme detaylarını doğrudan onların
sayfalarından alıntıladı. Yani: *doğru yapılandırılmış küçük bir site, bu nişte AI
alıntısı alabiliyor.* Bu planın tüm dayanağı bu.

**Sonuç:** Head keyword'lerde kısa vadede kazanamayız. Strateji **long-tail + niş dikey
+ programatik küme + alıntılanabilir format** üzerinden ilerlemek; Katman B'nin yerini
almak (ulaşılabilir hedef), Katman A'ya uzun vadede tırmanmak.

### 1.4 ⚠️ KRİTİK RİSK: Marka/Trademark
`Paper Anniversary®` ABD'de aynı kategoride (yıldönümü hediyesi) tescilli görünüyor.
`PaperAnniversaryGift.com` domaini **jenerik tanımlayıcı kullanım** olarak savunulabilir
ama:
- Site adını/logosunu "Paper Anniversary Gift" olarak **marka gibi** kullanmak
  (logo, tagline, "by us") risk yaratır.
- Etsy shop'un adı ile bu domain'in adı çakışırsa karışıklık iddiası güçlenir.

Ek olarak Etsy'de **`PaperAnniversaryLove`** adlı bir shop da var — yani bu isim etrafında
kalabalık artıyor, kendi ismini domain'e bağlamak stratejik olarak da zayıf.

**Önerim:** Domain'i tut, ama **marka kimliğini `byAliden` üzerine kur.**
Bu, hukuki riski çözmenin yanında bedava bir avantaj daha veriyor: byAliden zaten Etsy'de
**Star Seller** — yani satış geçmişi, yorumlar ve güven sinyali hazır. Sıfırdan marka
kurmaktan iyi.
- Logo, `Organization` schema `name`, e-posta, sosyal hesaplar, yazar kutusu → hepsi **byAliden**
- Site başlığı: **"byAliden — Paper Anniversary Gifts"** (❌ "Paper Anniversary Gift™ by us")
- Hiçbir yerde `®` kullanma, "Paper Anniversary" tek başına logo/marka gibi geçmesin —
  sadece **tanımlayıcı** (descriptive) kullanım: "paper anniversary gifts" bir konu, marka değil
- Footer'da net bir ayrışma cümlesi: *"byAliden is not affiliated with Paper Anniversary® by Anna V."*
- Yayına almadan önce USPTO TESS'te (`tmsearch.uspto.gov`) `paper anniversary` araması yap.
  Gerekirse 1 saatlik IP avukatı danışmanlığı en ucuz sigorta.
- Star Seller rozetini ve gerçek yorum sayısını sitede güven öğesi olarak kullan (uydurma yok,
  gerçek rakam + Etsy'ye link).

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

**İkinci ürün ekseni** (aramada byAliden'in `Custom Animated Love Letter / Digital
Anniversary E-card` listing'ini de gördüm — bu ayrı bir keyword kümesi ve ayrı bir
landing page hak ediyor):
- digital anniversary card / animated love letter
- long distance gift for boyfriend / girlfriend
- e-card anniversary gift (instant, no shipping)
- last minute gift for boyfriend (digital)

Bu iki ürün birbirini besler: aynı ziyaretçiye bundle ($8 kart + $18 harita = $22 paket)
satabilirsin ve site tek ürüne bağımlı kalmaz.

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
/love-letter/                       2. ürün: animasyonlu dijital love letter / e-card
  /love-letter/long-distance/
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

## 4.5 Görsel Kimlik — üründen türetilmiş

Siteyi sıfırdan tasarlamıyoruz: **ürünün kendisi zaten güçlü bir görsel dil taşıyor.**
Gönderdiğin mockup'lardan çıkardığım sistem:

| Öğe | Üründeki hali | Sitede karşılığı |
|---|---|---|
| Zemin | Krem/fildişi kâğıt (~`#F5F2EA`) | Site zemini aynı krem — ürün ile site aynı dünyada olsun |
| Çizgi | Koyu antrasit-sepya mürekkep (~`#2B2A26`) | Metin rengi, çizgiler, ikonlar |
| Tipografi | El yazısı büyük harf, geniş harf aralığı ("OUR LOVE MAP") | Başlıkta benzer karakterde display font; gövde temiz sans |
| Motif | **Kıvrılan yol** milestone'ları bağlıyor | "Nasıl çalışır" ve yol haritası bölümlerinde aynı kıvrımlı yol |
| İkon dili | Dağ, çadır, van, yüzük, pati, ev, uçak, "TO BE CONTINUED" tabelası | Site ikonları aynı el çizimi setinden — ürünün ikon sayfası hazır |
| Aksan rengi | Yok, tamamen siyah-beyaz | Sitede tek sıcak aksan (mürekkep kırmızısı) sadece CTA'da |

**Neden önemli:** Ziyaretçi Google'dan gelip siteyi gördükten sonra Etsy'ye tıkladığında
aynı estetikle karşılaşmalı. Kopukluk = güven kaybı = dönüşüm kaybı.

### Gerçek müşteri işi = en güçlü satış kanıtı

Yüklediğin ikinci fotoğraf (*"7 Incredible Years, 1 Year Married — Sam & Paul"*) tek başına
üç şeyi ispatlıyor ve üçü de sitede öne çıkmalı:

1. **Başlık bile kişiselleştirilebiliyor** — "Our Love Map" zorunlu değil. Bu listing'de net
   yazmıyor; sitede yazacağız.
2. **Çiftin kendi portresi çizilebiliyor** — Tower Bridge, gelin-damat, köpek, Disney, uçak.
   Bu, 3 yıldızlı yorumdaki *"cookie cutter"* iddiasının doğrudan çürütücüsü.
3. **Eşleşen tebrik kartı** da mevcut → doğal bir bundle ürünü.

> Aksiyon: `/gallery/` sayfası bu tip **gerçek teslimatlarla** dolacak, stüdyo
> mockup'larıyla değil. Her işin altına: kaç milestone, hangi özel istekler karşılandı.

### İki ayrı hikâye tipi var — bu, iki ayrı sayfa demek
Gönderdiğin mağaza görselleri iki farklı dünyayı gösteriyor ve bu tesadüf değil, **segment**:

| Stil | Örnek | İçerik | Hedef kitle |
|---|---|---|---|
| **Doğa / macera** | Alex & Jordan | Boulder, van life, Mount Rainier, Lake Tahoe, kabin, husky | Outdoor çiftler, "van life", hiking, dağ düğünü |
| **Şehir / seyahat** | Rachel & Ross | NYC kafe, Brooklyn Bridge, Rockefeller, NY Public Library, Eiffel, Louvre, Hamptons | Şehirli çiftler, seyahat severler, uluslararası ilişkiler |

Her ikisi de aynı ürün ama **arama niyeti farklı**. Bu yüzden:
- `/love-map/adventure-couples/` → "hiking couple gift", "van life anniversary gift",
  "mountain wedding anniversary print"
- `/love-map/city-story/` → "new york love story print", "travel couple anniversary gift",
  "long distance international couple gift"

Ayrıca Rachel & Ross örneğindeki *"Emma born, May 2025"* satırı, listing'de hiç
vurgulanmayan bir kapıyı açıyor: **bebek/aile milestone'ları**. Yeni keyword kümesi —
`first anniversary gift for new parents`, `our family story print`, `new baby milestone map`.
Hediye alan kişi çoğu zaman "bizim hikâyemizde bebek de var" diye arıyor.

> Not: Tüm mockup'lar aynı boho/İskandinav iç mekân dünyasında (krem duvar, meşe çerçeve,
> keten kanepe, jüt halı). Site de bu dünyada durmalı — mockup'ları kesip farklı bir
> tasarım diline yapıştırmak ürünü ucuzlatır.

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

> ✅ `AggregateRating` bizde **gerçek**: bu listing 4.9 / 119 yorum, shop 4.9 / 145.
> Yorumları sitede gerçekten göster (metin + tarih + Etsy'ye link), sonra schema'ya yaz.
> Uydurma rakam Google'dan manuel ceza getirir — gerek de yok, gerçeği zaten güçlü.

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

### 7.0 İtiraz haritası — gerçek yorumlardan çıkarıldı

119 yorumu okudum. Sitenin dönüşüm metni **tahminle değil, bu yorumlarla** yazılacak.
Olumsuz iki yorum burada altın değerinde: satın almayan kişinin kafasındaki soruyu
birebir söylüyorlar.

| İtiraz (gerçek yorumdan) | Sitede nasıl karşılanacak |
|---|---|
| *"Aldığım iş listing'deki görselden belirgin farklı, kişiselleştirilmiş hali daha kötü görünüyordu"* (1★) | **En kritik itiraz.** Galeri idealize mockup'larla değil, **gerçek müşteri teslimatlarıyla** dolu olsun. `/gallery/` sayfası: 12-20 gerçek iş, her birinin altında kaç milestone içerdiği. "Listing görseli = örnek, senin işin sana özel çizilir" cümlesi ürün sayfasında açıkça yazsın |
| *"AI is used to make the design"* (3★) | Süreci **dürüstçe** anlat. Hangi adım el çizimi, hangi adım dijital araç? `/how-it-works/` sayfası adım adım göstersin. Gizlemek en kötü seçenek — bu yorum zaten halka açık ve AI bunu okuyor |
| *"Cookie cutter design, istediğim sahneyi (ahır) yaptıramadım, örnek fotoğraf gönderemedim"* (3★) | **Bu iddia diğer yorumlarla çürüyor** — *"able to draw the cabin and house to match how it looks in real life"*, *"Artist was able to match the look of my current house"*, *"adding my dogs and features of my husband and I"*. Demek ki referans fotoğraftan gerçek bina çizilebiliyor; sorun **sürecin nasıl anlatıldığı**. Çözüm: `/how-it-works/` sayfasında "fotoğraf gönderebilirsin" adımı açıkça olsun + kapsam listesi (neyin mümkün olduğu, neyin olmadığı) net yazılsın |
| *"Revizyon sayısı sınırsız değil"* (3★) | Revizyon politikasını sayıyla yaz: *"2 rounds of revisions included."* Belirsizlik hayal kırıklığı üretiyor |
| *"Telefondan kaydedemedim, masaüstü gerekti"* (3★) | `/guides/how-to-download-and-print/` — telefondan indirme dahil, ekran görüntülü rehber. Hem destek yükünü düşürür hem uzun kuyruk trafiği getirir |
| *"İletişim o kadar hızlıydı ki sorulara cevap veremedim"* (3★) | Sipariş öncesi **hazırlık formu**: müşteri siteye gelip milestone'larını rahatça yazsın, Etsy'ye hazır gelsin. Bu aynı zamanda e-posta yakalama noktası |

**Olumlu tarafta sürekli tekrar eden 5 tema** — bunlar sitenin ana satış argümanları olmalı:
1. **Hız:** *"proof back to me within hours"*, *"sketch within 24 hours"*, *"done within 2 business days"*
2. **Esneklik:** *"made all the adjustments I wanted"*, *"added my dogs and features of my husband and I"*
3. **Kişisel ilgi:** *"asked for a picture to get our likeness just right"* — Ali'nin kendisi satış argümanı
4. **Değer:** *"really a steal for a fun, creative anniversary gift"*
5. **Duygusal etki:** *"can't wait for him to open it on our 1 year anniversary"*

### 7.0.1 Doğrulanmış vaatler — 150+ yorumdan çıkarıldı

Bunlar pazarlama cümlesi değil, **müşterilerin kendi yazdığı, kanıtlanabilir** iddialar.
Sitede birebir bu vaatleri veriyoruz; her birinin altında kaynak yorumu gösteriyoruz.

| Vaat | Kanıt |
|---|---|
| **İlk taslak ~24 saat, teslim 2-3 gün** | *"within 2 business days, even after receiving some feedback"* · *"turned this around within 3 days"* · *"purchase on Thursday, by Sunday I already had the downloadable file"* |
| **Acele siparişe yetişilir** | *"Even rushed my order so I could give it in time as a gift!"* |
| **Gerçek binanı fotoğraftan çizeriz** | *"able to draw the cabin and house to match how it looks in real life"* · *"Artist was able to match the look of my current house"* |
| **Evcil hayvan ve çift portresi eklenir** | *"customize by adding my dogs and features of my husband and I"* |
| **Finalden önce sana danışılır** | *"The seller checked in with me before finalizing the product"* · *"helped guide the process from the beginning"* |
| **Baskı ve çerçeveleme rehberi dosyayla birlikte gelir** | *"she sends instructions with recommendations for printing and framing"* |

> 📌 **Bedava içerik fırsatı:** Baskı/çerçeveleme rehberi **zaten var**, sadece müşteriye
> özel gönderiliyor. Onu `/guides/how-to-print-and-frame/` olarak yayınla — sıfır yeni
> emek, uzun kuyruk trafiği + AI alıntısı + destek yükünde düşüş. Bunu bana gönder,
> sayfaya çeviririm.

### 7.0.2 Fark edilmemiş en büyük satış argümanı: **tek dosya, çok kullanım**

Kristen'in yorumu tek başına bir landing page değerinde:

> *"I printed a large copy as decor, small copies for bookmarks and posted it digitally
> on social media."*

Yani $47'lık dosya bir poster değil, **bir varlık**. Ne listing'de ne rakiplerde bu
anlatılıyor. Sitede net bir bölüm olacak — *"One file. Print it big, print it small,
share it online."*
- Büyük baskı → duvar dekoru (A2 / 24x36)
- Küçük baskılar → **yer imi**, tebrik kartı içi, davetiye eki, misafir masası
- Dijital → sosyal medya paylaşımı, telefon duvar kâğıdı, düğün ekranı

Bu, algılanan değeri doğrudan yükseltir ve fiyat itirazını zayıflatır.

### 7.0.3 Yorumlardan çıkan yeni kullanım senaryoları = yeni sayfalar

Yorumlar, listing'in hedeflemediği alıcıları ortaya çıkarıyor. Her biri ayrı landing page:

| Senaryo | Kaynak yorum | Sayfa |
|---|---|---|
| Anne-babaya hediye | *"made a lovely gift for my parents"* | `/love-map/for-parents/` |
| Arkadaşa/aileye düğün hediyesi | *"such a great wedding gift idea for friends/family"* | `/love-map/wedding-gift/` |
| Düğünde misafir masası | *"so cool to have at our wedding for guests to look at"* | `/love-map/wedding-display/` |
| Bridal shower dekoru | *"shower decorations"* | rehber sayfası içinde |
| Nişan duyurusu | *"unique engagement announcement"* | `/love-map/engagement/` |
| Zor beğenene hediye | *"my husband is a graphic designer... will be impressed"* | rehber sayfası içinde |

### 7.0.4 Gözlem: uluslararası talep var, ama şimdilik İngilizce kalıyoruz

Yorumcular arasında İspanyolca yazan (*"Charming manner, a great professional"* — orijinali
İspanyolca), Yunan, Vietnam ve Hollanda kökenli isimler var. Talep tek dilli değil.
**Karar değişmiyor** — Faz 1-3 sadece İngilizce, çünkü tek dilde derinleşmek iki dilde
sığ kalmaktan iyidir. Ama Faz 4'te İspanyolca `/es/` kümesi masada tutulacak; o zamana
kadar hangi dillerden trafik geldiğini GSC'den ölçeriz.


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
| 4-6 ay | Günlük 300-800 ziyaret. **$47 AOV ile günde 30-50 nitelikli ziyaretçi bile aylık ~$2.000 ciro demek** |
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

**Etsy bu ortamda ağ seviyesinde bloklu** (`www.etsy.com` ve `byaliden.etsy.com` ikisi de
egress proxy tarafından reddediliyor). Listing'i kendim okuyamıyorum, o yüzden aşağıdakileri
bana yazman/yüklemen gerekiyor. **Yıldızlı olanlar olmadan başlayamam**, diğerleri sonra
gelebilir.

### Artık elimde olanlar
Listing verisini, 119 yorumu ve ürün görsellerini aldım. Fiyat, format, teslim süresi,
kişiselleştirme akışı, stil, sosyal kanıt ve fiyat merdiveni **çözüldü** (bkz. §0.5).
Bu maddeler artık bloklayıcı değil.

### Bloklayıcı — hâlâ sende
1. ⭐ **Domain:** PaperAnniversaryGift.com alındı mı? DNS nerede? Cloudflare'a taşımamız
   gerekiyor. Bu olmadan hiçbir şey yayına giremez.
2. ⭐ **Görsel paketi.** Yükleyebileceğini söyledin — öncelik sırasıyla:
   - **6-10 gerçek müşteri işi** (Sam & Paul gibi). `/gallery/` sayfasının tamamı buna
     dayanıyor. İsim/tarih hassassa kısmen bulanıklaştırırız, ama gerçek iş olsun
   - Ana mockup'ın tam çözünürlüklü hali (Alex & Jordan) — hero görseli
   - **İkon seti** görseli — "neler mümkün" bölümü için
   - "Nasıl sipariş verilir" 3 adım görseli
   - Yakın çekim doku/detay fotoğrafı — baskı kalitesi kanıtı
   - Varsa **eşleşen tebrik kartı** görselleri — bundle sayfası için
3. ⭐ **Personalized Website ürünü ($30.90):** müşteri tam olarak ne alıyor? Kendi alt alan
   adı mı, dosya mı? Ne kadar süre yayında kalıyor? Canlı demo kurmak istiyorum (§0.5)


### Önemli ama sonra gelebilir
5. **Yorumlar:** toplam sayı, ortalama puan, 3-4 alıntılanabilir yorum metni
   (Star Seller rozetini de kullanacağız)
6. **Diğer listing'lerin:** aramada `Custom Animated Love Letter / Digital Anniversary
   E-card` listing'ini gördüm. Tüm aktif ürünlerin listesi lazım — her biri ayrı landing
   page ve bundle stratejisi demek
7. **Yazar kimliği (E-E-A-T):** sitede gerçek isim + foto + kısa hikâye kullanabilir miyiz?
   ("Bu haritayı ilk olarak kendi yıldönümümüz için tasarladım..." tipi gerçek hikâye
   dönüşümü ciddi artırıyor ve Google'ın E-E-A-T sinyali için önemli)
8. **Bütçe:** anket ($150-300), AI görünürlük takip aracı ($50-100/ay), Pinterest
   zamanlayıcı — hangilerine açıksın? **Hepsi opsiyonel, sıfır bütçeyle de başlanır**
9. **Zaman:** haftada kaç saat ayırabilirsin? (outreach ve Pinterest senin elinle olmalı,
   kod ve içerik bende)

### Karar vermen gerekenler
10. **Marka adı:** önerim **byAliden** (§1.4'teki gerekçe). Onaylıyor musun?
11. **Kendi satış kanalı:** uzun vadede Gumroad/Lemon Squeezy ile Etsy komisyonunu kesmek
    istiyor musun, yoksa Etsy'de mi kalalım?

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
