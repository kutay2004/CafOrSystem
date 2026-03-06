# CafOrSystem - Kafe Yönetim Sistemi

Bu proje, bir kafenin ürün, kategori, çalışan ve müşteri yönetimini dijitalleştirmek amacıyla geliştirilmiş modern bir Blazor Web App uygulamasıdır.

## Özellikler
- Ürün Yönetimi: Menüdeki ürünlerin eklenmesi, güncellenmesi ve silinmesi
- Kategori Sistemi: Ürünlerin kategorilere göre gruplandırılması ve ilişkisel veri takibi
- Görsel Ana Sayfa: Kullanıcıyı karşılayan pasta ve kahve temalı içerik
- İlişkisel Veritabanı: Tablolar arası Foreign Key ilişkileri ve EF Core ile veri yönetimi
- Örnek Veri: SQL script içinde örnek kategori/ürün/müşteri/çalışan/sipariş verileri mevcuttur

## Kullanılan Teknolojiler
- Framework: .NET 8 / Blazor Web App
- ORM: Entity Framework Core (Database-First)
- Veritabanı: Microsoft SQL Server

## Kurulum ve Çalıştırma

### 1) Proje dosyalarını açma
Bu repo içinde proje dosyaları zip olarak bulunur:
- `Caf-Orzip.zip` dosyasını indirin
- Zip’i Extract edin
- Extract edilen klasördeki `CMPE232.sln` dosyasını Visual Studio ile açın

### 2) Veritabanı Yapılandırması
1. SQL Server üzerinde `CafOrSystem` adında bir veritabanı oluşturun.
2. Proje klasörü/ZIP içinde bulunan `Caforsql.sql` dosyasını SSMS ile açın.
3. Script’i çalıştırarak tabloları ve örnek verileri oluşturun.

### 3) Bağlantı Ayarları (Connection String)
`SengWeb/appsettings.json` ve/veya `SengWeb/appsettings.Development.json` içinde bağlantı dizesini kendi bilgisayarınıza göre güncelleyin.

Örnek:
```json
"ConnectionStrings": {
  "SengWebContext": "Server=DESKTOP-PQ9II1K\\SQLEXPRESS;Database=CafOrSystem;Trusted_Connection=True;MultipleActiveResultSets=true;TrustServerCertificate=True;"
}

Notlar:

Server=...\\SQLEXPRESS kısmı bilgisayardan bilgisayara değişir.

SQL Server instance adınız farklıysa ona göre düzenleyin (ör: localhost\\SQLEXPRESS).

4) Projeyi Çalıştırma

Visual Studio’da CMPE232.sln dosyasını açın.

Build > Rebuild Solution

F5 ile uygulamayı başlatın.

Startup project olarak SengWeb seçili olmalıdır.

Sunum / Açıklama Notları

Data Connectivity: Veritabanına bağlantı ConnectionStrings -> SengWebContext üzerinden sağlanır.

SQL Script: Caforsql.sql hem schema’yı hem de örnek verileri içerir.
