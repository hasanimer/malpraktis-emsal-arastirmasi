# Malpraktis Emsal Kararları için Agent Skill

Türkiye’de tıbbi malpraktis ve hekim sorumluluğu uyuşmazlıklarında emsal karar bulmak, kararları somut olayla karşılaştırmak ve atıfları kontrol etmek için Claude Code ve Codex’te kullanılabilen bir beceri. Aydınlatılmış onam, tıbbi kusur, komplikasyon, bilirkişi incelemesi, tazminat ve yargı yolu gibi konuları kapsar.

## Kurulum ve kullanım

```sh
git clone https://github.com/hasanimer/malpraktis-emsal-kararlar-skill.git malpraktis-emsal-arastirmasi
```

Klonlanan `malpraktis-emsal-arastirmasi` klasörünü kullandığınız aracın kişisel beceri dizinine taşıyın. Yeni bir oturumda beceriyi tablodaki adla çağırın.

| Araç | Kişisel beceri dizini | Çağırma |
| --- | --- | --- |
| Claude Code | `~/.claude/skills/` | `/malpraktis-emsal-arastirmasi` |
| Codex | `$CODEX_HOME/skills/` veya `~/.codex/skills/` | `$malpraktis-emsal-arastirmasi` |

Claude Code’da beceriyi bir projeyle paylaşmak için klasörü o projenin `.claude/skills/` dizinine de ekleyebilirsiniz. [Claude Code beceri belgeleri](https://code.claude.com/docs/en/skills)

Örnek araştırma isteği

```text
Özel hastanede aydınlatılmış onamın kapsamına ilişkin emsalleri bul.
İlgili gerekçeyi, PDF sayfasını ve karar künyesinin doğrulama durumunu göster.
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
