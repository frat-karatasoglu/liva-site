# Liva Pastane & Çerez

Kovancılar / Elazığ'daki Liva Pastane & Çerez için tanıtım sitesi. Saf HTML, CSS ve biraz JavaScript; derleme adımı yok.

## Yapı

| Dosya | Ne işe yarar |
| --- | --- |
| `index.html` | Ana sayfa (giriş animasyonu, tatlılar, kuruyemiş, mekân, iletişim) |
| `menu.html` | Salon menüsü (masada yenilebilen ürünler) |
| `style.css` | Tüm stiller |
| `img/` | Fotoğraflar ve sekme simgesi |
| `firebase.json` | Firebase Hosting ayarı |

## Yerelde önizleme

```bash
python -m http.server 8000
```

Sonra tarayıcıda `http://localhost:8000` adresini aç.

## Firebase Hosting ile yayın

```bash
npm install -g firebase-tools
firebase login
firebase use --add        # Firebase projesini seç
firebase deploy --only hosting
```

`firebase.json` içinde `public` klasörü depo kökü olarak ayarlı; `README.md` ve dosya adı `.` ile başlayanlar yayına girmez.

## Notlar

- **Animasyonlar:** Sistem "hareketi azalt" derse açılış animasyonu ve diğer hareketler atlanır. Adresin sonuna `?animasyon=1` eklenirse o tarayıcıda oynar, `?animasyon=0` geri alır.
- **Açılışı oturumda bir kez oynatmak:** `index.html` içindeki `ONCE = false` satırını `true` yap.
- **Menü:** Ürünler işletmenin FKPOS ürün listesinden, yalnızca masada tüketilebilen ana ürünler olarak seçildi. Fiyat yok.
- **Bilgiler:** Adres, telefon ve Instagram Google Haritalar kaydından ve işletmenin Instagram hesabından alındı. Çalışma saatleri eklenmedi.
- **Yazı tipleri:** Google Fonts (Gloock, Hanken Grotesk, Norican). Çalışması için internet gerekir.
