# Esame Istologico della Placenta — v4.0

**Strumento diagnostico per refertazione sistematica dell'istologia placentare.**  
SC Anatomia Patologica · ASST Fatebenefratelli-Sacco, Milano

---

## Struttura del tool

### 1 · Macroscopico
- EGA (settimane + giorni)
- Peso placentare con alert orientativo (% del peso atteso per EGA; tabella interna non sostitutiva di curve percentile validate — cfr. Pinar et al. 2011)
- Spessore (alert se <15 mm o >35 mm)
- Aspetto superficie fetale, colorito, lesioni macroscopiche evidenti
- Cordone: lunghezza (alert se <30 cm o >80 cm), inserzione, numero vasi (alert se arteria singola), aspetto

### 2 · Campionamento
- Numero sezioni disco placentare
- Membrane (campionate / non campionate / non disponibili)
- Cordone (campionato / non campionato)
- Lesioni macroscopiche campionate (sì / no / n.a.)

### 3 · Pilastri Fondamentali
- EGA istologica (compatibile / più precoce / più tardiva)
- Maturazione villare: adeguata · intermedia · ritardata (DVM) · accelerata (AVM) · degenerativa
- Nodi sinciziali (fisiologici / aumentati >30% — con nota che il dato isolato è scivoloso / ridotti)
- Fibrina perivillosa (assente · focale · estesa >25% — con formula condizionale per MPFD)

### 4 · MVM — Maternal Vascular Malperfusion
Sezione modulare: ogni voce è opzionale e indipendente.

**Infarti placentari** (checkbox separata):
- Estensione: focale · multifocale · estesa (>25%)
- Localizzazione: periferica/subculorale · centrale · diffusa
- % parenchima coinvolto (stima)
- Aspetto temporale: recenti · organizzati · misti
- Contesto clinico: a termine senza complicanze · precoci/IUGR/preeclampsia · morte endouterina

**Lesioni vascolari materne** (checkbox indipendenti):
- Arteriopatia deciduale (decidual arteriopathy)
- Aterosi acuta (foam cell arteriopathy)
- Necrosi fibrinoide arterie spirali
- Ipoplasia villare distale
- Accelerated villous maturation
- Nodi sinciziali aumentati (>30% villi terminali)

Note: il commento clinico-patologico usa `mvm_has_findings` — si attiva solo se almeno una sottovoce è selezionata. Se MVM è checkata ma vuota, il tool avvisa di verificare la selezione.

### 5 · FVM — Fetal Vascular Malperfusion
Checkbox indipendenti:
- Trombosi grossi vasi fetali coriali
- Villi con karyorrhexis stromale-vascolare
- Villi avascolari
- Eritrociti nucleati in eccesso
- Ipercoiling del cordone
- Nodo vero (true knot)

Distribuzione: segmentale · globale/diffusa · focale  
Stima % parenchima coinvolto

### 6 · Villite
- Grado: lieve · moderata · severa
- Distribuzione: focale · multifocale · diffusa
- Infiltrato prevalente: linfocitario (CD8+) · plasmacellule · granulomi · inclusi citomegalici · misto
- Eziologia: **VUE** ("quadro compatibile con VUE, in assenza di criteri morfologici o clinici per eziologia infettiva") · **sospetta infettiva** ("morfologia non escludente — richiede correlazione clinico-sierologica")
- Griglia morfologica orientativa embedded (VUE / Treponema / granulomi / CMV / pattern severo)

### 7 · Corioamnionite — criteri Amsterdam
- MIR (risposta materna): Grado 1 subamniotica · Grado 2 corionica · Grado 3 necrotizzante
- FIR (risposta fetale): assente · Grado 1 flebite/arterite · Grado 2 vasculite corionica · Grado 3 funisite necrotizzante

### 8 · Calcificazioni
- Entità: scarse (fisiologiche) · moderate · marcate e confluenti
- Distribuzione: periferica · centrale · diffusa
- Aspetto: sparse e fini · a depositi solidi · massive e confluenti
- Linguaggio referto: sempre "reperto aspecifico"; le scarse sono esplicitamente fisiologiche

### 9 · Altre Lesioni
**CHIV — Istiocitosi intervillosa cronica:**
- Entità infiltrato istiocitario, distribuzione spaziale
- IHC CD68/CD163 (eseguita o no)
- Associazione con fibrina perivillosa
- Componente infettiva esclusa (base morfologica / IHC-PCR / non valutata)
- Diagnosi nel referto sempre condizionale ("compatibile con CHIV; conferma IHC se non eseguita")

