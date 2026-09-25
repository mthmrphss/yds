# YDS Hazırlayıcı - Uzaktan Soru Deposu

Bu depo, **YDS Hazırlayıcı** uygulamasının uzaktan güncellenen **özgün** sorularını barındırır.
Sorular YDS/YÖKDİL formatında (11 soru tipi, kolay/orta/zor) uygulama için yazılmıştır; ÖSYM veya
yayınevi kitapçıklarından alınmış soru içermez. Çıkmış sorular yalnızca uygulamanın içinde bulunur.

## Nasıl çalışır?

1. Uygulama açılışta veya **Ayarlar → Güncellemeleri Kontrol Et** ile `manifest.json` dosyasını okur.
2. `version`, uygulamadaki sürümden büyükse `endpoints.questions` dosyasını indirir.
3. İndirilen dosya yalnızca özgün soruları günceller: yeni sorular eklenir, çıkarılanlar silinir,
   kullanıcının cevap geçmişi korunur. Çıkmış sorulara dokunulmaz.

## Yeni soru eklemek

`yds_pdf/scripts/original/` altındaki dosyalara soru ekleyip `scripts/build_all.sh` çalıştırın,
`build_question_bank.py` içindeki sürümü artırın ve bu depoyu commit + push edin.

Şu an: 550 soru (cloze: 45, dialogue: 51, grammar: 59, irrelevant_sentence: 45, paragraph_completion: 45, reading: 48, restatement: 51, sentence_completion: 56, translation_en_tr: 45, translation_tr_en: 45, vocabulary: 60).
