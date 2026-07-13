# AI Newsroom — Redazione Artificiale

Progetto dimostrativo di **AI Agent Engineering**: una redazione giornalistica completamente orchestrata da agenti AI autonomi con model `opencode/deepseek-v4-flash-free`.

## Architettura

| Agente | Ruolo |
|--------|-------|
| **Editor-in-Chief** | Orchestratore centrale — coordina il flusso di lavoro |
| **Researcher** | Cerca notizie e immagini sul web |
| **Writer-Articolo** | Scrive articoli con tono giornalistico professionale |
| **Fact-Checker** | Verifica accuratezza dei fatti e licenze delle immagini |
| **Publisher** | Genera sito statico HTML |

## Stack

- **OpenCode** — framework agentico con MCP
- **Prompt Engineering** avanzato (Chain-of-Thought, meta-prompting)
- **MCP (Model Context Protocol)** — tool calling multi-agente
- **PowerShell + Python/JS** — automazione e integrazioni
- **GitHub Pages** — hosting statico

## Pipeline

```
Ricerca → Scrittura → Fact-Checking → Download immagini → Pubblicazione sito
```

Ogni articolo passa attraverso tutti e 4 gli agenti prima della pubblicazione, con validazione automatica.

## Risultati

- ✅ **6 articoli pubblicati** su temi reali (AI, sport, viaggi, attualità)
- ✅ **95.8% test superati** (24 test: 3 agenti × 8 test case ciascuno)
- ✅ **0 dipendenze esterne** — tutto locale, immagini copyright-free
- ✅ **Sito statico** completo con hero + griglia articoli

## Come eseguire

```bash
# Clona il repository
git clone https://github.com/FabioBl77/AI-Newsroom.git
cd AI-Newsroom

# Apri con OpenCode
opencode .

# Per generare nuove notizie:
#   Editor-in-Chief, cerca notizie su [tema]

# Per eseguire la suite di test:
#   Editor-in-Chief-Test, cercami...
```

## Struttura

```
├── .opencode/
│   └── agents/          # Configurazioni agenti
├── docs/
│   ├── index.html       # Home page
│   ├── *.html           # Pagine articoli
│   └── images/          # Immagini copyright-free
├── notizie.json         # Indice persistenti articoli
└── opencode.json        # Configurazione OpenCode
```

## Sito live

[https://FabioBl77.github.io/AI-Newsroom/](https://FabioBl77.github.io/AI-Newsroom/)

---

*Progetto realizzato con OpenCode — framework agentico per software engineering AI.*
