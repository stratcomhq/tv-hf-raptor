# 📺 Lista IPTV + EPG con Proxy

Benvenuto nella tua **lista IPTV personalizzata** con **EPG** integrata e supporto proxy, perfetta per goderti i tuoi contenuti preferiti ovunque ti trovi!

---

## 🌟 Cosa include la lista?

- **🎥 Pluto TV Italia**  
  Il meglio della TV italiana con tutti i canali Pluto TV sempre disponibili.

- **⚽ Eventi Sportivi Live**  
  Segui in diretta **calcio**, **basket** e altri sport. Non perderti neanche un'azione!

- **📡 Sky e altro ancora**  
  Contenuti esclusivi: film, serie TV, sport e molto di più direttamente da Sky.

---

## 🔗 Link Lista + EPG

Queste liste devono essere utilizzate con un proxy.

- **Lista M3U**  
  [`https://raw.githubusercontent.com/nzo66/TV/refs/heads/main/lista.m3u`](https://raw.githubusercontent.com/nzo66/TV/refs/heads/main/lista.m3u)

- **EPG XML**  
  [`https://raw.githubusercontent.com/nzo66/TV/refs/heads/main/epg.xml`](https://raw.githubusercontent.com/nzo66/TV/refs/heads/main/epg.xml)

Non sai come creare un proxy o vuoi una lista gia pronta usa questo link.

- **Lista M3U con Proxy**  
  [`https://nzo66-tvproxy.hf.space/proxy?url=https://raw.githubusercontent.com/nzo66/TV/refs/heads/main/lista.m3u`](https://nzo66-tvproxy.hf.space/proxy?<server-ip>/proxy?url=https://raw.githubusercontent.com/nzo66/TV/refs/heads/main/lista.m3u)

---

## 🔗 Link Film & MPD TEST

Queste liste devono essere utilizzate con mediaflow-proxy usando il link cosi.

- **Lista Film**  
  [`https://nzo66-mfpform3u.hf.space/proxy?<server-ip>:<password>&https://raw.githubusercontent.com/nzo66/TV/refs/heads/main/film.m3u`](https://nzo66-mfpform3u.hf.space/proxy?<server-ip>:<password>&https://raw.githubusercontent.com/nzo66/TV/refs/heads/main/film.m3u)

- **Lista MPD**  
  [`https://nzo66-mfpform3u.hf.space/proxy?<server-ip>:<password>&https://raw.githubusercontent.com/nzo66/TV/refs/heads/main/mpd.m3u`](https://nzo66-mfpform3u.hf.space/proxy?<server-ip>:<password>&https://raw.githubusercontent.com/nzo66/TV/refs/heads/main/mpd.m3u)

Sostituisci:

- `<server-ip>` con l'indirizzo IP del tuo server mediaflow-proxy  
- `<password>` con la password del tuo mediaflow-proxy  

---

## 📺 Come aggiungere la lista su Stremio

Per utilizzare questa lista IPTV su Stremio, dovrai usare l'addon **OMG Premium TV**:

### 🚀 Installazione OMG Premium TV

1. **Usa questo fork specifico**: [https://github.com/nzo66/OMG-Premium-TV](https://github.com/nzo66/OMG-Premium-TV)  
2. **Deploy su Docker** tramite Hugging Face o VPS seguendo la guida nel repository  
3. **Configura l'addon** inserendo:
   - **URL M3U**: Il link della lista M3U sopra indicato senza il proxy 
   - **URL EPG**: Il link dell'EPG XML sopra indicato  
   - **Abilita EPG**: Metti la spunta su Abilita EPG
   - **Proxy URL**: Url del tuo MFP
   - **Proxy Password**: Api Password del tuo MFP
   - **Forza Proxy**: Metti la spunta su Forza Proxy
   - **Intervallo Aggiornamento Playlist**: Metti 02:00
4. **Installa su Stremio** cliccando sul pulsante "INSTALLA SU STREMIO"

### ✨ Funzionalità disponibili

Con OMG Premium TV potrai sfruttare:
- Supporto playlist **M3U/M3U8** complete  
- **EPG integrata** con informazioni sui programmi  
- **Filtri per genere** e ricerca canali  
- **Proxy per maggiore compatibilità**  
- **Resolver Python** per stream speciali  
- **Backup e ripristino** della configurazione  

---

### ✅ Crea il tuo proxy personalizzato

- **Mediaflow Proxy**:  
  [mediaflow-proxy](https://github.com/mhdzumair/mediaflow-proxy)
  
- **Mediaflow Proxy Per HuggingFace**
  
  `(i canali non sempre funzionano su HuggingFace)`

  Usa questa repo ottimizzata: [hfmfp](https://github.com/nzo66/hfmfp)

- **TvProxy**:
  [tvproxy (repo GitHub)](https://github.com/nzo66/tvproxy)

  `usando questo proxy hai la possibilita' di installarlo su un qualsiasi dispositivo android grazie all'app Termux`

---

## ⚙️ Vuoi Personalizzare la lista

### 1. Fai il fork della repo

Avvia creando un fork della repository proxy.

### 2. Modifica il file `.env`.

---

### 🔁 Come proxare la lista con Mediaflow-Proxy?

Utilizza il seguente URL: `https://nzo66-mfpform3u.hf.space/proxy?<server-ip>:<password>&<url-lista>`

questo sara il link della tua lista da mettere nelle app iptv!

Sostituisci:

- `<server-ip>` con l'indirizzo IP del tuo server MFP
- `<password>` con la password del tuo mediaflow-proxy  
- `<url-lista>` con l'URL effettivo della tua lista M3U (es. quello GitHub)

Questo ti permetterà di servire la lista M3U attraverso il tuo proxy personale in modo sicuro e performante.

---

### 🔁 Come proxare la lista con TvProxy?

Utilizza il seguente URL: `https://<server-ip>/proxy?url=<url-lista>`

questo sara il link della tua lista da mettere nelle app iptv!

Sostituisci:

- `<server-ip>` con l'indirizzo IP del tuo server TvProxy
- `<url-lista>` con l'URL effettivo della tua lista M3U (es. quello GitHub)

Questo ti permetterà di servire la lista M3U attraverso il tuo proxy personale in modo sicuro e performante.

---

## 🚀 Esecuzione automatica con GitHub Actions

Dopo le modifiche:

1. Vai sulla sezione **Actions** della tua repo  
2. Avvia manualmente lo script  
3. Assicurati che **GitHub Actions sia abilitato** nella repository  

---

## 💡 Ottenere link M3U8 diretti per Daddylive con proxy HTTP su GitHub

Per ottenere i link M3U8 diretti per Daddylive e farli funzionare correttamente, è necessario configurare i proxy HTTP come variabile d'ambiente su GitHub. Questa variabile è specificamente `HTTP_PROXY`.

### Come configurare `HTTP_PROXY` su GitHub:

1.  **Accedi alle impostazioni del tuo repository GitHub**: Vai su `Settings` -> `Secrets and variables` -> `Actions`.
2.  **Aggiungi una nuova variabile**: Clicca su `New repository variable`.
3.  **Nome della variabile**: Inserisci `HTTP_PROXY`.
4.  **Valore della variabile**: Qui dovrai inserire i tuoi proxy. È fortemente consigliato utilizzare proxy di alta qualità per una maggiore stabilità. Puoi ottenerli da servizi come [webshare.io](https://www.webshare.io/).

    **Importante**: Per un funzionamento ottimale, avrai bisogno di **almeno due account proxy** da webshare.io. I proxy devono essere separati da una virgola (`,`).

    **Formato esempio per il valore di `HTTP_PROXY`**:
    `http://user1:pass1@ip1:port1,http://user2:pass2@ip2:port2`

    Assicurati che i proxy siano attivi e funzionanti.

Configurando questa variabile, le tue GitHub Actions utilizzeranno automaticamente questi proxy per risolvere i link M3U8 di Daddylive, garantendo una riproduzione fluida.

---

### Come ottenere proxy gratuiti da webshare.io:

1.  **Visita il sito web**: Vai su <mcurl name="https://www.webshare.io/" url="https://www.webshare.io/"></mcurl>.
2.  **Registrati per un account gratuito**: Clicca su "Get Started for Free" o "Sign Up" e crea un account. Non è richiesta una carta di credito.
3.  **Accedi alla dashboard**: Dopo la registrazione, verrai reindirizzato alla tua dashboard.
4.  **Scarica i proxy gratuiti**: Nella dashboard, cerca l'opzione per scaricare i tuoi proxy gratuiti. <mcreference link="https://www.webshare.io/" index="1">1</mcreference> Webshare.io offre 10 proxy gratuiti per account, con un limite di traffico di 1GB al mese. <mcreference link="https://www.webshare.io/" index="1">1</mcreference>

### Come estrarre la stringa del proxy da webshare.io:

1.  **Accedi alla tua dashboard di webshare.io**.
2.  Vai nella sezione Free > Proxy List, seleziona le seguenti opzioni:
    -   **Authentication Method**: `Username/Password`
    -   **Connection Method**: `Rotating Proxy Endpoint`
    -   **Proxy Protocol**: `HTTP`
3.  Clicca su "See example configurations" o un'opzione simile.
4.  Cerca l'esempio del comando `curl`. La stringa del proxy sarà la parte all'interno delle doppie virgolette, subito dopo `-x` o `--proxy`.
    -   **Esempio**: Se il comando `curl` è `curl -x "http://user:pass@ip:port/" http://example.com`, la stringa del proxy è `http://user:pass@ip:port` (assicurati di escludere la barra finale `/` se presente).

---

## 🤝 Hai bisogno di aiuto?

Apri una **issue** o proponi un miglioramento con una **pull request**.  
Contribuire è sempre benvenuto!
