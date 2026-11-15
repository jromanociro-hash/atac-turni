# ATAC Turni – prima versione PWA

Questa è una base installabile per iPhone, pensata per essere pubblicata su un hosting HTTPS e aggiunta alla schermata Home da Safari.

## Cosa funziona già
- Interfaccia responsive in stile scuro premium.
- Inserimento, modifica ed eliminazione manuale dei turni.
- Tipi: lavoro, riposo RS, Legge 104, VP provvisorio e altri permessi.
- Calendario mensile e dettaglio del giorno.
- Statistiche mensili e settimanali (VP esclusi dalle ore definitive).
- Calcolo indicativo dell'ora di partenza in base alla durata viaggio e all'anticipo.
- Salvataggio locale sul dispositivo.
- Backup JSON esportabile/importabile.
- Cache offline della struttura dell'app.

## Limiti importanti della prima versione
- Non è ancora collegata al portale ATAC.
- Non inserire credenziali in questa PWA: la sincronizzazione dovrà essere realizzata tramite un backend sicuro.
- Le notifiche programmate e il controllo automatico ogni venerdì alle 15 richiedono un servizio server-side; iOS non garantisce l'esecuzione puntuale di attività in background di una PWA.
- Il tempo di viaggio è per ora un valore predefinito modificabile, non un calcolo traffico live.

## Pubblicazione
Caricare il contenuto di questa cartella su un hosting statico HTTPS (ad esempio GitHub Pages, Netlify o Cloudflare Pages). Poi aprire l'indirizzo in Safari su iPhone → Condividi → Aggiungi alla schermata Home.

## Prossima fase
Collegare un backend con:
1. autenticazione e segreti conservati lato server;
2. sincronizzazione ATAC con sessione, attese robuste e gestione delle schermate intermedie;
3. lettura e confronto del solo intervallo di turni non ancora acquisito;
4. aggiornamento programmato del venerdì alle 15;
5. log diagnostici senza esporre credenziali o token.
