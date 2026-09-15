# Il tuo sito da ricercatore

Sito statico (HTML/CSS/JS puro, nessuna build necessaria) pronto per GitHub Pages.

## Struttura

```
index.html              → tutta la pagina, sezioni comprese
assets/css/style.css     → stile (tema scuro, tipografia, layout)
assets/js/main.js        → evidenzia la sezione attiva nel menu laterale
assets/img/              → qui vanno la tua foto e le immagini dei paper
assets/cv.pdf            → il tuo CV in PDF (da aggiungere)
```

## Come personalizzarlo

1. **Testi**: apri `index.html` e sostituisci i segnaposto (nome, affiliazione, bio,
   news, pubblicazioni, progetti, premi, educazione, contatti). Sono tutti in inglese;
   puoi tradurli in italiano se preferisci, basta modificare il testo — CSS e layout
   restano invariati.
2. **Foto**: metti il tuo file in `assets/img/`, poi nel file `index.html` sostituisci
   il blocco `<div class="avatar-placeholder">JR</div>` con
   `<img class="avatar" src="assets/img/tuafoto.jpg" alt="Il tuo nome">`.
3. **CV**: metti il PDF in `assets/cv.pdf` (o cambia il link nel bottone "Download CV").
4. **Colori/font**: tutte le variabili sono in cima a `assets/css/style.css`, sotto `:root`.
   Cambia `--accent` per un colore diverso, o i valori `--font-serif` / `--font-sans`
   per un'altra combinazione tipografica da Google Fonts.

## Come pubblicarlo su GitHub Pages

1. Crea un repository su GitHub chiamato `<tuo-username>.github.io`
   (questo nome esatto ti dà la pagina all'indirizzo radice).
2. Carica tutto il contenuto di questa cartella nella root del repository
   (non in una sottocartella).
3. Vai su **Settings → Pages** nel repository, e in "Build and deployment"
   seleziona come source **Deploy from a branch**, branch `main`, cartella `/ (root)`.
4. Dopo qualche minuto la pagina sarà live su `https://<tuo-username>.github.io`.

Se invece vuoi tenerlo come repository separato (es. `mio-sito-ricerca`), sarà
raggiungibile su `https://<tuo-username>.github.io/mio-sito-ricerca/`.

## Note

- Il sito è completamente statico: nessuna dipendenza da build tool, npm o simili.
- È responsive: sotto gli 860px la sidebar si sposta in alto.
- Rispetta `prefers-reduced-motion` e ha il focus visibile per l'accessibilità da tastiera.
