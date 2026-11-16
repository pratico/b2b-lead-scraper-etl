# B2B Lead Scraper — Local-First Lead Generation ETL, Chrome MV3 Harvester & Multi-Channel Outreach CRM

🇬🇧 / 🇺🇸 **ENGLISH** | [🇮🇹 Vai alla versione in Italiano](#-italiano)

[![Portfolio](https://img.shields.io/badge/Portfolio-antoniangeloflore.com-0d6efd?style=flat-square)](https://antoniangeloflore.com)
[![Stack](https://img.shields.io/badge/Stack-Node.js%20%7C%20MySQL%20%7C%20HTMX%20%7C%20Chrome%20MV3-198754?style=flat-square)](https://github.com/pratico)
[![Architecture](https://img.shields.io/badge/Architecture-Local--First%20%2F%20Anti--Ban%20Pacing-dc3545?style=flat-square)](https://antoniangeloflore.com)

## Product Overview

**B2B Lead Scraper** is a local-first web platform designed for marketing agencies, B2B consultants, and sales operations teams that require a continuous, qualified pipeline of business leads.

Engineered to run locally on **Linux** alongside a dedicated **Google Chrome Extension (Manifest V3)**, the system automates the extraction and qualification of public business records by industry and geographic area, eliminates duplicates in a structured MySQL database, and orchestrates both **time-boxed email outreach** and **LinkedIn prospecting** through an integrated anti-ban CRM module.

## The Problem Solved

In real-world B2B prospecting, the true bottleneck is not closing deals—it is building clean, compliant contact pipelines without wasting engineering or sales hours:

- **Hours lost in manual prospecting:** Repetitive browsing, copying, and pasting of company contacts from public directories and search engines.
- **Fragmented & inconsistent spreadsheets:** Leads scattered across unstructured CSV files with missing fields, invalid emails, and inconsistent formatting.
- **Duplicate outreach & reputation damage:** Contacting the same prospect multiple times across different channels due to lack of centralized tracking.
- **Account bans from aggressive automation:** Cloud bots that blast identical messages without randomized delays, triggering SMTP blacklists or LinkedIn account restrictions.

**B2B Lead Scraper** centralizes the entire lifecycle—from local data harvesting and target segmentation to paced, trackable multi-channel outreach.

## Operator Workflow

From the operator's perspective, the end-to-end workflow is deterministic and streamlined:

1. **Target Definition & Local Harvesting (Chrome MV3 + X-Ray SERP):** Using the companion **Chrome Extension (Manifest V3)** on local Linux workstations and built-in Google X-Ray DOM parsers, the operator captures public business records and decision-maker profiles without cloud proxy overhead.
2. **Automated Normalization & Deduplication:** Incoming records are sanitized and cross-checked against unique database constraints, automatically discarding duplicates before insertion.
3. **Target Segmentation & Qualification:** Leads are segmented into operational target groups (e.g., SMEs/Web Agencies vs. Enterprise IT teams) with instant filtering by status, group, and dispatch dates.
4. **Time-Boxed & Paced Email Automation:** A background Node.js cron daemon dispatches personalized emails strictly within configured weekday schedules and business hours, applying randomized min-max delays (jitter) and daily hard limits to protect sender reputation.
5. **Integrated LinkedIn Outreach & Anti-Ban CRM:** A dedicated module organizes LinkedIn prospects by country and role, compiles personalized messages from JSON templates, tracks connection requests vs. direct messages, and enforces a **20-action/day safety guard** with a **5–10 minute randomized countdown timer**.
6. **Outcome:** A clean, deduplicated, and continuously updated B2B pipeline managed by a single operator in minutes per day.

## Key Features & Operational Benefits (ROI)

- **Hybrid Local Execution + Chrome Extension (MV3):** Captures structured data directly from the local browser session without expensive cloud scraping proxies. *Benefit: Maximum reliability, zero proxy costs, and full local control over collected records.*
- **Deterministic Deduplication Engine:** Enforces strict uniqueness across company domains, emails, and LinkedIn profile URLs. *Benefit: Zero duplicate outreach and protected brand reputation.*
- **Randomized Pacing & Time-Boxing Daemon:** Schedules email delivery only on active weekdays and target hours with randomized minute/second jitter and daily caps. *Benefit: High inbox deliverability and zero spam triggers.*
- **Built-in LinkedIn Outreach & Pacing Guard:** Tracks connection requests, direct messages, template IDs, and replies while enforcing daily caps and randomized cooldown timers. *Benefit: Safe, systematic LinkedIn prospecting without risking account restrictions.*
- **Reactive HTMX + Bootstrap 5 Back-Office:** Instant filtering, bulk group actions, and live status checkboxes without heavy SPA overhead. *Benefit: Fast single-operator execution with minimal cognitive friction.*

## High-Level Architecture & Stack

- **Node.js & Express:** Asynchronous backend runtime managing REST/HTMX endpoints, background cron daemons, and queue workers.
- **MySQL:** Relational storage ensuring strict referential integrity, unique indexing, and fast multi-criteria querying.
- **Chrome Extension (Manifest V3):** Local browser companion for structured DOM extraction from public business directories.
- **Bootstrap 5 & HTMX:** Lightweight, responsive operator dashboard with real-time partial DOM updates.
- **Linux Environment:** Native local execution platform engineered for stability and unattended background workers.

## Confidentiality Notice & B2B Licensing

🔒 **Proprietary Software Asset (All Rights Reserved):** This repository serves as a functional and architectural showcase within the Professional Portfolio ([https://antoniangeloflore.com](https://antoniangeloflore.com) — *note: portal and technical video pitches are currently in Italian, with full English B2B communication and delivery*). For operational security and NDA compliance, the source code and internal extraction modules are not publicly exposed.

🤝 **Custom B2B Pipelines & White-Label Inquiries:** Available for custom ETL/outreach automation, white-label SaaS licensing, and asynchronous technical consultations (no calls required). Connect via [antoniangeloflore.com](https://antoniangeloflore.com) or [LinkedIn](https://www.linkedin.com/in/antoniangelo-f-30003622/).

---

<a name="-italiano"></a>
## 🇮🇹 ITALIANO

# B2B Lead Scraper — Piattaforma Locale di Lead Generation ETL, Estensione Chrome MV3 & CRM Outreach Multicanale

## Panoramica del Prodotto

**B2B Lead Scraper** è una piattaforma web local-first pensata per agenzie di marketing, consulenti commerciali e team B2B che necessitano di un flusso continuo e qualificato di contatti aziendali.

Progettata per operare in ambiente locale **Linux** affiancata da un'apposita **Estensione Chrome (Manifest V3)**, la piattaforma automatizza la raccolta e la qualifica di anagrafiche aziendali pubbliche per settore e area geografica, elimina i doppioni in un database MySQL strutturato e gestisce sia le **campagne email temporizzate** sia il **contatto su LinkedIn** tramite un modulo CRM anti-ban integrato.

## Il Problema Risolto

Nella prospezione B2B reale, il vero collo di bottiglia non è la vendita, ma la costruzione ordinata e sostenibile delle liste contatti:

- **Tempo perso nella ricerca manuale:** ore spese a navigare, copiare e incollare dati aziendali da directory pubbliche e motori di ricerca.
- **Dati incoerenti e sparsi:** anagrafiche salvate in fogli di calcolo disordinati, con campi mancanti e formati non uniformi.
- **Doppioni e contatti ripetuti:** lo stesso prospect contattato più volte per mancanza di tracciamento centralizzato, con danno reputazionale.
- **Blocchi account da invii aggressivi:** automazioni prive di ritardi casuali e limiti giornalieri che compromettono la deliverability email o causano restrizioni sui profili LinkedIn.

**B2B Lead Scraper** centralizza l'intero ciclo operativo: dall'acquisizione locale alla segmentazione, fino alla gestione tracciata dei follow-up multicanale.

## Come Funziona (Flusso Operativo Utente)

Il funzionamento pratico della piattaforma segue un flusso lineare e deterministico:

1. **Definizione target e acquisizione locale (Estensione Chrome MV3 + X-Ray SERP):** tramite l'estensione Chrome dedicata in ambiente locale Linux e i parser DOM integrati, l'operatore acquisisce anagrafiche aziendali pubbliche e profili professionali senza dipendere da costosi proxy cloud.
2. **Pulizia e deduplicazione automatica:** i dati raccolti vengono normalizzati e verificati contro i vincoli di unicità del database MySQL, scartando automaticamente ogni duplicato.
3. **Segmentazione e qualifica dell'anagrafica:** i lead vengono suddivisi per gruppi target operativi con filtri istantanei per stato, gruppo e data di spedizione.
4. **Automazione email temporizzata (Pacing & Time-Boxing):** un demone asincrono Node.js invia le email esclusivamente nei giorni lavorativi e nelle fasce orarie configurate, applicando ritardi casuali (jitter min-max) e tetti massimi giornalieri.
5. **Modulo CRM LinkedIn Anti-Ban integrato:** una sezione dedicata organizza i contatti LinkedIn per paese e ruolo, genera messaggi personalizzati da template JSON, traccia separatamente richieste di collegamento e messaggi diretti e applica una **soglia di sicurezza di 20 azioni/giorno** con **timer randomizzato da 5 a 10 minuti**.
6. **Risultato finale:** una pipeline commerciale pulita, tracciata e priva di duplicati gestita da un solo operatore in pochi minuti al giorno.

## Funzionalità Principali & Vantaggi Operativi (ROI)

- **Esecuzione Locale + Estensione Chrome (MV3):** acquisizione strutturata direttamente dal browser locale senza infrastrutture proxy esterne. *Vantaggio: massima affidabilità operativa e controllo totale sui dati raccolti.*
- **Deduplicazione deterministica:** controllo rigoroso di unicità su domini aziendali, indirizzi email e URL dei profili LinkedIn. *Vantaggio: zero contatti duplicati e reputazione aziendale protetta.*
- **Demone Email con Pacing Randomizzato e Time-Boxing:** invii schedulati solo nei giorni e negli orari impostati con intervalli casuali. *Vantaggio: elevata deliverability e protezione dagli spam filter.*
- **CRM LinkedIn con Protezione Anti-Ban:** gestione completa di richieste di collegamento, messaggi diretti, template utilizzati e risposte con contatore giornaliero e countdown di raffreddamento. *Vantaggio: prospezione sistematica senza rischi per l'account.*
- **Interfaccia Reattiva Bootstrap 5 + HTMX:** filtri istantanei, azioni massive per gruppo e salvataggio live delle checkbox. *Vantaggio: operatività rapida senza sovraccarico.*

## Tecnologie Utilizzate (Ad Alto Livello)

- **Node.js ed Express:** runtime e framework backend per la gestione di rotte HTMX/REST, code asincrone e demoni cron.
- **MySQL:** database relazionale per anagrafiche strutturate, vincoli di unicità e interrogazioni multi-criterio ad alte prestazioni.
- **Chrome Extension (Manifest V3):** estensione browser locale per l'estrazione strutturata da fonti pubbliche.
- **Bootstrap 5 & HTMX:** interfaccia web leggera e reattiva con aggiornamenti parziali del DOM in tempo reale.
- **Ambiente Linux:** piattaforma di esecuzione nativa progettata per stabilità e processi asincroni continui.

## Nota di Riservatezza & Collaborazioni B2B

🔒 **Asset Software Proprietario (Tutti i diritti riservati):** Questo repository ha finalità di presentazione funzionale e architetturale per il Portfolio Professionale ([https://antoniangeloflore.com](https://antoniangeloflore.com)). Per ragioni di sicurezza operativa e accordi di riservatezza (NDA), il codice sorgente e i moduli interni di estrazione non sono esposti pubblicamente.

🤝 **Sviluppo Custom & Licensing White-Label:** Disponibile per pipeline B2B su misura, licenze White-Label e consulenze tecniche asincrone (zero call). Contatti su [antoniangeloflore.com](https://antoniangeloflore.com) o su [LinkedIn](https://www.linkedin.com/in/antoniangelo-f-30003622/).
