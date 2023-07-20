# APPWEB

Il sistema si propone di risolvere il problema del monitoraggio di determinati parametri a domicilio con l'obiettivo di visualizzare lo stato di salute di una persona, nel particolare caso in questione un atleta o un paziente.
L'architettura è costituita da:
1. i dispositivi indossabili polar verity sense e polar H10
2. un'app android che permette l'acquisizione dei dati tramite BLE ANT+, la possibilità di aggiungere parametri misurati dall'utente in questione, come pressione arteriosa e diabete, la possibilità di aggiungere eventuali esercizi svolti dall'utente, la possibilità di visualizzare i propri dati in modo intellegibile attraverso dei grafici [repo app android](https://github.com/UniSalento-IDALab-IoTCourse-2022-2023/wot-project-part1-AndroidApp-DegiorgiProto)
3. un'app web utilizzabile dal medico che dà la possibilità di visualizzare i propri pazienti e i relativi dati acquisiti e aggiunti attraverso dei grafici [repo app web](https://github.com/UniSalento-IDALab-IoTCourse-2022-2023/wot-project-part3-WebApp-DegiorgiProto)
4. un backend costituito da un server che fa da intermediario con il database che raccoglie i dati acquisiti e che permette quindi di aggiungerli e prelevarli per la visualizzazione, e il database stesso. [repo backend](https://github.com/UniSalento-IDALab-IoTCourse-2022-2023/wot-project-part2-Backend-DegiorgiProto)


## Operazioni preliminari

Bisogna installare la libreria json per elaborare i dati in formato json
```
npm install json
```

Questa repository riguarda l'implementazione di una app web con lo scopo di essere utilizzata dal medico.
I file in html creano lo scheletro delle pagine della web app, cui è aggiunto lo stile grazie ai file css. I file html tramite i form vanno a interrogare il server nodejs interfacciandosi con il database consentendo al medico di effettuare le operazioni di login e registrazione, mentre le operazioni di visualizzazione dei valori acquisiti dai suoi pazienti tramite la diagnostica domestica sono possibili grazie ai file handlebars che consentono di usare lo stesso scheletro di pagina html ma dinamicamente aggiornati con i dati presi dal db.
