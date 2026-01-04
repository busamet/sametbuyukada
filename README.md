# Akademik Site - GitHub Pages Kurulum Rehberi

Bu rehber, hazırlanan akademik web sitesini GitHub Pages üzerinden yayınlamak için gereken adımları açıklamaktadır.

## Dosya Yapısı

```
academic-site/
├── index.html          # Ana sayfa
├── publications.html   # Yayınlar sayfası
├── resources.html      # Kaynaklar sayfası
├── contact.html        # İletişim sayfası
├── style.css           # Stil dosyası
├── script.js           # JavaScript dosyası
├── files/              # İndirilebilir dosyalar (oluşturmanız gerekiyor)
│   ├── docentlik-hesaplama.xlsx
│   ├── modal-mantik-egitim.pdf
│   └── ...
└── README.md           # Bu dosya
```

## GitHub Pages Kurulumu

### Adım 1: GitHub Hesabı Oluşturma
Eğer yoksa, [github.com](https://github.com) adresinden ücretsiz bir hesap oluşturun.

### Adım 2: Yeni Repository Oluşturma
1. GitHub'da sağ üst köşedeki "+" butonuna tıklayın
2. "New repository" seçin
3. Repository adını `kullaniciadi.github.io` formatında girin
   - Örnek: `buyukada.github.io`
4. "Public" seçeneğini işaretleyin
5. "Create repository" butonuna tıklayın

### Adım 3: Dosyaları Yükleme
1. Oluşturulan repository sayfasında "uploading an existing file" linkine tıklayın
2. Tüm site dosyalarını sürükleyip bırakın:
   - index.html
   - publications.html
   - resources.html
   - contact.html
   - style.css
   - script.js
3. "Commit changes" butonuna tıklayın

### Adım 4: GitHub Pages Aktivasyonu
1. Repository'de "Settings" sekmesine gidin
2. Sol menüden "Pages" seçin
3. "Source" bölümünde "Deploy from a branch" seçin
4. Branch olarak "main" ve folder olarak "/ (root)" seçin
5. "Save" butonuna tıklayın

### Adım 5: Site Erişimi
Birkaç dakika içinde siteniz şu adreste yayınlanacaktır:
```
https://kullaniciadi.github.io
```

## Özelleştirmeler

### Kişisel Bilgileri Güncelleme
Tüm HTML dosyalarında aşağıdaki bilgileri kendi bilgilerinizle değiştirin:
- "Büyükada" → Kendi adınız
- E-posta adresi
- Kurum bilgileri
- ORCID, Google Scholar linkleri

### Yayın Linkleri Ekleme
`publications.html` dosyasında her yayın için:
```html
<a href="https://dergipark.org.tr/tr/pub/DERGI/issue/SAYI/MAKALE" class="publication-link" target="_blank">
    DergiPark
</a>
```
`#` yerine gerçek DergiPark linklerini ekleyin.

### İndirilebilir Dosyalar
1. `files/` klasörü oluşturun
2. Excel, PDF dosyalarınızı bu klasöre yükleyin
3. `resources.html` dosyasındaki linkleri güncelleyin

### İletişim Formu (Opsiyonel)
Formspree kullanmak için:
1. [formspree.io](https://formspree.io) adresinde ücretsiz hesap oluşturun
2. Yeni form oluşturun
3. `contact.html` dosyasında form action URL'sini güncelleyin:
```html
<form action="https://formspree.io/f/YOUR-FORM-ID" method="POST">
```

## Özel Alan Adı (İsteğe Bağlı)

Kendi alan adınızı kullanmak için:
1. Bir alan adı satın alın (örn: namecheap.com, google domains)
2. GitHub repository'de `CNAME` dosyası oluşturun
3. İçine alan adınızı yazın: `www.siteadiniz.com`
4. Alan adı sağlayıcınızda DNS ayarlarını yapın

## Güncelleme

Site içeriğini güncellemek için:
1. GitHub'da ilgili dosyayı açın
2. Kalem (edit) ikonuna tıklayın
3. Değişiklikleri yapın
4. "Commit changes" butonuna tıklayın

Değişiklikler birkaç dakika içinde siteye yansıyacaktır.

## Destek

Sorunlar için GitHub Issues kullanabilir veya iletişim sayfasındaki bilgilerden ulaşabilirsiniz.

---

Bu şablon [Claude](https://claude.ai) tarafından oluşturulmuştur.
