<div align="center">

# ◉ JARVIS EVERYWHERE

### Jarvis On Every. Jarvis For Every.

**La tua voce. La tua casa. Le tue idee.**

Un progetto per portare un assistente vocale open-source in ogni stanza,
con Home Assistant e strumenti di produttività al centro.

![Stato: concept e demo](https://img.shields.io/badge/stato-concept_%26_demo-00F2C3?style=for-the-badge&labelColor=1B2327)
![Home Assistant: integrazione prevista](https://img.shields.io/badge/Home_Assistant-previsto-38BDF8?style=for-the-badge&labelColor=1B2327)
![Coming Soon](https://img.shields.io/badge/release-coming_soon-00D2FF?style=for-the-badge&labelColor=1B2327)

### [↗ Esplora il sito e prova la demo](https://samu3k.github.io/jarvis-everywhere/)

[La visione](#la-visione) · [Cosa esiste oggi](#cosa-esiste-oggi) · [Roadmap](#roadmap) · [Contribuire](#contribuire)

<sub>Unico sviluppatore: <a href="https://github.com/Samu3k">Samu3k</a> · Nome repository: <code>jarvis-everywhere</code></sub>

</div>

---

> **PROGETTO IN SVILUPPO.** Unico sviluppatore: **Samu3k**. Questa repository presenta la visione di JARVIS e una demo frontend simulata. Il motore vocale, il collegamento reale a Home Assistant e i servizi di produttività sono ancora da implementare.

## La visione

Immagina di entrare in salotto, in cucina o in studio e dire soltanto:

> «Hei Jarvis…»

Nessuna app da cercare, nessuna interfaccia da aprire. L’obiettivo è avere punti voce distribuiti nelle stanze e un assistente centrale capace di interpretare le richieste, usare gli strumenti giusti e rispondere dove ti trovi.

Home Assistant è il punto di partenza per la domotica. Musica, bozze email e task più articolati estenderanno l’esperienza oltre il controllo della casa.

**JARVIS** è il nome dell’assistente. **Jarvis Everywhere** esprime la direzione del progetto: renderlo presente e utile in tutta la casa.

## Un giorno, in casa

| Dove | Cosa vorresti dire | Esperienza desiderata |
| --- | --- | --- |
| Salotto | «Imposta il clima a 22 gradi» | Controllare il condizionatore tramite Home Assistant |
| Cucina | «Metti musica» | Riprodurre la musica nello spazio scelto |
| Studio | «Scrivi una bozza email» | Preparare un testo da rileggere e completare |
| Camera | «Serata relax» | Richiamare una sequenza di azioni personalizzata |
| Ogni stanza | «Qual è lo stato della casa?» | Ricevere un riepilogo dei dispositivi configurati |

Questi esempi descrivono l’obiettivo. La demo sul sito ne simula alcuni, senza eseguire azioni reali.

## Cosa esiste oggi

- Landing page responsive in **un unico `index.html`**, con CSS e JavaScript integrati.
- Interfaccia scura con accenti verde acqua/ciano, nucleo animato e anelli orbitali.
- Tema chiaro e scuro, con pulsante sole/luna animato e preferenza ricordata nel browser.
- Interfaccia completa in italiano e inglese, con selettore IT/EN: anche le risposte della demo cambiano lingua.
- Avviso «Progetto in sviluppo» e indicazione dell’unico sviluppatore nella prima schermata.
- Piantina interattiva di quattro stanze e selezione dell’ambiente.
- Demo testuale con comandi rapidi per clima, musica, bozze email e stato Home Assistant.
- Stato indipendente per stanza durante la visita e scenari «Serata relax» e «Modalità lavoro».
- Animazioni della forma d’onda, comparsa delle sezioni e supporto a `prefers-reduced-motion`.
- Visione, architettura proposta, roadmap e FAQ.

La demo riconosce parole chiave italiane e inglesi e scenari predefiniti: **non è un modello AI**. Non usa il microfono, non riproduce musica, non controlla dispositivi e non invia email. I comandi e lo stato restano nella memoria della pagina e si azzerano ricaricandola. Solo tema e lingua vengono salvati in `localStorage`, quando disponibile. Il font viene richiesto a Google Fonts; le icone sono incorporate nel file.

### Prova qualche comando

```text
Hei Jarvis, imposta il clima a 24 gradi in cucina
Metti musica in salotto
Ferma la musica in salotto
Scrivi una bozza email in studio
Stato Home Assistant
Hei Jarvis, serata relax in camera
Hei Jarvis, modalità lavoro in studio

Hey Jarvis, set the climate to 24 degrees in the kitchen
Play music in the living room
Write an email draft in the study
Hey Jarvis, relax evening in the bedroom
```

La temperatura accettata dalla demo va da 16 a 30 °C. Puoi scegliere una stanza dall’interfaccia o nominarla nel comando. Le bozze sono esempi predefiniti, non testi generati a partire da richieste libere.

## Architettura proposta

```text
Punti voce nelle stanze
        │
        ▼
Richiamo «Hei Jarvis» + riconoscimento vocale
        │
        ▼
Assistente centrale: interpretazione e instradamento
        │
        ├── Home Assistant → dispositivi, clima, scene
        ├── Musica → integrazione da scegliere
        └── Produttività → bozze email e strumenti futuri
        │
        ▼
Risposta vocale nella stanza di origine
```

Questo è uno schema di progetto, non uno stack già implementato. Restano da scegliere hardware dei punti voce, wake word engine, riconoscimento e sintesi vocale, modello AI, protocolli e servizi esterni. Il comportamento locale o cloud e la gestione dei dati saranno documentati insieme a queste scelte.

## Roadmap

### 01 — Presentazione e demo

- [x] Definire identità visiva e visione iniziale.
- [x] Realizzare la landing page e la demo simulata.
- [x] Esplorare scenari e stato per stanza nella demo.
- [x] Scrivere la documentazione iniziale.
- [x] Creare la repository e preparare i file per GitHub Pages.
- [x] Aggiungere temi chiaro/scuro e traduzione italiano/inglese.

### 02 — Primo prototipo reale

- [ ] Scegliere e documentare lo stack voce.
- [ ] Collegare un ambiente di test a Home Assistant.
- [ ] Completare il percorso voce → intento → azione → risposta.
- [ ] Validare un primo punto voce in una stanza.
- [ ] Definire autenticazione, autorizzazioni e gestione dei dati.

### 03 — Multiroom e produttività

- [ ] Gestire punti voce e risposte in più stanze.
- [ ] Integrare la riproduzione musicale.
- [ ] Aggiungere strumenti per preparare bozze email.
- [ ] Richiedere conferma prima dell’eventuale invio di messaggi.
- [ ] Documentare installazione, configurazione e compatibilità hardware.

La roadmap è indicativa e non promette date di rilascio.

## Aprire la demo in locale

Scarica la repository e apri `index.html` nel browser. Non sono necessari installazione, compilazione, chiavi API o un server. Se Google Fonts non è disponibile, viene usato il font di sistema.

## Pubblicare il sito su GitHub Pages

1. Crea una repository chiamata **`jarvis-everywhere`** nell’account **`Samu3k`**. Per usare Pages con GitHub Free, scegli una repository pubblica.
2. Carica `index.html` e questo `README.md` nella cartella principale del branch `main`.
3. Apri **Settings → Pages** e seleziona **Deploy from a branch**.
4. Scegli **`main`** e **`/ (root)`**, quindi salva.
5. Attendi il completamento della pubblicazione e apri **[il sito JARVIS](https://samu3k.github.io/jarvis-everywhere/)**.

Riferimento: [documentazione ufficiale di GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site).

### Collegamenti del progetto

| Destinazione | Indirizzo previsto |
| --- | --- |
| Repository | https://github.com/Samu3k/jarvis-everywhere |
| Sito | https://samu3k.github.io/jarvis-everywhere/ |
| Demo | https://samu3k.github.io/jarvis-everywhere/#demo |
| Roadmap sul sito | https://samu3k.github.io/jarvis-everywhere/#roadmap |

Se scegli un nome diverso, aggiorna `GITHUB_URL` e gli attributi `href` dei link `data-repository` in `index.html`, poi i collegamenti in questo README. Gli `href` espliciti mantengono i link disponibili anche con JavaScript disattivato.

## Struttura iniziale

```text
jarvis-everywhere/
├── index.html    # Landing page, stile e demo interattiva
└── README.md     # Visione, stato del progetto e collegamento al sito
```

## Contribuire

Sono benvenuti casi d’uso, test della demo, miglioramenti di accessibilità e proposte sulle integrazioni.

- Apri una issue descrivendo il problema o lo scenario che immagini.
- Per modifiche ampie, discuti prima l’approccio in una issue.
- Nelle pull request indica cosa cambia e come hai verificato il risultato.

In questa fase sono particolarmente utili esperienze con Home Assistant, hardware audio, riconoscimento vocale e interazioni multiroom.

## Licenza

L’obiettivo è distribuire JARVIS come progetto open-source. **La licenza non è ancora stata scelta**: prima di presentare il codice come liberamente riutilizzabile verrà aggiunto un file `LICENSE` con i termini applicabili. Questa documentazione non assegna una licenza al progetto.

---

<div align="center">

**Jarvis su tutto, Jarvis per tutti.**

[◉ Torna al sito e prova la demo](https://samu3k.github.io/jarvis-everywhere/)

<sub>JARVIS — Unico sviluppatore: Samu3k · Progetto in sviluppo</sub>

</div>
