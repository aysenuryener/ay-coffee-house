# Ay Coffee House — Web & Marka Paketi

Premium kahve evi. Espresso kahve tonları + sıcak tan aksan (#B48A55),
lüks serif başlık + SF Pro/Neue Haas hissi gövde. **Google Fonts kullanılmaz**
(cihazdaki premium fontlar + isteğe bağlı self-host). Çok dilli: **TR / EN / AR**
(Arapça RTL). Menüde yeni yönetmelik gereği **kalori (kcal)** bilgisi.

## Dosyalar
- `index.html` — Ana site (TR/EN/AR, gerçek fotoğraflar, kalori menü).
- `menu.html` — Dijital menü + QR hedefi (TR/EN/AR, kalori).
- `qr.html` — Masa QR kartı (gerçek QR'ı yuvaya koy, yazdır).
- `social-kit.html` — Instagram profil/story/feed/highlight şablonları.
- `stationery.html` — Kartvizit, sadakat/hediye kartı, antetli kâğıt, zarf.
- `images/` — 16 görsel yerleştirildi (bkz. images/README.txt).

## Çalıştırma
```bash
cd ay-coffee-house
python3 -m http.server 5173   # http://localhost:5173
```
Ya da index.html'e çift tıkla.

## Deploy (Vercel)
```bash
git init && git add . && git commit -m "Ay Coffee House"
vercel        # veya vercel.com'dan repoyu içe aktar
```
Statik site — ekstra ayar yok.

## Fontlar (Google Fonts YOK)
Başlıklar: **Cormorant** (500) · Gövde/nav/buton/etiket: **Inter** (400/500).
Bunny Fonts üzerinden yükleniyor (Google değil): `fonts.bunny.net`. İnternet
bağlantısı olduğu sürece ekstra kurulum gerekmez; tamamen çevrimdışı çalışması
gerekirse woff2 dosyalarını `fonts/` klasörüne indirip @font-face ile bağlarım.

## Renkler (WCAG AA doğrulanmış)
Ana başlık #3E3027 (11.6:1) · menü adı #4A3A2F (10.4:1) · gövde #7A6C61 (4.6:1)
· muted #7B6D62 (4.55:1) · fiyat/aksan metin #926D3C (4.5:1) · dekoratif altın çizgi #B48A55
· zemin #F8F4ED / #F3EEE5 · kart #FCFAF7 · aktif buton #4A3A2F/beyaz (10.8:1)
· pasif buton metin #5E4C40 (7.8:1), kenarlık #DCCFBE.
Tüm oranlar WCAG AA (4.5:1) eşiğini geçer; python ile hesaplanıp doğrulanmıştır.
