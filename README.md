## CONSEGNA DAY 1

Creiamo con Laravel il nostro sistema di gestione del nostro Portfolio di progetti.
Oggi iniziamo un nuovo progetto che si arricchirà nel corso delle prossime lezioni: man mano aggiungeremo funzionalità e vedremo la nostra applicazione crescere ed evolvere.

Iniziamo con il definire il layout, modello, migrazione, controller e rotte necessarie per il sistema portfolio:

1. Autenticazione: si parte con l'autenticazione e la creazione di un layout per back-office
2. Creazione del modello Project con relativa migrazione, seeder, controller e rotte
3. Per la parte di back-office creiamo un resource controller Admin\ProjectController per gestire tutte le operazioni CRUD dei progetti
   Bonus
   Implementiamo la validazione dei dati dei Progetti nelle operazioni CRUD che lo richiedono usando due form requests.

## CONSEGNA DAY 2

Aggiungiamo una nuova entità Type. Questa entità rappresenta la tipologia di progetto ed è in relazione one to many con i progetti.
I task da svolgere sono:

-   creare la migration per la tabella types
-   creare il model Type
-   creare la migration di modifica per la tabella projects per aggiungere la chiave esterna
-   aggiungere ai model Type e Project i metodi per definire la relazione one to many
-   visualizzare nella pagina di dettaglio di un progetto la tipologia associata, se presente
-   permettere all'utente di associare una tipologia nella pagina di creazione e modifica di un progetto
-   gestire il salvataggio dell'associazione progetto-tipologia con opportune regole di validazione

### Bonus 1:

creare il seeder per il model Type.

### Bonus 2:

aggiungere le operazioni CRUD per il model Type, in modo da gestire le tipologie di progetto direttamente dal pannello di amministrazione.

## CONSEGNA DAY 3

Aggiungiamo una nuova entità Technology. Questa entità rappresenta le tecnologie utilizzate ed è in relazione many to many con i progetti.
I task da svolgere sono:

-   creare la migration per la tabella technologies
-   creare il model Technology
-   creare la migration per la tabella pivot project_technology
-   aggiungere ai model Technology e Project i metodi per definire la relazione many to many
-   visualizzare nella pagina di dettaglio di un progetto le tecnologie utilizzate, se presenti
-   permettere all'utente di associare le tecnologie nella pagina di creazione e modifica di un progetto
-   gestire il salvataggio dell'associazione progetto-tecnologie con opportune regole di validazione

### Bonus 1:

Creare il seeder per il model Technology.

### Bonus 2:

Aggiungere le operazioni CRUD per il model Technology, in modo da gestire le tecnologie utilizzate nei progetti direttamente dal pannello di amministrazione.

## CONSEGNA DAY 4

Aggiungiamo un'immagine ai nostri progetti.
Ricordiamoci di creare il symlink con l'apposito comando artisan e di aggiungere l'attributo enctype="multipart/form-data" ai form di creazione e di modifica!

### Bonus

Inviare una email quando viene creato un nuovo post

### Bonus 2

Permettere l'eliminazione dell'immagine del post dal form di modifica

## CONSEGNA DAY 5

### Milestone 1

Aggiungiamo al nostro progetto Laravel una nuovo Api/ProjectController. Questo controller risponderà a delle richieste via API e si occuperà di restituire la lista dei progetti presenti nel database in formato json.

### Milestone 2

Testiamo la chiamata API tramite Postman e assicuriamoci di ricevere i dati correttamente.

### Milestone 3

nome repo 2: vite-boolfolio
Iniziamo ad occuparci della parte front-office della nostra applicazione: creiamo un nuovo progetto Vue 3 con Vite e installiamo axios.
Colleghiamo questo progetto ad una repo separata.

### Milestone 4

Nel componente principale della nostra Vue App facciamo una chiamata API all’endpoint costruito nel progetto Laravel (milestone 1) e recuperiamo tutti i progetti dal nostro back-end.
Stampiamo in console i risultati e verifichiamo di ricevere i dati correttamente.

### Milestone 5

Creiamo un nuovo componente ProjectCard, che corrisponde ad una card per visualizzare un progetto. Utilizziamo questo componente per visualizzare tutti i progetti ricevuti tramite API.

### Bonus:

Gestire la paginazione dei risultati
Buon lavoro e buon divertimento!

### Consigli

Per modificare il colore della topbar di vscode in progetti specifici:
CTRL + SHIFT + P
Selezionate "Preferences: Open Workbench Settings (JSON)"
Incollare il seguente codice:

```
{
  "workbench.colorCustomizations": {
    "titleBar.activeBackground": CODICE_COLORE,
    "titleBar.activeForeground": "#fff"
  }
}
```

Io uso il verde "#117F4E" per Vue ed il rosso "#AC3535" per Laravel, vanno inseriti al posto di CODICE_COLORE
