# ⏳ Countdown Timer

> Un timer di conto alla rovescia completo, in un **singolo file HTML** — zero dipendenze, zero build, funziona offline.

Apri `countdown.html` nel browser e via: nessun server, nessuna installazione, nessun framework. Tutto lo stato (impostazioni, titoli, logo, coda) viene salvato localmente nel browser tramite `localStorage`.

---

## 🚀 Avvio rapido

```bash
# basta aprire il file nel browser
code countdown.html        # VS Code: "Open with Live Server" oppure doppio click sul file
```

Oppure, se vuoi servirlo localmente:

```bash
python3 -m http.server 8080
# → http://localhost:8080/countdown.html
```

Funziona in tutti i browser moderni (Chrome, Firefox, Edge, Safari) su desktop e mobile.

---

## ✨ Funzionalità

### 🕐 Modalità Singolo
- **Timer principale** con display grande e leggibile (es. `15:00`), che mostra lo stato corrente: tempo rimanente o **«Tempo scaduto!»** al termine.
- **Preset rapidi**: pulsanti per `1 min`, `2 min`, `3 min`, `5 min`, `10 min`, `15 min` — un click e il timer è pronto.
- **Tempo personalizzato**: campi separati per **ore**, **minuti** e **secondi** per qualsiasi durata (anche oltre 24 h).
- **💾 Salva**: memorizza la configurazione corrente (durata, titolo, logo, impostazioni) nel `localStorage` del browser, così ritrovi tutto all'apertura successiva.

### 📋 Modalità Coda
Per chi gestisce più intervalli di fila (pomodoro, lezioni, turni, workout):
- **+ Aggiungi**: inserisci un nuovo elemento in coda con la propria durata (ore / min / sec) e il proprio titolo.
- **Carica… / Rimuovi**: carica o elimina gli elementi della coda.
- **Avvia**: parte la sequenza — al termine di ogni voce il timer passa automaticamente alla successiva, fino a svuotare la coda.

### 🎨 Personalizzazione
| Elemento | Opzioni |
|---|---|
| **Titolo** | Testo libero sopra il timer (es. «Pausa caffè», «Lezione 3») |
| **Font del titolo** | Selezionabile tra i font disponibili |
| **Dimensione testo** | Slider in percentuale (default `100%`) |
| **Logo** | Caricamento di un'immagine personalizzata, con controllo di **dimensione** e **colore**; rimovibile con ✕ |

### 🔊 Audio
- **Suono finale** al termine del conto alla rovescia, scegliibile tra:
  - 🎵 **Bip**, **Campanella**, **Ding**, **Sirena**, **Arpeggio** (sintetizzati in tempo reale con la Web Audio API — nessun file necessario)
  - 📁 **File audio…**: carica il tuo MP3/WAV/OGG preferito
- **☒ Attivo**: on/off globale del suono.
- **Volume**: regolabile in percentuale (default `80%`).
- **Bip ogni secondo** negli ultimi istanti, per un conto alla rovescia udibile:
  - attivabile con scelta della finestra: **5 sec**, **10 sec**, **15 sec** o **30 sec**.

### ⚙️ Importa / Esporta
- **⬇ Esporta**: salva tutte le impostazioni (suoni, volume, titolo, logo, lingua, coda…) in un file JSON portabile — perfetto per backup o per trasferire la configurazione su un altro PC/browser.
- **⬆ Importa**: ripristina una configurazione da un file esportato in precedenza.

### 🌍 Lingue
- Interfaccia multilingua: la lingua è selezionabile dalle impostazioni e viene salvata automaticamente.

---

## ⌨️ Scorciatoie da tastiera

| Tasto | Azione |
|---|---|
| `Spazio` | Avvia / Pausa |
| `R` | Azzera il timer |
| `F` | Schermo intero |

I pulsanti a schermo sono equivalenti: **Avvia/Pausa**, **↺ Azzera**, **⛶ Schermo intero**.

---

## 🏗️ Note tecniche

- **Single-file app**: HTML + CSS + JavaScript in un unico file, nessuna dipendenza esterna, nessun CDN, nessuna rete richiesta.
- **Audio sintetizzato**: i suoni predefiniti (bip, campanella, ding, sirena, arpeggio) sono generati con la [Web Audio API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API), quindi istantanei e senza latenza da caricamento file.
- **Persistenza**: `localStorage` per lo stato; JSON per import/export esplicito.
- **Schermo intero** tramite Fullscreen API, ideale per proiettori e TV in aula o in palestra.
- **Responsive**: utilizzabile anche su tablet e smartphone.

---
