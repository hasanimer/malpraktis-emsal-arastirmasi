# Malpraktis Emsal Araştırması

Türkiye’de tıbbi malpraktis ve hekim sorumluluğu uyuşmazlıklarında emsal karar bulmak, kararları somut olayla karşılaştırmak ve atıfları kontrol etmek için bir Codex becerisi. Aydınlatılmış onam, tıbbi kusur, komplikasyon, bilirkişi incelemesi, tazminat ve yargı yolu gibi konuları kapsar.

## Kurulum ve kullanım

```sh
git clone https://github.com/hasanimer/malpraktis-emsal-arastirmasi.git
```

Klonlanan `malpraktis-emsal-arastirmasi` klasörünü `$CODEX_HOME/skills` altına taşıyın. `CODEX_HOME` tanımlı değilse varsayılan dizin `~/.codex/skills` olur. Yeni bir Codex sohbetinde beceriyi `$malpraktis-emsal-arastirmasi` ile çağırın.

```text
$malpraktis-emsal-arastirmasi ile özel hastanede aydınlatılmış onamın
kapsamına ilişkin emsalleri bul. İlgili gerekçeyi, PDF sayfasını ve
karar künyesinin doğrulama durumunu göster.
```

Yerel derlemede arama için bir MCP bağlantısı gerekmez. LegalUga MCP bağlıysa beceri ek karar aramak ve bulunan künyeleri ve alıntıları kontrol etmek için onu da kullanır.

## Karar derlemesi

57 Markdown dosyası, kaynak PDF’nin 5.230 sayfasının metnini ve sayfa numaralarını içerir. TSV dizinindeki 6.750 başlık kaydı, kararların geçtiği sayfaları gösterir. Bir karar derlemenin farklı bölümlerinde birden fazla kez yer alabilir.

- Konuya veya PDF sayfa aralığına göre gezin. [Konu ve sayfa dizini](references/emsal-dizini.md)
- Bir kararın derlemede geçtiği sayfaları bulun. [Karar başlıkları (TSV)](references/karar-basliklari.tsv)
- Metinde arama yapın. [Markdown dosyaları](references/metin/)
- Araştırma ve doğrulama akışını inceleyin. [Beceri yönergesi](SKILL.md)

## Kaynak

Av. Hakan Dimdik, *Malpraktis (Tıbbi Kötü Uygulama) Davalarına İlişkin Emsal Kararlar*, 26.11.2026. Derleme karar pasajları içerir. Dilekçe atıfları için karar künyesini, ilgili gerekçeyi ve hükmü kararın resmî kaynağından kontrol edin. [Kaynak kapağı ve içindekiler](references/metin/00-kapak-ve-icindekiler-0001-0004.md)
