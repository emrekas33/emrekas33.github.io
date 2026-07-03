# Atölye Defteri

Yedek parça tedarik işi için basit, tek dosyalık bir kayıt paneli. İşleri, tedarikçileri, tamircileri ve parça stoğunu takip etmek için kullanılır. Sunucu, veritabanı veya kurulum gerektirmez — tek bir `index.html` dosyasıdır.

## Özellikler

- **Panel** — toplam iş, bekleyen iş, toplam kâr ve az kalan stok özetleri
- **İşler** — tamirciye yönlendirilen parça talepleri, maliyet/satış/kâr takibi
- **Parça Stok** — parça adı, parça numarası, stok adedi, min. uyarı seviyesi, hızlı +1/−1 güncelleme
- **Tedarikçiler** ve **Tamirciler** — iletişim bilgileri ve notlar

## Veri nasıl saklanıyor?

Tüm veriler tarayıcınızın **localStorage**'ında saklanır — yani veriler yalnızca kaydettiğiniz cihaz + tarayıcıda kalır, hiçbir sunucuya gönderilmez. Bu şu anlama gelir:

- Farklı bir cihazdan açtığınızda veriler görünmez (senkronize olmaz).
- Tarayıcı geçmişini/verilerini temizlerseniz kayıtlar silinir.
- Ciddi kullanım için düzenli olarak yedek almanız önerilir (ileride bir "dışa aktar" özelliği eklenebilir).

## Kurulum / Kullanım

### 1) Doğrudan aç
`index.html` dosyasını herhangi bir tarayıcıda çift tıklayarak açabilirsiniz. İnternet bağlantısı sadece font yüklemek için gerekir (Google Fonts); olmasa da panel çalışır, sadece yazı tipi tarayıcı varsayılanına döner.

### 2) GitHub Pages ile yayınla (ücretsiz, herkese açık link)
1. Bu klasörü GitHub'da yeni bir repoya yükleyin (aşağıya bakın).
2. Repo ayarlarında **Settings → Pages** yolunu izleyin.
3. **Branch: main**, **Folder: / (root)** seçip kaydedin.
4. Birkaç dakika içinde `https://KULLANICI_ADINIZ.github.io/REPO_ADI/` adresinden erişilebilir olur.

## GitHub'a yükleme

Yerel bilgisayarınızda bu klasörün içindeyken:

```bash
git init
git add .
git commit -m "İlk sürüm: Atölye Defteri"
git branch -M main
git remote add origin https://github.com/KULLANICI_ADINIZ/REPO_ADI.git
git push -u origin main
```

Ya da GitHub web arayüzünden "Upload files" ile bu dosyaları sürükleyip bırakabilirsiniz — komut satırı gerekmez.

## Dosya yapısı

```
atolye-defteri/
├── index.html      # Tüm uygulama (HTML + CSS + JS tek dosyada)
├── README.md        # Bu dosya
└── .gitignore
```

## Geliştirme notları

Bağımlılık yok, build adımı yok. `index.html` içinde düzenleme yapıp tarayıcıda yenilemeniz yeterli. Veri modeli `localStorage` anahtarları üzerinden basit JSON dizileridir: `atolye-defteri:suppliers`, `atolye-defteri:mechanics`, `atolye-defteri:jobs`, `atolye-defteri:stock`.
