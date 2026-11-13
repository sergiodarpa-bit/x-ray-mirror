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

## Da sapere

- La fotocamera funziona solo su HTTPS, che GitHub Pages fornisce automaticamente.
- La pagina scarica three.js e MediaPipe da `cdn.jsdelivr.net` e i modelli di tracciamento da `storage.googleapis.com`: serve una connessione internet.
- Un repository pubblico è visibile a chiunque, e lo è anche il sito.
- **Licenza dei modelli anatomici:** BodyParts3D, © The Database Center for Life Science, licenza CC Attribution-Share Alike 2.1 Japan. L'attribuzione è già nella pagina; i modelli derivati (inclusi nel file) restano sotto la stessa licenza.
- Non è uno strumento medico: l'anatomia è un modello di un adulto adattato alla tua testa, non una scansione.
