# X-Ray Mirror

Specchio a raggi X in tempo reale: cranio, cervello, muscoli e ossa della mano sovrapposti alla tua immagine, tracciati con la webcam (MediaPipe + three.js).

Tutto gira nel browser: il video non viene mai caricato su un server.

## Pubblicare su GitHub Pages (dal sito, senza installare nulla)

1. Vai su <https://github.com/new>.
   - **Repository name:** `x-ray-mirror` (o un altro nome)
   - **Public** (con un account gratuito, GitHub Pages funziona solo con repository pubblici)
   - Clicca **Create repository**.
2. Nella pagina del repository vuoto clicca **uploading an existing file**, trascina `index.html` (e questo `README.md`) e clicca **Commit changes**.
3. Vai su **Settings → Pages**.
   - **Source:** *Deploy from a branch*
   - **Branch:** `main`, cartella `/ (root)` → **Save**
4. Dopo 1–2 minuti il sito è online su:

   `https://<tuo-utente>.github.io/x-ray-mirror/`

   L'indirizzo compare anche in cima a Settings → Pages.

## Usarlo

- Apri il link in **Chrome o Edge** (desktop o Android), clicca **Start camera** e consenti l'accesso alla fotocamera.
- La prima volta i tracker impiegano qualche secondo a caricarsi.
- Scena dimostrativa senza fotocamera: aggiungi `#demo` all'indirizzo, ad esempio `https://<tuo-utente>.github.io/x-ray-mirror/#demo`.

## Dispositivi

La pagina contiene uno script di avvio della fotocamera (`window.XRCamera` in `index.html`) pensato per Mac, PC Windows, Android, iPhone e iPad:

- **Browser consigliati:** Chrome o Edge su computer, Chrome su Android, Safari su iPhone e iPad (aggiornati).
- **Impostazioni di ripiego:** se la fotocamera rifiuta la risoluzione 1280×720, lo script riprova con impostazioni più semplici.
- **iPhone e iPad:** il video parte muto e "inline", come richiede iOS.
- **Rotazione del telefono:** il riquadro si adatta quando il telefono passa da verticale a orizzontale.
- **Ritorno all'app:** se il telefono sospende la fotocamera mentre sei in un'altra app, al ritorno riparte da sola.
- **Più fotocamere:** se il computer ne ha più di una (webcam USB, fotocamere virtuali), compare il menu **Camera** per sceglierla. La scelta viene ricordata.
- **Fotocamera bloccata o occupata:** la pagina spiega cosa fare su quel dispositivo, per esempio come riattivare il permesso su iPhone, Android, Mac o Windows, o di chiudere Zoom/Teams se la stanno usando.
- **Browser interni delle app** (Instagram, Facebook, TikTok, LinkedIn…): di solito non possono usare la fotocamera. La pagina lo segnala, offre **Copy link** e su Android anche **Open in Chrome**.
- **Tracker:** se il tracciamento si blocca usando la scheda grafica, la pagina passa da sola a una modalità più lenta ma più compatibile.

## Da sapere

- La fotocamera funziona solo su HTTPS, che GitHub Pages fornisce automaticamente.
- La pagina scarica three.js e MediaPipe da `cdn.jsdelivr.net` e i modelli di tracciamento da `storage.googleapis.com`: serve una connessione internet.
- Un repository pubblico è visibile a chiunque, e lo è anche il sito.
- **Licenza dei modelli anatomici:** BodyParts3D, © The Database Center for Life Science, licenza CC Attribution-Share Alike 2.1 Japan. L'attribuzione è già nella pagina; i modelli derivati (inclusi nel file) restano sotto la stessa licenza.
- Non è uno strumento medico: l'anatomia è un modello di un adulto adattato alla tua testa, non una scansione.
