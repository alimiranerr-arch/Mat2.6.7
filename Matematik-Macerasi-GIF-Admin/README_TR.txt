MATEMATİK MACERASI – HELPY GIF EKLENTİSİ

İçerik:
- index.html: Yüklenen HTML'e Helpy duyuru kontrolleri ve ziyaretçi duyuru katmanı eklendi.
- assets/: Gönderdiğin GIF/WebP/JPG görselleri.
- js/helpy-notices.js: Bakım, önemli çalışma ve büyük teknik sorun duyuruları.
- css/app.css: Son gönderdiğin app.css dosyası; Helpy duyuru stilleri eklendi.
- icons/: Son gönderdiğin SVG ve 96/192/512 px PNG uygulama ikonları.
- manifest.webmanifest: İkon yolları /icons/ klasörüne işaret eden manifest.

KURULUM
1. ZIP'i çıkar.
2. İçindeki dosyaları Netlify sitenin yayın kök dizinine yükle.
3. /assets/ ve /js/ klasörleri index.html ile aynı seviyede kalmalı.
4. Admin girişi yapıp Admin > Sistem & Özellik Kontrol Merkezi > Helpy bölümünden duyuruyu aç.

ÖNEMLİ SINIRLAMA
Yüklenen HTML, şu dosyaları çağırıyor fakat bunlar bu sohbette verilmedi:
 /vendor/qrcode.js
 /js/fixtures.js
 /js/core.js
 /js/sync.js
 /js/game.js
 /js/features.js
 /js/social.js
 /js/admin.js
 /js/hako_extensions.js

README ve kontrol raporu da bu eksikliği doğruluyor. Bu nedenle bu eklenti, orijinal oyun kodunun tüm çalışma zamanı davranışlarını veya admin giriş sistemini denetleyemez.

Ayrıca bu ZIP'e ortak sunucu ayarı/backend eklenmedi. Admin panelinden kaydedilen duyuru durumu yalnızca aynı tarayıcıdaki localStorage içinde tutulur. Başka cihazlardaki ziyaretçilere küresel yayın yapmak için sunucu tarafında ortak ayar API'si ve güvenli admin yetkilendirmesi gerekir. İstemci tarafındaki localStorage ayarı güvenlik sınırı değildir. Admin istisnası da mevcut uygulamanın #adminOpen ve #tabAdmin görünürlük durumuna dayanır; sunucu tarafı güvenlik sağlamaz.

GÖRSEL DAVRANIŞI
- Büyük teknik sorun: Helpy teknik onarım GIF'i.
- Bakım molası: seçilen bakım GIF'i.
- Önemli işlem: seçilen Helpy görseli.
- Bakım ve büyük sorun ekranları kapatılamaz; önemli işlem duyurusu kapatılabilir.

GÜVENLİK
Öğrenci hesapları, sohbetler, e-posta ve konum gibi verileri etkileyen backend kodları bu pakette bulunmadığından güvenlik açığı taraması tam olarak yapılamadı. Bu ZIP, sunucu güvenliği veya kimlik doğrulama düzeltmesi iddia etmez.

DOSYA BİÇİMİ NOTU
Gönderdiğin “Bakım Molası (1).gif” dosyasının içeriği teknik olarak tek kare PNG biçiminde; pakette doğru MIME türüyle bakim-molasi.png olarak saklandı. VentRepair görseli ise gerçek, 11 karelik animasyonlu GIF.
