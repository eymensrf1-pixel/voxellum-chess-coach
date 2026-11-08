# VOXELLUM Chess Coach (ilk web sürümü)

## Özellikler
- Chess.com kullanıcı adıyla herkese açık profil ve istatistikleri getirir.
- Son aylardaki maçları listeler; PGN dosyası kullanıcı cihazına indirilmez.
- Maç hamlelerini tahtada gezdirir.
- Stockfish 19 Lite Single ile tarayıcı içinde analiz yapar.
- Derinlik seçimi ve seçili pozisyon için en iyi 3 hamle.

## Çalıştırma
Bu proje statik web uygulamasıdır. `index.html`, `manifest.webmanifest` ve `sw.js` dosyalarını HTTPS destekleyen statik bir web barındırıcısına aynı klasör yapısıyla yükleyin. `file://` üzerinden açmayın; modül, Worker ve PWA özellikleri için HTTP(S) gerekir.

Android telefonda Chrome ile siteni açıp tarayıcı menüsünden **Ana ekrana ekle** seçeneğini kullanabilirsin.

## Önemli
- Chess.com Published Data API herkese açık, salt okunur bir API'dir. İstekler seri gönderilir; API 12 saate kadar önbellek kullanabilir ve yoğun paralel istekler 429 sınırına takılabilir.
- Bazı ağ/tarayıcı koşullarında Chess.com API CORS veya istek sınırı nedeniyle erişilemeyebilir.
- Stockfish ilk analizde yaklaşık 1.7 MB'lık motor dosyalarını CDN'den yükler; motorun JS ve WASM dosyaları aynı klasör yolundan sunulmalıdır.
- İlk sürümde analiz derinliği 8-14 aralığındadır. Telefonun ısınmasını veya yavaşlamasını önlemek için kısa aralar verin.
- Hata sınıflandırması değerlendirme kaybına dayalı yaklaşık bir sınıflandırmadır; Chess.com'un kendi Game Review etiketleri değildir.
- Bu bağımsız proje Chess.com ile bağlantılı veya onun tarafından onaylanmış değildir.
- Stockfish.js GPL-3.0 lisanslıdır; dağıtım yaparken ilgili lisans ve kaynak bildirimlerini koruyun.
