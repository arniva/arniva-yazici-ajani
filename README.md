# Arniva Yazıcı Ajanı — Kurulum

Arniva Yazıcı Ajanı, Arniva Cloud'daki raporları ve etiketleri tarayıcının yazdırma penceresiyle
uğraşmadan, tek tıkla bilgisayarınıza bağlı yazıcıya (A4 lazer, termal fiş, etiket yazıcısı)
gönderir. Yazdırma yapılacak her bilgisayara bir kez kurulur.

Gereksinim: Windows 10 ya da 11 (64 bit), Chrome, Edge ya da Firefox'un güncel sürümü.

## 1. Kurulum

1. Arniva Cloud'da bir raporu açın, **Yazdır** düğmesinin yanındaki oktan **Yazıcıya gönder…**
   seçin ve **Kurulumu indir**'e tıklayın. (Doğrudan indirme:
   <https://github.com/arniva/arniva-yazici-ajani/releases/latest/download/ArnivaYaziciAjani-win-Setup.exe>)
2. İnen `ArnivaYaziciAjani-win-Setup.exe` dosyasını çalıştırın. Yönetici yetkisi gerekmez.
   Yayıncı **ARNİVA YAZILIM İTHALAT İHRACAT TİCARET A.Ş.** olarak görünmelidir. Windows "Windows
   bilgisayarınızı korudu" derse **Ek bilgi** → **Yine de çalıştır**'ı seçin.
3. Kurulum bitince saatin yanındaki simge alanında mavi yazıcı simgesi görünür. Ajan her oturum
   açılışında kendiliğinden başlar ve yeni sürümleri kendisi yükler.

## 2. İlk eşleştirme (her tarayıcıda bir kez)

1. Arniva Cloud'da **Yazdır** → **Yazıcıya gönder…** → **Eşleştir**'e tıklayın.
2. Tarayıcı "**Bu cihazdaki uygulamalar**a erişmek istiyor" diye sorarsa **İzin ver**'i seçin.
3. Ekranda Windows'un kendi penceresi açılır: "https://app.arniva.cloud bu bilgisayardaki
   yazıcılara belge göndermek istiyor". **Evet**'i seçin. Pencere görev çubuğunda yanıp sönüyor
   olabilir.
4. Pencere "Yazıcı ajanı hazır" der; yazıcılarınız listelenir.

## 3. Yazdırma

- Yazıcıyı, kopya sayısını ve gerekirse tepsiyi seçip **Yazdır**'a basın.
- **Bu rapor için bu bilgisayarda hatırla** işaretlenirse o raporda bir sonraki **Yazdır**
  (ya da Alt + Z) hiçbir şey sormadan aynı yazıcıya gönderir.
- Rapor listesinde sağ tık → **Yazıcıya gönder…** raporu açmadan basar.
- Yeni bir yazıcıyı denemek için **Test sayfası**: yazıcı adı, kâğıt boyu ve 50 mm'lik bir
  ölçek çizgisi basılır (cetvelle 50 mm çıkmalıdır).

## Sorun giderme

| Belirti | Çözüm |
|---|---|
| "Yazıcı ajanına ulaşılamadı" | Simge alanında mavi yazıcı simgesi var mı bakın; yoksa Başlat menüsünden **Arniva Yazıcı Ajanı**'nı açın. Kurulu değilse 1. adım. |
| "Tarayıcı izni engellendi" | Adres çubuğundaki kilit simgesi → Site ayarları → **Bu cihazdaki uygulamalar** (ya da "Yerel ağ erişimi") → **İzin ver**, sonra sayfayı yenileyin. |
| Onay penceresi görünmüyor | Görev çubuğunda yanıp sönen pencereye tıklayın. 60 saniyede yanıtlanmazsa kapanır; **Eşleştir**'e yeniden basın. |
| "Eşleştirme reddedildi" | Yanlışlıkla **Hayır** dendiyse **Eşleştir**'e yeniden basıp **Evet**'i seçin. |
| Yazıcı listede yok | Yazıcı Windows'ta kurulu ve açık olmalı (Ayarlar → Yazıcılar ve tarayıcılar). Pencerede yenile düğmesine basın. |
| Fiş kenarları kesik ya da kaymış | Test sayfasını basın; 50 mm çizgi doğru değilse yazıcı sürücüsünün kâğıt ayarını denetleyin. Raporun içeriği kâğıt kenarından en az 4 mm içeride olmalıdır (80 mm rulonun basılabilir alanı 72 mm'dir). |
| "Yazıcı ajanı eski" | Ajan kendini günceller; hemen güncellemek için simge → **Çıkış**, sonra Başlat menüsünden yeniden açın ya da kurulumu yeniden indirin. |

Destek için: simge → **Günlüğü aç**. Günlük, hangi siteden hangi yazıcıya kaç sayfa
gönderildiğini gösterir (belge içeriği yazılmaz).

## Kaldırma ve izinler

- İzni geri almak: simge → **Eşleşmiş siteleri kaldır**.
- Oturum açılışında başlamasın: simge → **Windows açılışında başlat** işaretini kaldırın.
- Kaldırmak: Windows Ayarlar → Uygulamalar → **Arniva Yazıcı Ajanı** → Kaldır.

## Kurumsal kurulum (BT yöneticileri için)

- Ajan yalnız bu bilgisayarın içinden (`127.0.0.1:41967`) bağlantı kabul eder; yerel ağa açık
  değildir, güvenlik duvarı kuralı gerekmez.
- Tarayıcı izin sorusunu önceden vermek için Chrome/Edge ilkesi
  `LocalNetworkAccessAllowedForUrls` = `https://app.arniva.cloud`.
