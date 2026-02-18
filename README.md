# 🥁 KitVault  
### Marketplace di Drum Kit e Sample Pack

**KitVault** è una piattaforma web dedicata a producer, beatmaker e sound designer che vogliono condividere o vendere i propri drum kit e sample pack.  
Il progetto offre un ambiente moderno, sicuro e intuitivo per caricare contenuti musicali, ascoltare anteprime, acquistare kit e scoprire nuovi creator tramite una mappa interattiva.

Sviluppato come progetto finale, KitVault integra tutte le tecnologie richieste: sicurezza, sessioni, cookie, prepared statements, transazioni, API esterne, AJAX, MVC e un database relazionale avanzato.

---

## 🚀 Funzionalità principali

### 👤 Gestione utenti
- Registrazione con validazione HTML5, JS e PHP  
- Login con sessioni e cookie “Ricordami”  
- Autenticazione a due fattori tramite email  
- Dashboard personale per gestire kit, profilo e vendite  

### 🎵 Gestione dei contenuti musicali
- Upload di drum kit e sample pack (ZIP + anteprime audio)  
- Player audio integrato  
- Tag, generi musicali, descrizioni  
- Commenti e rating tramite AJAX  

### 🛒 Sistema di acquisto
- Carrello persistente tramite sessioni  
- Checkout con pagamento simulato (Stripe test mode)  
- Transazioni SQL per garantire consistenza  
- `SELECT ... FOR UPDATE` per evitare acquisti concorrenti  
- Email di conferma ordine tramite API esterna  

### 🌍 Mappa dei producer
- Integrazione con **Google Maps API**  
- Ogni producer può impostare la propria posizione  
- Mappa interattiva con marker e link ai profili  

### 🔍 Ricerca avanzata (AJAX)
- Ricerca live per nome, tag, genere  
- Filtri dinamici senza ricaricare la pagina  
- Ordinamento per popolarità, prezzo o data  

### ⭐ Funzionalità social
- Commenti AJAX  
- Wishlist / preferiti  
- Profilo pubblico del producer  

---

## 🗄️ Struttura del database

Il database segue un modello relazionale avanzato con 8–10 tabelle principali:

- `users`  
- `producers_profiles`  
- `kits`  
- `samples`  
- `orders`  
- `order_items`  
- `comments`  
- `ratings`  
- `favorites`  
- `transactions_log`  

Sono presenti chiavi esterne, relazioni 1‑N e N‑N, vincoli di integrità e indici per ottimizzare le query.

---

## 🧱 Architettura MVC

KitVault utilizza il pattern **Model–View–Controller**:

- **Model** → gestione database, query, transazioni  
- **View** → pagine HTML/CSS responsive  
- **Controller** → logica applicativa, validazioni, routing  

Questa struttura garantisce modularità, manutenibilità e chiarezza del codice.

---

## 🔐 Sicurezza

- Sanitizzazione input con `filter_var`, `htmlspecialchars`, prepared statements  
- Protezione CSRF tramite token  
- Sessioni sicure per autenticazione e aree riservate  
- Cookie con scadenza e flag HttpOnly  
- Validazioni lato client e lato server  

---

## 🌐 Tecnologie esterne integrate

- **Google Maps API** → mappa dei producer  
- **SendGrid/Postmark** → invio email (registrazione, MFA, conferma ordine)  
- **Stripe (test mode)** → simulazione pagamenti  

---

## 📱 Front-end

- Layout responsive (Flexbox / Grid)  
- Componenti AJAX per ricerca, commenti e player audio  
- Interfaccia moderna e intuitiva  

---

## 🎤 Conclusione

**KitVault** è un progetto completo e professionale che integra:

- Sicurezza avanzata  
- Gestione utenti  
- Upload multimediale  
- Pagamenti simulati  
- API esterne  
- AJAX  
- MVC  
- Database complesso  

Il risultato è una piattaforma creativa e funzionale, ideale per dimostrare competenze full‑stack e passione per la musica.

---

## 📄 Licenza
Progetto sviluppato per scopi didattici.