**MPFD — Fibrina perivillosa massiva / maternal floor infarction:**
- Distribuzione fibrina: basale (maternal floor) · transmurale · multifocale
- % parenchima con intrappolamento villare
- Intrappolamento villare (presente / assente)
- Conferma su campionamento multiplo (sì / da confermare)
- Diagnosi nel referto: "compatibile con/da valutare per MPFD se confermato su sezioni rappresentative"; se basale aggiunge "in distribuzione suggestiva per maternal floor infarction"
- **Mai "MPFD" secco** senza clausola di conferma

---

## Output generato

### Diagnosi istologica sintetica (Amsterdam/Redline)
Box separato in apertura del referto, in linguaggio nomenclaturale strutturato. Elenca solo le lesioni effettivamente selezionate. Voci MVM riflettono esattamente le checkbox attive (non tutte le possibili lesioni MVM).

### Descrizione morfologica
Prosa italiana refertativa, organizzata in blocchi:
1. Macroscopico
2. Campionamento
3. Pilastri fondamentali
4. Lesioni (un blocco per categoria, nell'ordine di rilevanza)

### Commento clinico-patologico
Formula sempre **prudente e condizionale**. Principi applicati:
- Il patologo descrive il reperto, non imposta la terapia
- "Correlare con…" / "di pertinenza clinica" / "se clinicamente indicato"
- Workup per trombofilia: suggerito solo per MVM significativa, calibrato sul contesto (infarti focali a termine ≠ infarti estesi precoci)
- Corioamnionite: "comunicare al clinico" — solo FIR Grado 3 riceve formulazione urgente, sempre senza indicazioni terapeutiche
- VUE: "quadro compatibile con VUE, in assenza di criteri morfologici o clinici per eziologia infettiva" — diagnosi di esclusione ragionata, non etichetta automatica
- CHIV/MPFD: "non esistono strategie preventive universalmente validate; eventuali approcci nelle gravidanze successive sono di pertinenza ostetrico-materno-fetale"

---

## Logica di sicurezza

| Situazione | Comportamento |
|---|---|
| MVM checkata, nessuna sottovoce selezionata | Avviso "verificare la selezione" |
| MVM checkata, solo lesioni vascolari (no infarti) | Commento su arteriopatia/MVM senza nominare infarti |
| MVM checkata, infarti selezionati | Commento calibrato su estensione e contesto clinico |
| Fibrina estesa >25% nei pilastri | Formula "da valutare per MPFD se confermato" (mai diagnosi automatica) |
| Nodi sinciziali aumentati | "può rientrare nel pattern MVM se sostenuto da ulteriori dati" (mai assertivo) |
| Villite con sospetto infettivo | Commento urgente, gestione demandata al clinico |
| Calcificazioni scarse a termine | Esplicitamente fisiologiche, nessun workup suggerito |

---

## Pulsanti

| Pulsante | Funzione |
|---|---|
| 🆕 Nuovo caso | Azzera tutti i campi, chiude i pannelli lesione, nasconde il referto, torna in cima (richiede conferma) |
| 📄 Genera Referto | Compila diagnosi sintetica, descrizione morfologica e commento |
| 📋 Copia referto (testo) | Copia negli appunti in formato testo plain (diagnosi + descrizione + commento) |

---

## Riferimenti bibliografici

- Khong TY et al. Sampling and Definitions of Placental Lesions: Amsterdam Placental Workshop Group Consensus Statement. *Arch Pathol Lab Med.* 2016;140(7):698–713.
- Redline RW. Classification of placental lesions. *Am J Obstet Gynecol.* 2015;213(4 Suppl):S21–8.
- Benirschke K, Kaufmann P, Baergen RN. *Pathology of the Human Placenta.* 6th ed. Springer; 2012.
- Pinar H et al. Placental weight percentile curves for singleton and multiple pregnancies. *Pediatr Dev Pathol.* 2011;14(6):450–8. *(curva di riferimento consigliata per validazione percentile; la tabella interna del tool è orientativa)*

---

## Disclaimer

- Strumento sviluppato per uso interno nella SC di Anatomia Patologica dell'ASST Fatebenefratelli-Sacco, Milano
- Non sostituisce il giudizio clinico del patologo
- Il referto generato è una **bozza strutturata** da revisionare prima della firma
- I workup suggeriti sono orientativi e vanno adattati al contesto clinico locale
- "Tu non stai automatizzando la diagnosi. Stai automatizzando la prudenza."

---

*v4.0 — maggio 2026*
