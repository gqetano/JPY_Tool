# Logo Blob Tool — Grana

Tool statico pronto per GitHub Pages. Non richiede installazione, build o server.

Su desktop l'interfaccia occupa l'intera viewport senza scorrimento della pagina: tutti i controlli, incluso **Scarica PNG HD**, sono raccolti nella colonna a sinistra e il canvas occupa lo spazio restante. Il selettore del file viene mostrato direttamente senza la dicitura visibile “Immagine”. Gli elenchi che possono crescere oltre lo spazio disponibile mantengono uno scorrimento interno. Su mobile il canvas resta fisso nella parte superiore, mentre la colonna dei controlli scorre indipendentemente sotto l'anteprima.

Questa variante aggiunge una grana procedurale stabile. La sezione **Grana** contiene direttamente lo slider, inizialmente impostato su `10`, e lo switch per accendere o spegnere l'effetto. La grana viene ricalcolata anche nel PNG HD.

All'apertura viene mostrato il logo del cliente incorporato nel tool. Il comando **Immagine** permette comunque di caricare temporaneamente qualsiasi altra immagine. Lo slider **Dimensione** la ridimensiona dal `25%` al `100%`, mantenendola centrata e proporzionata nell'anteprima e nel PNG esportato.

Lo switch **Effetto globale** alterna tra la composizione elaborata e il logo originale. Quando l'effetto è spento, il logo usa il colore del **Livello 1**; anche il PNG esportato segue lo stato dello switch.

## Pubblicazione

1. Crea un repository GitHub.
2. Carica `index.html` e `.nojekyll` nella cartella principale del repository.
3. Apri **Settings → Pages**.
4. In **Build and deployment**, scegli **Deploy from a branch**.
5. Seleziona il branch `main`, la cartella `/(root)` e salva.

Il tool elabora le immagini localmente nel browser: il logo caricato non viene inviato a un server.

La sfocatura include un sistema di compatibilità automatico per Safari e iOS meno recenti: se il browser non supporta il filtro nativo del canvas, il tool usa una sfocatura software equivalente. Il fallback viene applicato sia all'anteprima sia al PNG HD.

Ogni livello dispone di colore, **Morbidezza** ed **Espansione** indipendenti. Seleziona un livello per modificarlo, usa **Aggiungi livello** o **Duplica** e trascina qualsiasi punto della sua riga per riordinarlo. Durante lo spostamento compaiono un'anteprima semitrasparente e una linea che indica la nuova posizione. Lo slider **Espansione** cresce in modo intuitivo verso destra e copre l'intervallo completo da `1` a `255`.

**🎲 Genera** crea una nuova combinazione cromatica senza salvarla automaticamente. **Salva** conserva la palette corrente — anche se creata manualmente — per la durata della sessione del browser. **Scarica PNG HD** ricalcola ed esporta il risultato a `3300 × 2100 px`.

Il comando **Sfondo** permette di attivare un colore pieno da includere nel PNG. Quando è disattivato, l'esportazione conserva la trasparenza.
