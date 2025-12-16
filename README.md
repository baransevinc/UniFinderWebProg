# UniFinder

UniFinder, üniversite öğrencilerinin birbirleriyle iletişim kurmasını ve yeni sosyal bağlantılar oluşturmasını amaçlayan bir web uygulamasıdır.  
Uygulama, **ASP.NET Core Razor Pages (.NET 8)** altyapısı kullanılarak geliştirilmiştir.

## Özellikler

- **Kullanıcı Hesapları:** Güvenli kayıt olma ve giriş yapma sistemi
- **Profil Düzenleme:** Üniversite, şehir, ilgi alanları ve profil fotoğrafı bilgilerini güncelleme
- **Eşleşme Mekanizması:** Ortak üniversite veya ilgi alanlarına göre kullanıcı eşleştirme
- **Mesajlaşma:** Eşleşen kullanıcılar arasında anlık sohbet imkânı
- **E-posta Bildirimleri:** Gmail SMTP üzerinden e-posta gönderimi
- **Duyarlı Arayüz:** Mobil ve masaüstü cihazlara uyumlu tasarım

## Kullanılan Teknolojiler

- ASP.NET Core Razor Pages (.NET 8)
- Entity Framework Core (SQL Server)
- SMTP (Gmail)
- HTML, CSS ve JavaScript

## Kurulum

### Gereksinimler

- .NET 8 SDK
- SQL Server
- Visual Studio 2022 veya üzeri

### Veritabanı Yapılandırması

`appsettings.json` dosyasında yer alan `DefaultConnection` ayarını kendi SQL Server bilgilerinizle güncelleyin.

Örnek bağlantı tanımı:

```json
"ConnectionStrings": {
  "DefaultConnection": "Server=SUNUCU_ADI;Database=UniFinder;Trusted_Connection=True;TrustServerCertificate=True"
}
Veritabanı Migrasyonları
Projeye ait migration işlemlerini çalıştırarak veritabanını oluşturun.

E-posta Ayarları
E-posta gönderimi için appsettings.json dosyasındaki MailSettings bölümünü kendi SMTP bilgilerinizle doldurun.

Örnek yapılandırma:

json
Kodu kopyala
"MailSettings": {
  "Mail": "mailadresiniz@gmail.com",
  "DisplayName": "UniFinder",
  "Password": "uygulama-sifresi",
  "Host": "smtp.gmail.com",
  "Port": 587
}
Uygulamayı Çalıştırma
Projeyi Visual Studio üzerinden başlatın ve tarayıcıdan aşağıdaki adrese gidin:

arduino
Kodu kopyala
https://localhost:5001
Kullanım
Kayıt Olma: Yeni bir kullanıcı hesabı oluşturun

Profil Güncelleme: Kişisel bilgilerinizi ve ilgi alanlarınızı düzenleyin

Eşleşmeler: Diğer öğrencilerle eşleşmeleri görüntüleyin

Sohbet: Eşleştiğiniz kullanıcılarla mesajlaşın

Proje Yapısı
UniFinderWebProg/ – Ana Razor Pages projesi

Controllers/ – İsteklerin ve iş mantığının yönetildiği katman

Views/ – Razor Pages dosyaları

wwwroot/ – CSS, JavaScript ve görseller

appsettings.json – Uygulama yapılandırmaları

Güvenlik
Şifreler ve hassas bilgiler kaynak kod içinde tutulmamalıdır

Gerçek ortamda User Secrets veya ortam değişkenleri kullanılması önerilir

Katkı
Projeye katkı sağlamak için issue açabilir veya pull request gönderebilirsiniz.

Lisans
Bu proje MIT lisansı ile lisanslanmıştır.
