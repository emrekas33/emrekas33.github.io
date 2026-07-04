# Atölye Defteri

Opel yedek parça / motor parça tedarik işini kayıt altına almak için basit, tek dosyalık bir web paneli. Kurulum gerektirmez — tek bir `index.html` dosyası, tarayıcıda direkt çalışır.

## Özellikler
- **Panel:** toplam iş, bekleyen iş, toplam kâr, az kalan stok, toplam stok değeri, potansiyel kâr, en aktif tedarikçi
- **İşler:** tamirciye giden iş kayıtları (araç/motor, aranan parça, tedarikçi, maliyet/satış, kâr)
- **Parça Stok:**
  - Parça adı, parça numarası, kategori, adet, min. uyarı seviyesi, alış/satış fiyatı
  - Arama, kategoriye göre filtreleme, sıralama (ada/stoğa/değere göre), "sadece az stoklu" filtresi
  - Her parça için stok hareket geçmişi (giriş/çıkış/düzenleme kaydı)
  - **Excel'e Aktar:** tüm listeyi tek tıkla `.xlsx` olarak indirin
  - **Excel'den İçe Aktar:** dışa aktardığınız formatta bir dosyayı geri yükleyip toplu güncelleme/ekleme yapın
  - **Yazdır:** filtrelenmiş listeyi yazdırılabilir rapor olarak açar
- **Tedarikçiler** ve **Tamirciler** listesi

Veriler tarayıcının kendi hafızasında (`localStorage`) saklanır — kurulum, veritabanı ya da internet bağlantısı gerekmez.

> **Not:** Veriler sadece kullandığınız tarayıcı + cihazda saklanır. Farklı bir bilgisayar veya tarayıcıdan açarsanız kayıtları göremezsiniz. Tarayıcı geçmişini/verilerini temizlerseniz kayıtlar da silinir.

## GitHub'a Yükleme (import)

### Yöntem 1 — Tarayıcıdan, komut satırı olmadan
1. [github.com/new](https://github.com/new) adresinden yeni bir repo oluşturun (örn. `atolye-defteri`).
2. Repo sayfasında **"uploading an existing file"** linkine tıklayın.
3. Bu klasördeki `index.html` ve `README.md` dosyalarını sürükleyip bırakın.
4. **Commit changes** ile onaylayın.

### Yöntem 2 — Git ile (bilgisayarınızda git kuruluysa)
```bash
cd atolye-defteri
git init
git add .
git commit -m "İlk sürüm: Atölye Defteri"
git branch -M main
git remote add origin https://github.com/KULLANICI_ADINIZ/atolye-defteri.git
git push -u origin main
```

## Ücretsiz Yayınlama (GitHub Pages)
Dosyayı internetten herkese açık bir linkle paylaşmak isterseniz:
1. GitHub'da repo sayfasında **Settings > Pages** bölümüne gidin.
2. **Source** olarak `main` branch'i ve `/ (root)` klasörünü seçin, **Save**'e basın.
3. Birkaç dakika içinde siteniz `https://KULLANICI_ADINIZ.github.io/atolye-defteri/` adresinde yayında olur.

Dosya adı `index.html` olduğu için GitHub Pages otomatik olarak ana sayfa olarak tanır, ekstra ayara gerek yok.

## Yerelde Çalıştırma
İnternete koymadan sadece kendi bilgisayarınızda kullanmak isterseniz `index.html` dosyasına çift tıklamanız yeterli — tarayıcıda direkt açılır.
