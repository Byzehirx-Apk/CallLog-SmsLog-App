# CallLog-SmsLog-App
Sms Log Call Log Apk App
Forensic IT Services App 

Kullanımı ve Çalışma Prensibi

Detaylı Anlatım

Uygulama 1 veya birden fazla amacı karşılamak üzere tasarlanmıştır. 

Ben Size A,B ve C Bölüm ile Detayları Anlatayım 

A.Bölümü 

SMS Mesaj Verileri

SMS Mesaj Liste/Düzen

SMS Mesaj İzni Yorumu 

Terminal özelliği 

Android SQLite SDKManager

Özel terminal komutları

A/Bölümüne giriş ‼️

1. SMS inbox "Özelliği"

Bu eylem butonu "//sms/inbox" cihaz içerisinde bulunan tüm gelen "inbox"  mesajları cihaz ...databases/mmssms.db dâhili hafızası deposundan çeker. 

SMS inbox 

SMS Hizmet Servisini çağrır 

Hizmetin çalışma prensibi (READ_SMS) İzinine ihtiyaç duyar. (Dangerous)☢️

2. SMS send "Özelliği"

Bu eylem butonu "//sms/send" cihaz içerisinde bulunan tüm gönderilen "send) mesajları cihaz ...databases/mmssms.db dâhili hafızası deposundan çeker. 

SMS send

SMS Hizmet Servisini çağrır 

Hizmetin çalışma prensibi (READ_SMS) İzinine ihtiyaç duyar. (Dangerous)☢️

Özet: SMS inbox ve SMS send çalışma prensipleri aynı amaca hizmet ediyor. 

3. SMS/List "Eylemi"

SMS/List Butonu [SMS inbox ve SMS send] 2 özelliğe hizmet eden düzenleyici 

SMS inbox veya SMS send kullanıldığında ekrana gelen veriyi listelemek veriyi ayrıştırmak için kullanılır. 

Bilgilendirme: (?)

Android "Manage a SQLite Database" özelliğini geliştirilerek tüm veriyi çeşitli veritabanı hizmetleri kullanarak sistem içerisinde saklar bunlardan en yaygını "db" SQLite Database    

Öyle sanıldığı gibi text "txt" dosyasında saklanmıyor veriler

/data/user_de/0/com.android/providers.telephony/databases/mmssms.db buradaki veriyi ROOT izni olmadan çekmek veriyi okunaklı anlaşılır şekilde ayrıştırmak için özel bir "JsonTextDecode"Java kullanarak (JSON) formatı kullanılmıştır. "SMS/List" butonu JSON çalıştırarak veriyi düzenler.

//SMS inbox, SMS send ve SMS/List aynı amaca hizmet ediyor. 

Not: 

1) Gelen/alınan mesajları çekebilmek için "//sms/inbox" komutu yazılmak zorundadır.

2) Gönderilen/iletilen mesajları çekebilmek için "//sms/send" komutu yazılmak zorundadır.//

 4. Terminal Command "özelliği"  

>Run (red button) buton işlevi

Android SDK Platform-Tools paketine dahildir 

Bilinen Linux Terminal Komut çalıştırıcısı

SDKManager hizmetini tetiklemek komut girişi ile servis veya hizmet çalıştırmak "SMS inbox ve SMS send" butonları özel yazılan komutlar 1."//sms/inbox" 2."//sms/send" komutlarımızı çalıştırmak için aracı olan ana hizmet yapı mimarisidir. 

Aynı zamanda "logcat" gibi verileri ve birden fazla komut çalıştırabilen "ROOTSUZ" modifiye edilmiş Terminaldir. 

B.Bölümü

READ_SMS

READ_CALL_LOG

Arama Geçmişi

Verileri Sdcard Saydetmek

Tehlikeli/Risk

 B/Bölümüne giriş 

 1. SMS.db izni "özelliği" 

SMS.db izni butonu ile SMS Mesaj erişimine izin verilir.

android.permission.READ_SMS 🚫

2. CallLog.db izni "özelliği"  

CallLog.db izni butonu ile CallLog Arama kaydı erişimine izin verilir.

android.permission.READ_CALL_LOG 🚫

UYARI: İstenilen izinler risklidir ve tehlikeli.

Bkz Referans http://androidpermissions.com/

Bkz Referans https://developer.android.com/.../permissions/overview

Android'in kullanmak için izninizi gerektirdiği "tehlikeli" izinlerdir.  Bu "tehlikeli" izinler, arama geçmişinize, özel mesajlarınıza, konumunuza, kameranıza, mikrofonunuza ve daha fazlasına erişimi içerir. www.avg.com sitesinden alıntı.

3. Verileri kaydet "Eylemi"

Verileri kaydet butonu ile ekran'da görülen tüm veri olduğu gibi ( Sdcard ) "//Android/data/paketismi/file" içerisine txt dosyası olarak kayıt edilir. 

