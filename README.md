# e-commerce-bug-control-basic-
NUnit ile E-Ticaret Hata (Bug) Yakalama ve Test Otomasyonu Projesi.
# E-Ticaret Test Otomasyonu ve Kalite Projesi

Bu proje, **Pîrî Reis Üniversitesi** Bilgisayar Programcılığı programı kapsamında, **MTH2005 Yazılım Test ve Kalitesi** dersi vize ödevi olarak geliştirilmiştir.

**Öğrenci:** Mehmet Akif Ayrılmaz 
**Eğitmen:** Emrah SARIÇİÇEK  
**Tarih:** 29 Nisan 2026

## 1. Proje Neyi Simüle Ediyor?
Bu uygulama, bir e-ticaret sisteminin arka plan (backend) işleyişini simüle eder. Görsel bir arayüz yerine, C# kod seviyesinde şu adımlar gerçekleştirilir:
* **Ürün Yönetimi (`Product.cs`):** Ürünlerin adı, fiyatı ve stok bilgileriyle tanımlanması.
* **Sepet İşlemleri (`Cart.cs`):** Kullanıcının seçtiği ürünleri sepete eklemesi, silmesi ve sepetin toplam tutarını hesaplaması.
* **Sipariş Süreci (`OrderService.cs`):** Sepetteki ürünlerin stok kontrolünün yapılması ve siparişin onaylanması.

Not: Sistem, "Yazılım Kalite" ve "QA" test süreçlerini deneyimlemek amacıyla bilerek mantıksal hatalar (bug'lar) içerecek şekilde tasarlanmıştır.

## 2. Testler Nasıl Çalıştırılır?
Projeyi kendi bilgisayarınızda test etmek için şu adımları izleyebilirsiniz:
1. Projeyi **Visual Studio 2022** ile açın.
2. Üst menüden **Test > Test Gezgini (Test Explorer)** penceresini açın.
3. Sol üstteki **Tümünü Çalıştır (Run All)** butonuna basın.


## 3. Uygulanan Test Metotları
Projede, NUnit kütüphanesi kullanılarak `ECommerceTests.cs` dosyası içerisinde 4 farklı test türü simüle edilmiştir:
* **White Box (Birim Test):** Kodun iç yapısı bilinerek değişkenlerin kontrolü.
* **Black Box (Kara Kutu):** Sistemin içi bilinmeden sadece girdi/çıktı kontrolü.
* **Gray Box (Gri Kutu):** Hem kullanıcı eylemi hem de arka plandaki listenin (RAM) durumu.
* **Integration (Entegrasyon):** Sepet (`Cart`) ve Sipariş (`OrderService`) modüllerinin beraber çalışabilirliği.
