# SmartTraffic

## Piattaforma per la gestione intelligente della viabilità urbana
L'obiettivo del progetto è realizzare SmartTraffic, una piattaforma per la gestione della viabilità in una smart city. La piattaforma consente di monitorare le condizioni del traffico, gestire segnalazioni relative a problemi sulla rete stradale, coordinare interventi sulla viabilità e informare i cittadini sulle eventuali criticità.
La rete stradale della città è rappresentata attraverso un insieme di tratti stradali, ciascuno caratterizzato da un nome, una posizione e uno stato della viabilità. Ogni tratto stradale può trovarsi in uno dei seguenti stati: regolare, rallentato, congestionato o chiuso. I tratti e i luoghi di interesse possono essere associati a elementi geografici resi disponibili da un sistema cartografico basato su OpenStreetMap (OSM).
La piattaforma consente di consultare le informazioni sulla viabilità in un contesto cartografico, mostrando sulla mappa tratti stradali, segnalazioni, avvisi e chiusure. Le informazioni operative di SmartTraffic restano distinte dai dati cartografici di riferimento, pur potendo essere associate a essi mediante identificativi o riferimenti geografici.
La piattaforma raccoglie informazioni sul traffico attraverso sensori esterni e segnalazioni inviate dai cittadini. Gli operatori comunali possono analizzare le segnalazioni, gestire gli interventi e disporre modifiche temporanee alla viabilità.

## Si immaginano almeno i seguenti attori.

### Operatore della Viabilità
L'Operatore della Viabilità è un membro del personale comunale incaricato di monitorare e gestire la circolazione stradale.
Può consultare lo stato di tutti i tratti stradali della città e visualizzare le segnalazioni inviate dai cittadini. Può prendere in carico una segnalazione, verificarne la fondatezza e, se necessario, aprire un intervento.
Ogni segnalazione segue un ciclo di vita composto dai seguenti stati: inviata, in verifica, risolta e respinta.
L'Operatore può inoltre modificare lo stato di un tratto stradale in presenza di situazioni che richiedono provvedimenti sulla circolazione.

### Responsabile della Viabilità
Il Responsabile della Viabilità è un Operatore con privilegi aggiuntivi, incaricato di coordinare gli interventi sulla rete stradale.
Può programmare chiusure temporanee di tratti stradali per lavori, manifestazioni o altre esigenze, specificando la motivazione, la data e l'ora di inizio e fine.
Può inoltre assegnare gli interventi alle squadre operative e monitorarne l'avanzamento.
Quando un intervento viene completato, il Responsabile può autorizzare la riapertura del tratto stradale interessato.

### Squadra Operativa
La Squadra Operativa è incaricata di eseguire gli interventi sulla rete stradale, ad esempio in seguito a incidenti, ostacoli sulla carreggiata o problemi infrastrutturali.
Può consultare gli interventi che le sono stati assegnati e aggiornarne lo stato.
Ogni intervento segue un ciclo di vita composto da quattro stati: programmato, assegnato, in corso e completato.
Al termine dell'intervento, la squadra inserisce un rapporto contenente una descrizione delle attività svolte e l'eventuale presenza di criticità non risolte.

### Cittadino
Il Cittadino è un utente registrato che può consultare le condizioni del traffico e inviare segnalazioni relative a problemi sulla rete stradale.
Ogni segnalazione deve riferirsi a uno specifico tratto stradale e contenere una categoria (incidente, ostacolo, dissesto stradale o altro) e una descrizione del problema. Il tratto o il luogo interessato può essere individuato anche attraverso una mappa.
Il Cittadino può visualizzare lo stato delle proprie segnalazioni e ricevere aggiornamenti quando queste vengono prese in carico o risolte.

### Visitatore
Il Visitatore è un utente non autenticato che può consultare liberamente le informazioni pubbliche sulla viabilità urbana.
Può visualizzare lo stato corrente dei tratti stradali, le chiusure programmate e gli eventuali avvisi relativi a incidenti o congestioni.

### Sistema di Monitoraggio del Traffico
Il Sistema di Monitoraggio del Traffico è un servizio esterno che raccoglie dati da sensori distribuiti lungo la rete stradale.
Per ogni tratto stradale monitorato, fornisce periodicamente informazioni relative al numero di veicoli rilevati e alla velocità media di percorrenza.
La piattaforma utilizza queste informazioni per determinare lo stato del traffico, secondo soglie configurabili dagli operatori.

### Sistema di Notifiche
Il Sistema di Notifiche è un servizio esterno utilizzato per inviare comunicazioni agli utenti.
La piattaforma lo utilizza per informare i cittadini delle variazioni significative della viabilità sui tratti stradali di loro interesse e per comunicare gli aggiornamenti relativi alle segnalazioni inviate.

### Sistema Cartografico OpenStreetMap
Il Sistema Cartografico OpenStreetMap è un sistema secondario che rende disponibili dati geografici relativi a strade e luoghi, utili a identificare e rappresentare gli elementi della rete viaria. SmartTraffic interagisce con tale sistema attraverso interfacce applicative per consultare informazioni cartografiche e per mostrare i punti di interesse attraverso la mappa

## Vincoli e Dettagli Tecnici
Il progetto deve essere sviluppato in Java e successivamente portato su Spring Boot.
Lo strato di presentazione deve consentire una rappresentazione cartografica delle informazioni pubbliche sulla viabilità e delle segnalazioni.
Si devono utilizzare almeno due design pattern diversi dal Singleton.
Le interazioni con il Sistema di Monitoraggio del Traffico e con il Sistema di Notifiche possono essere simulate.
L’interazione con il sistema cartografico deve invece essere dimostrabile almeno sui dati geografici necessari ai casi d’uso