Kayıt esnasında örn: /dosyaismi.txt olarak "/" başta olmalı ismi yazıp sonuna ".txt" yazılmalıdır. 

Terminal Command 

>Run {red button} özelliği ile kayıt edilen dosya ismi örn: /dosyaismi.txt yazıldığında kayıt ekrana gelir. 

4. CallLog history "özelliği"

CallLog history butonu cihaz içerisindeki tüm arama kayıtlarını ekrana yansıtır 

CallLog Hizmet Servisini çağrır 

Hizmetin çalışma prensibi (READ_CALL_LOG) İzinine ihtiyaç duyar. (Dangerous) 

CallLog history özelliği için (SMS/List) düzenleyici kullanılmamalıdır CallLog history için ayrı javakodu yazılıp entegre edilmiştir. 

CallLog history verisi içinde (Verileri kaydet) kullanılabilir. kayıt yolu "//Android/data/paketismi/file"

5. Telegram App 

Benimle telegram üzerinden irtibata geçmek için 

İletişim kanalıdır.

C.Bölümü son

1)Delete 2)Kapat 3)Uyg_sıfrla 4)Title 5)Devlp

Ayarlar bölümüne erişmek için (Terminal Command) "//app/set" komutu yazılıp >Run {red button} tetiklenmelidir.

1. Delete "Eylemi"

Delete butonu ile "Title ve Developer"  Ekran üste görülen ve okunan  İngilizce yazılan Uygulama Başlığı/Açıklaması ve Developer sonrası nick "By ZehirX" yazılarını siler/delete.

2. Kapat "Eylemi" 

Kapat butonu sizi yanıltmasın uygulamayı kapatmaz sadece ayarlar bölümünü kapatır. 

3. Uyg_sıfırla "Eylemi" 

Uyg_sıfırla butonu ile yapılan işlem 

Uygulama içerisinde verilen izinler (Permissions)

Uygulama ile Sdcard içerisine kayıt edilen veriler (txt) dosyaları

Ve Uygulama içerisinde yapılan değişiklikler ayarlar kompile Reset/Sıfırlanır. Bu işlem Tavsiye edilir çünkü hata veya durduruldu uyarıları alındığında kullanılmalıdır. 

4. Title "Eylemi" 

Title butonu isminden anlaşılacağı üzere (BAŞLIK) istenilen kendi özel başlığınız veya açıklamanızı yazabilirsiniz. 

Ek Not: HTML komutları kullanarak dah güzel ve hoş yazılar yazabilirsiniz.

//Örn

<p> Merhaba! Bu paragraf yazısıdır </p>

<b> Merhaba! Bu kalın yazıdır </b> 

<u>Merhaba! Bu altı çizili yazıdır</u>

     <h1>Başlık Yazısı H1</h1> 

    <h2>Başlık Yazısı H2</h2>

    <h3>Başlık Yazısı H3</h3>

5. Devlp "Eylemi" 

Devlp butonu ile Developer ismi/nicki değiştirilebilir şuan benim nickim "Bu ZehirX" yazıyor bunun yerine kendi nickini yazabilir ve Uygulamayı kendi nickinle kullanabilirsin.

Bu uygulama https://developer.android.com/ sitesi tarafından "Dangerous"☢️  Tehlikeli izinler listesinde bulunan 

2 İzine ihtiyaç duyar 

1 ) android.permission.READ_SMS 🚫

metin mesajlarınızı okuyun (SMS veya MMS)

Uygulamaya, telefonunuzda veya SIM kartınızda saklanan SMS mesajlarını okuma izni verir. Bu, uygulamanın içerik veya gizlilikten bağımsız olarak tüm SMS mesajlarını okumasını sağlar.

Bkz Referans http://androidpermissions.com/permission/android.permission.READ_SMS

2 ) android.permission.READ_CALL_LOG 🚫

arama kaydını oku

Uygulamaya, gelen ve giden aramalarla ilgili veriler de dahil olmak üzere telefonunuzun arama kaydını okuma izni verir. Bu izin, uygulamaların arama günlüğü verilerinizi kaydetmesine olanak tanır ve kötü amaçlı uygulamalar, sizin haberiniz olmadan arama günlüğü verilerini paylaşabilir.

Bkz Referans http://androidpermissions.com/permission/android.permission.READ_CALL_LOG

Yorum:

Bu 2 (Permission) İzin uygulamalar tarafından kullanılmasını önlemek adına Google  güvenlik uygulamaları ve "Play Protect" AppStore tarafından güvenlik riski olarak tespit edilmesi sonucunda (READ_SMS, READ_CALL_LOG) izinlerini kullanan  Uygulamanın yüklenmesi veya yüklü uygulamalar listesinden kaldırılmasını "Kırmızı" Uyarı bildirimi ile kullanıcıyı ikaz etmektedir.

