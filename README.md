🌆 La Città Strana — VR (con controller)
Una città qualunque, in VR. Cammini con i controller del Quest — e vedrai le tue mani (stilizzate) al posto dei controller stessi. Parli con la gente, vai a dormire quando vuoi. Ma ogni giorno che passa, qualcosa è un po' più strano. Da qualche parte c'è un vicolo che, se guardi abbastanza a fondo, ti porta fuori dalla simulazione.
Costruito con Three.js + WebXR, un unico file HTML, per Meta Quest 3S.
🚀 Pubblicarlo su GitHub Pages
Crea un repository su GitHub e carica index.html (e questo README.md).
Settings → Pages → branch main, cartella /root. Otterrai un link tipo:
https://<tuo-utente>.github.io/citta-strana/
Apri il link nel browser del Quest 3S, controller in mano, e tocca "Entra in VR".
WebXR richiede HTTPS: GitHub Pages lo fornisce automaticamente. Aprire il file in locale con doppio click non farà comparire il pulsante VR.
🎮 Controlli
Azione
Controller
Camminare
Stick sinistro
Girarsi (a scatti, per il comfort)
Stick destro
Interagire (parlare, dormire, aprire il vicolo, tornare dal portale)
Grilletto
Volare nel vuoto (dopo l'uscita dalla simulazione)
Tieni premuto il grilletto
Al posto dei controller vedrai due mani stilizzate — è un aspetto semplificato (non seguono le dita reali), ma sostituisce i blocchi grigi dei controller con qualcosa che sembra davvero "tue mani".
✋ Come si gioca
Parlare con un NPC: avvicinati e premi il grilletto — apparirà una nuvoletta con quello che ha da dirti. Le frasi cambiano (e si fanno più inquietanti) col passare dei giorni.
Andare a dormire: c'è un letto vicino a una casa nella città. Avvicinati e premi il grilletto per far passare il giorno.
Il vicolo segreto: si trova stretto tra due edifici. All'inizio non succede nulla, ma dal terzo giorno in poi, premendo il grilletto in fondo al vicolo, verrai risucchiato fuori dalla simulazione: un vuoto fatto di codice che cade, dove puoi volare liberamente tenendo il grilletto premuto. Un portale luminoso ti riporta in città.
Ci sono due bar in città (Neon Cat e Zion Bar) con i loro avventori.
🎨 Novità grafiche
Bloom (effetto luce/bagliore) sulle insegne al neon, i lampioni, il portale e la porta del vicolo — dà molta più atmosfera notturna.
Sole visibile in cielo con bagliore, luce d'ambiente più morbida.
Piante in vaso vicino ai bar e a casa.
Pulviscolo/lucciole sospese nell'aria per dare profondità alla scena.
Se noti cali di prestazioni nel visore, apri index.html e cerca la riga const ENABLE_BLOOM = true; vicino all'inizio dello script: mettila su false per disattivare il bloom (è l'effetto più pesante).
🛠️ Personalizzarlo
Tutto il codice è in index.html:
buildingDefs: posizione ed edifici della città
npcDefs e DIALOGUE_TIERS: dove sono gli NPC e cosa dicono nei vari giorni
SECRET_DAY_THRESHOLD: da quale giorno si apre il vicolo segreto
advanceDay(): cosa cambia ogni giorno (colore del cielo, nebbia, frequenza dei glitch)
bloomPass: parametri del bagliore (forza, raggio, soglia)
🔮 Note e limiti di questa versione
Il movimento è "a piedi" con lo stick (con collisione semplice contro gli edifici in città); nel vuoto non c'è collisione, puoi volare ovunque.
Il vicolo è volutamente stretto: è un passaggio segreto, non una strada normale.
Da computer (senza visore) puoi comunque vedere la scena e guardarti intorno col mouse, ma l'interazione richiede i controller in VR.
Prossimi passi possibili: audio ambientale, più NPC con dialoghi propri, un vero e proprio "Roblox Studio" per scriptare le scene via HTML/JS (ne avevamo parlato!).
📄 Licenza
Fai quello che vuoi con questo progetto: modificalo, condividilo, pubblicalo come tuo.
