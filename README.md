# Progetto SOASEC Front-End

Progetto esame Sicurezza delle Architetture Orientate ai Servizi: [Demo App Front-End](https://antonioacademy10.github.io/progetto-soasec-github-pages/#/)

# Getting Started

## Pre-Requisiti

Affinchè sia possibile testare il progetto tramite la pagina hostata su GitHub Pages bisognerà avviare i seguenti server:

 - Server NodeJS (Services)
 - Server Keycloak (Auth)
 - Server MongoDB (Storage)

Reperibili al seguente [repository](https://github.com/antonioacademy10/progetto-soasec).

## Framework/Linguaggi utilizzati

 - [Flutter](https://www.flutter.dev/)
 - [Dart](https://www.dart.dev/)


# Installazione

Affinchè sia possibile usufruire del progetto nella sua interezza, anche se non vi è la necessità di installare alcun software bisogna tuttavia effettuare alcune operazioni:

Anzitutto bisognerà modificare il file **hosts** al fine di rendere compatibile il token JWT ricevuto tramite Keycloak.

Per far ciò quindi bisognerà eseguire tramite terminale il seguente comando:

> sudo nano /etc/hosts

Ed infine aggiungere la seguente:

> 127.0.0.1 keycloak

Una volta fatto ciò, una volta connessi alla pagina GitHub Pages, da Chrome, bisognerà:

1. Cliccare sul *lucchetto* di fianco all'url corrente
2. Selezionare **Impostazioni Sito**
3. Impostare **Contenuti non sicuri** su **Consenti**

Tale procedura risulta **necessaria** in quanto essendo il server hostato su localhost mediante risolutore di nome *127.0.0.1 keycloak*, vi sono alcune richieste eseguite mediante **http** ed altre eseguite in **https**.
Per default policy, Chrome bloccherà l'interoperabilità tra le due tipologie di richieste, rendendo impossibile la comunicazione con il server Keycloak.

# Utilizzo
L'applicazione consiste in due differenti parti:

- Pubblica
- Privata

Una volta aperta l'applicazione, vi sarà presentata la lista dei Candidati "Mock" i quali saranno pre-inseriti all'interno del Server di Storage. 
Per poter effettuare qualsiasi interazione con tali dati, bisognerà quindi procedere al login per poter accedere alla parte privata.

Sono presenti due differenti tipologie di utenti:

> 
>antonio.elefante
>123456789 
>admin

Oppure

> salvatore.ambrosio
>Password123!
>user

In funzione del ruolo, sarà quindi possibile interagire in due differenti modi con l'applicazione:

- Admin: Create / Delete
- User: Update

# Contatti

Antonio Elefante - antonioacademy10@gmail.com
Salvatore Ambrosio
