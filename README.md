# 🌍 Climate Monitoring
---
## Descrizione
Climate Monitoring è un'applicazione finalizzata alla rilevazione e all'analisi di parametri climatici forniti da centri di monitoraggio sul territorio italiano.  
Il sistema rende disponibili, sia a operatori ambientali sia a comuni cittadini, i dati climatici relativi alla propria zona di interesse.  
Gli operatori possono creare nuove stazioni meteorologiche e inserire i vari parametri rilevati, mentre i cittadini possono visualizzare le previsioni meteorologiche.

## 🏗️ Architettura del Sistema

Il sistema è strutturato in **tre moduli principali** che comunicano tra loro tramite **RMI (Remote Method Invocation)**:

- **`org.a3b.clientCM`**  
  Gestisce il lato client e l'interfaccia grafica (GUI).

- **`org.a3b.serverCM`**  
  Gestisce il lato server, la connessione al database e la distribuzione del sistema.

- **`org.a3b.commons`**  
  Contiene le risorse condivise e i modelli di dati utilizzati da entrambi i moduli.

---

## 📊 Funzionalità e Database

L'applicazione consente di:
- Creare nuovi **centri di monitoraggio**
- Inserire **misurazioni climatiche**
- Visualizzare **aree geografiche** e **operatori registrati**

Il database **PostgreSQL (`dbCM`)** gestisce le seguenti entità:

- **CentriMonitoraggio**  
  Informazioni sui centri registrati.

- **CoordinateMonitoraggio**  
  Aree geografiche con latitudine e longitudine separate per facilitare la manipolazione applicativa.

- **OperatoriRegistrati**  
  Dettagli degli operatori autorizzati.

- **ParametriClimatici**  
  Record delle misurazioni climatiche:
  - Vento  
  - Umidità  
  - Pressione  
  - Temperatura  
  - Precipitazioni  
  - Ghiacciai  

  Tutti i parametri sono misurati su una **scala da 1 a 5**.

---

## 🚀 Installazione e Setup

### Requisiti di Sistema
- **Java JDK 17** o superiore  
- **Sistema operativo a 64 bit**  
  (testato su Arch Linux e Windows 11)
- **Server PostgreSQL**

---

## 👥 Autori
- **Michael Bernasconi**
- **Beatrice Balzarini**
- **Iuri Antico**
- **Gabriele Borgia**
