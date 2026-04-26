# Crema Storica — Archivio fotografico georeferenziato

Sito GitHub Pages: https://lucasccrema.github.io/crema-storica/

## Come aggiungere una nuova fotografia

### 1 — Aggiungi il file immagine
Copia il file `.jpg` nella cartella `images/` del progetto.

### 2 — Modifica index.html
Apri `index.html` con Notepad++ e trova l'array delle foto (cerca `lat:`).
Aggiungi una nuova riga alla fine dell'array, prima della `]` di chiusura:

```javascript
{id:XXX, desc:"TITOLO BREVE", file:"NOMEFILE.jpg", author:"AUTORE", lat:45.000000, lng:9.000000, caption:"Descrizione lunga opzionale.", src:"", tag:"CATEGORIA"},
```

**Campi:**
- `id` — numero progressivo (ultimo id presente + 1)
- `desc` — titolo breve visibile sul marker della mappa
- `file` — nome esatto del file immagine con estensione (es. `1960_piazzaDuomo.jpg`)
- `author` — fotografo/fonte, oppure `""` se sconosciuto
- `lat` / `lng` — coordinate GPS (tasto destro su Google Maps → copia coordinate)
- `caption` — descrizione lunga opzionale, oppure `""`
- `src` — link fonte originale, quasi sempre `""`
- `tag` — categoria: `"vie"`, `"porte"`, ... (vedi tag già usati nel file)

### 3 — Pubblica con GitHub Desktop
1. Apri GitHub Desktop
2. Nella colonna sinistra vedrai i file modificati
3. Scrivi un messaggio nel campo **Summary** (es. "Aggiunge foto piazza Duomo 1920")
4. Clicca **Commit to main**
5. Clicca **Push origin** in alto a destra

Il sito si aggiorna su GitHub Pages in 1-2 minuti.

### Tornare a una versione precedente
- **Prima del commit:** GitHub Desktop → tasto destro sul file → "Discard changes"
- **Dopo il commit ma prima del push:** Repository menu → "Undo commit"
- **Dopo il push:** crea un nuovo commit che corregge l'errore