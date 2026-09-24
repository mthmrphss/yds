# YDS Hazırlayıcı - Uzaktan Müfredat & Soru Bankası Havuzu

Bu depo, **YDS Hazırlayıcı** mobil uygulamasının uzaktan soru, kelime, eşdizim ve konu anlatımı güncellemelerini çeken resmi veri deposudur.

Uygulama, her açılışta veya **Ayarlar -> "Güncellemeleri Şimdi Kontrol Et"** tıklandığında bu depodaki `manifest.json` dosyasını kontrol eder.

---

## 📂 Dosya Yapısı

- `manifest.json`: Versiyon kontrolü, son güncelleme tarihi ve dosya eşlemeleri.
- `questions.json`: 220+ Akademik YDS soru bankası (5 seçenek, çözüm açıklamaları ve çeldirici analizleri).
- `vocabulary.json`: 800+ Akademik YDS kelime havuzu (tanımlar, eşanlamlılar, örnek cümleler ve SM-2 aralıklı tekrar parametreleri).
- `connectors.json`: 45+ Mantıksal bağlaç tablosu (Zıtlık, Sebep-Sonuç, Ödün, vb.).
- `collocations.json`: 160 Akademik eşdizim (Fiil + İsim, Sıfat + İsim).
- `phrasal_verbs.json`: 110 Sık çıkan phrasal verb ve resmi akademik eş anlamlıları.
- `grammar_notes.json`: Akademik gramer konu anlatımları, ipuçları ve ÖSYM tuzakları.
- `exam_strategies.json`: 4 Adımlı Çözüm Rutini ve 180 Dk Zaman Yönetimi kuralları.

---

## 🔄 Yeni Soru veya Kelime Nasıl Eklenir?

1. `questions.json` veya `vocabulary.json` dosyasını açıp listenin sonuna yeni sorunuzu / kelimenizi ekleyin.
2. `manifest.json` dosyasındaki **`version`** değerini artırın:
   ```json
   "version": "1.1",
   "updated_at": "2026-10-01",
   "changelog": "50 yeni Cümle Tamamlama ve Okuma Parçası sorusu eklendi."
   ```
3. Değişiklikleri `git commit` ve `git push` ile repoya gönderin.

> **Tebrikler!** APK'yı yüklemiş olan tüm kullanıcılar uygulamayı açtıklarında yeni soruları otomatik olarak telefonlarına indirmiş olacaktır. Kullanıcıların daha önce çözdüğü deneme ve kelime ezber geçmişleri korunur.
