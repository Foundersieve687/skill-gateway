<p align="center">
  <img src="skill.png" alt="Skill Gateway" width="400">
</p>

# Skill Gateway

> **v0.1.0-beta**

**Rule all skills.**

The meta-skill that routes every request to the right skill — invisibly.

> There are hundreds of Claude/Agent Skills scattered across dozens of repos. You shouldn't have to memorize them. Skill Gateway does the thinking for you.

---

[🇬🇧 English](#en) · [🇹🇷 Türkçe](#tr)

---

<a id="en"></a>

## 🇬🇧 English

### What Is This?

Skill Gateway is the **entry point** to the entire Claude/Agent Skill ecosystem. Instead of memorizing hundreds of skills across dozens of repos, just describe what you need — Skill Gateway finds the right skill and starts working immediately.

### How It Works

```
You: "Create a presentation"

Behind the scenes:
  → Skill Gateway triggers first (priority on every task)
  → Internal assessment: "This is a pptx skill job"
  → Reads pptx skill's SKILL.md
  → Starts making the presentation

You only see the result. Gateway is invisible.
```

Three scenarios:

| Situation | What Happens |
|-----------|-------------|
| **Clear request** ("merge PDFs", "make a spreadsheet") | Direct handoff to the relevant skill, starts working |
| **Ambiguous request** ("I need a design") | Asks ONE clarifying question, starts working with the answer |
| **Conversation** ("How are you?", "What is AI?") | Doesn't trigger, Claude works normally |

### Contents

```
skill-gateway/
├── SKILL.md              # Main skill file
├── README.md             # This file
├── skill-gateway.skill   # Uploadable skill package
├── skill.png             # Project image
└── VERSION               # Semantic version
```

**SKILL.md includes:**
- Gateway behavior rules (always handoff, invisible routing)
- Decision flowchart
- Curated catalog of 60+ categorized skills
- References to 7 major aggregator repos
- Quick routing table (decision shortcuts)
- Workaround strategies when no skill exists
- Web search instructions for discovering new skills

### Catalog Categories

| Category | Examples |
|----------|----------|
| 📄 Document & File | docx, pdf, pptx, xlsx, epub |
| 💻 Development | frontend-design, TDD, debugging, MCP builder, Playwright |
| 🔒 Security | OWASP, VibeSec, Trail of Bits, sanitize |
| 📊 Data & Analysis | CSV summarizer, PostgreSQL, MySQL |
| 📣 Marketing & Content | SEO, email marketing, creative director |
| 🎨 Creative & Design | canvas-design, theme-factory, video |
| 🏗️ Project & Workflow | kanban, Linear, git, changelog |
| ☁️ Platform (Official) | Vercel, Cloudflare, Stripe, Sentry, Expo, Google |

### Installation

#### Claude.ai
1. **Settings** → **Skills** → **Add Skill**
2. Upload the `skill-gateway.skill` file
3. Skill Gateway now automatically triggers on every task

#### Claude Code
```bash
# Personal skill
cp -r skill-gateway ~/.claude/skills/

# Project-level
cp -r skill-gateway .claude/skills/
```

#### API
```bash
# Via Skills API
# Details: https://docs.anthropic.com/en/docs/agents-and-tools/skills
```

### Important Notes

- **Skill ≠ MCP Server.** Skills are instruction packages, MCP servers are live API connections. Gateway can recommend either.
- **Quality varies.** Official provider skills > well-starred repos > random community skills.
- **Security.** Skills execute code. Be cautious with skills from unknown sources.
- **Freshness.** The catalog covers foundational skills; web search handles newly released ones.

---

<a id="tr"></a>

## 🇹🇷 Türkçe

### Ne İşe Yarar?

Skill Gateway, tüm Claude/Agent Skill ekosisteminin **giriş kapısıdır**. Yüzlerce skill arasında kaybolmanıza gerek yok — siz derdinizden bahsedin, Skill Gateway doğru skill'i bulur ve direkt işe başlar.

### Nasıl Çalışır?

```
Sen: "Bir sunum hazırla"

Perde arkası:
  → Skill Gateway tetiklenir (her task'ta ilk o devreye girer)
  → İç değerlendirme: "Bu pptx skill'inin işi"
  → pptx skill'inin SKILL.md'sini okur
  → Sunumu yapmaya başlar

Sen sadece sonucu görürsün. Gateway görünmezdir.
```

Üç senaryo:

| Durum | Ne Olur |
|-------|---------|
| **Açık istek** ("PDF birleştir", "Excel yap") | Direkt ilgili skill'e handoff, işe başlar |
| **Belirsiz istek** ("Bir tasarıma ihtiyacım var") | Tek bir soru sorar, cevapla birlikte işe başlar |
| **Sohbet** ("Nasılsın?", "AI nedir?") | Tetiklenmez, Claude normal çalışır |

### İçindekiler

```
skill-gateway/
├── SKILL.md              # Ana skill dosyası
├── README.md             # Bu dosya
├── skill-gateway.skill   # Yüklenebilir skill paketi
├── skill.png             # Proje görseli
└── VERSION               # Semantic versiyon
```

**SKILL.md şunları içerir:**
- Gateway davranış kuralları (always handoff, invisible routing)
- Karar akış şeması (decision flowchart)
- 60+ skill içeren kategorize edilmiş katalog
- 7 büyük aggregator repo referansı
- Hızlı yönlendirme tablosu (decision shortcuts)
- Skill bulunamadığında workaround stratejileri
- Web search ile güncel skill tarama talimatları

### Katalog Kategorileri

| Kategori | Örnekler |
|----------|----------|
| 📄 Doküman & Dosya | docx, pdf, pptx, xlsx, epub |
| 💻 Geliştirme | frontend-design, TDD, debugging, MCP builder, Playwright |
| 🔒 Güvenlik | OWASP, VibeSec, Trail of Bits, sanitize |
| 📊 Veri & Analiz | CSV summarizer, PostgreSQL, MySQL |
| 📣 Pazarlama & İçerik | SEO, email marketing, creative director |
| 🎨 Yaratıcı & Tasarım | canvas-design, theme-factory, video |
| 🏗️ Proje & Workflow | kanban, Linear, git, changelog |
| ☁️ Platform (Official) | Vercel, Cloudflare, Stripe, Sentry, Expo, Google |

### Kurulum

#### Claude.ai
1. **Settings** → **Skills** → **Add Skill**
2. `skill-gateway.skill` dosyasını yükleyin
3. Artık her task'ta Skill Gateway otomatik devreye girer

#### Claude Code
```bash
# Kişisel skill olarak
cp -r skill-gateway ~/.claude/skills/

# Proje bazlı
cp -r skill-gateway .claude/skills/
```

#### API
```bash
# Skills API ile
# Detaylar: https://docs.anthropic.com/en/docs/agents-and-tools/skills
```

### Önemli Notlar

- **Skill ≠ MCP Server.** Skill'ler talimat paketidir, MCP server'lar canlı API bağlantısıdır. Gateway ikisini de önerebilir.
- **Kalite değişkendir.** Resmi provider skill'leri > iyi yıldızlı repo'lar > rastgele community skill'leri.
- **Güvenlik.** Skill'ler kod çalıştırır. Bilinmeyen kaynaklardan gelen skill'lere dikkat edin.
- **Güncellik.** Katalog temel skill'leri kapsar, yeni çıkanlar için web search yapar.

---

## Contributing

Found a skill that should be in the catalog? Open a PR or issue.

## License

MIT
