# Sözlükler

Çevrimdışı kullanım için sıkıştırılmış sözlük verisi.

| Dosya | İçerik | Boyut |
|---|---|---|
| `sozluk-tr-1.tsv.gz` | Türkçe sözlük (106.041 tanımlı madde, 192.695 çekimli/başka yazımlı biçim yönlendirmesi) | 3,4 MB |
| `sozluk-en-1.tsv.gz` | İngilizce sözlük, tanımlar İngilizce (438.840 tanımlı madde, 76.829 düzensiz biçim/başka yazım yönlendirmesi) | 12,0 MB |

## Kaynak ve lisans

Türkçe veri **Türkçe Vikisözlük**'ten (tr.wiktionary.org), İngilizce veri **İngilizce Vikisözlük**'ten (en.wiktionary.org) türetilmiştir; ham veri [kaikki.org](https://kaikki.org/) dışa aktarımlarından alınmıştır.

Bu depodaki dosyalar **Creative Commons Atıf-AynıLisanslaPaylaş 4.0 (CC BY-SA 4.0)** ile lisanslıdır:
https://creativecommons.org/licenses/by-sa/4.0/deed.tr

Kaynak göstererek kullanabilir, değiştirebilir ve yeniden dağıtabilirsiniz; türettiğiniz veriyi aynı lisansla paylaşmanız gerekir.
Tanımların yazarları Vikisözlük katkıcılarıdır.

## Biçim

UTF-8, gzip ile sıkıştırılmış, satır başına bir kayıt, alanlar sekmeyle ayrılır, anahtara göre sıralıdır.

```
#sozluk <TAB> dil <TAB> sürüm <TAB> kaynak
kelime <TAB> tür <TAB> n <TAB> anlam1 [<TAB> anlam2 <TAB> anlam3] [<TAB> >madde]
kelime <TAB> >madde
```

- `n`: maddenin ortak anlam sayısı (0: yalnız özel ad anlamı vardır).
- `>madde` (tek başına): bu yazım kendi başına madde değildir, gösterilen maddeye yönlendirir (çekimli biçim ya da başka yazım).
- `>madde` (anlamlardan sonra): kelime hem kendi başına maddedir hem de gösterilen maddenin çekimli biçimidir (`left` → `leave`).
- Her maddede en çok üç anlam tutulur; uzun anlamlar kesilir (Türkçe 220, İngilizce 170 karakter).
- İngilizce dosyada kuralla bulunabilen düzenli biçimler (`walked`, `houses`) yer almaz; yalnız düzensizler vardır (`went` → `go`).
- İngilizce dosyada özel adlar ve birden çok kelimeden oluşan maddeler yoktur.

## Sürümler

Dosya adındaki sayı sürümdür. Yayınlanmış bir dosya değiştirilmez; yeni sürüm yeni adla eklenir (`sozluk-tr-2.tsv.gz`).

`sozluk-tr-1.tsv.gz` SHA-256: `f80c1c1722ad1b20d23c223d08e8d9f986205f3727f3d4f1f3c6a32de5719bd1`

`sozluk-en-1.tsv.gz` SHA-256: `f8cf98930072a559c8e3e5746be4a6be6bbbb8f606995e2ffd485d316be26d36`

---

**English:** Compressed dictionary data for offline use. Derived from the Turkish Wiktionary (via the kaikki.org export) and licensed under CC BY-SA 4.0. Definitions are written by Wiktionary contributors.
