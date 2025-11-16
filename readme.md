# 🫀 Esame Istologico della Placenta

**Tool diagnostico per refertazione sistematica dell'istologia placentare secondo linee guida internazionali.**

---

## 📋 Struttura

### **Sezione 1: Macroscopico**
- **EGA** (settimane + giorni)
- **Peso placenta** (con calcolo % rispetto a peso atteso)
- **Spessore** (con alert range: atrofia < 10mm, edema > 30mm)
- **Lunghezza cordone** (con alert: corto < 30cm, lungo > 80cm)
- **Aspetto superficie fetale** (normale, opaco, furfureo, nodulare)
- **Colore** (rosso normale, pallido, scuro, giallastro)
- **Cordone ombelicale** (normale 3 vasi, villoso, edematoso, trombosato)

### **Sezione 2: Pilastri Fondamentali**
- **EGA all'istologia** (compatibile, precoce, tardiva)
- **Maturazione villare** (maturi, intermedi, immaturi, degenerativi)

### **Sezione 3: Lesioni Patologiche** (toggle per attivare/disattivare)

#### **🔴 Infarti Placentari**
- Estensione (focale, multifocale, estesa)
- Localizzazione (periferica, centrale, diffusa)
- % parenchima coinvolto (stima)
- Note descrittive

#### **🟡 Villite**
- Grado (lieve, moderata, severa)
- Distribuzione (focale, multifocale, diffusa)
- Tipo infiltrato (non specifico, linfocitario, plasmatico, misto, granulocitario)
- Sospetto eziologico (CMV, toxo, sifilide, ecc.)

#### **🟢 Calcificazioni**
- Distribuzione (periferica, centrale, diffusa)
- Stadio (scarsa=fisiologica, moderata, diffusa=patologica)
- Aspetto microscopico (sparse, depositi solidi, massivi)
- Interpretazione clinica

### **Sezione 4: Note Aggiuntive**
- Corioamnionite, amniotite, emorragia, edema, altre osservazioni

---

## 🎯 Output Diagnostico

Genera automaticamente:
1. **Referto macroscopico strutturato**
2. **Valutazione pilastri fondamentali** (EGA, villi)
3. **Lesioni con grado di severità**
4. **Conclusione clinica** con:
   - Diagnosi integrata
   - Significato clinico
   - Workup consigliato
   - Follow-up ostetrico/pediatrico

---

## 🚨 Alert Automatici

- **Peso**: < 80% atteso = Ipotrofia | > 120% = Ipertrofia
- **Spessore**: < 10mm = Atrofia | > 30mm = Edema
- **Cordone**: < 30cm = Rischio compressione | > 80cm = Rischio annodamento

---

## 📚 Metodologia

### **Riferimenti**
- **Benirschke K, Kaufmann P, Baergen RN.** *Pathology of the Human Placenta*. 6th ed. Springer; 2012. (Gold standard per istologia placentare)
- **ISSHP** - International Society for the Study of Hypertension in Pregnancy. Criteri per insufficienza placentare e preeclampsia
- **SIPat** - Società Italiana di Anatomia Patologica. Linee guida per refertazione istologica placentare

---

## 🔧 Uso Pratico

1. **Compila Macroscopico** (peso, spessore, aspetto)
   - Alert automatici ti avvisa di parametri critici
   
2. **Rivedi Pilastri** (EGA, villi)
   - Coerenza con EGA clinica?
   
3. **Attiva/Disattiva Lesioni** (checkbox)
   - Se presenti, riempi dettagli specifici
   
4. **Clicca "Genera Referto"**
   - Output automatico con conclusione e workup

---

## 💡 Conclusioni Automatiche

### **Scenario 1: Placenta Normale**
> Esame senza alterazioni. Struttura e maturazione compatibile con EGA. Villi maturi, assenza di lesioni. Adeguata funzione placentare.
- **Workup**: Nessuno
- **Follow-up**: Standard ostetrico

### **Scenario 2: Infarti Placentari**
> Insufficienza placentare cronica con infarti multifocali.
- **Workup**: Trombofilgia materna (Fattore V, G20210A, proteina C/S), anticorpi antifosfolipidi
- **Follow-up**: Counseling su ricorrenza in gravidanze future, terapia tromboprofilattica

### **Scenario 3: Villite**
> **URGENTE** - Fortemente sospetta infezione congenita.
- **Workup**: Serologica materna STAT (CMV, toxo, sifilide, listeria), PCR liquor neonatale
- **Follow-up**: Pediatria multidisciplinare urgente (neurologia, audiologia, oftalmologia)

### **Scenario 4: Calcificazioni Patologiche**
> Stress placentare cronico, possibile insufficienza placentare.
- **Workup**: Screening preeclampsia, IUGR, trombofilgia se ricorrente
- **Follow-up**: Correlazione con clinica ostetrica

### **Scenario 5: Alterazioni Multiple**
> **URGENTE** - Danno placentare severo multifattoriale.
- **Workup**: Completo per infezione + trombofilgia + anticorpi antifosfolipidi
- **Follow-up**: Multidisciplinare urgente, alto rischio outcome sfavorevole

---

## 🎨 Design

- **Light theme** (grigio pallido #f8f9fa) - coerente con tool melanoma
- **Responsive** - desktop, tablet, mobile
- **Accessibilità** - colori high-contrast (ok/warn/danger)
- **Intuitivo** - toggle per lesioni, alert automatici per parametri critici

---

## ⚠️ Disclaimers

1. **Non è diagnosi automatica** - Richiede giudizio clinico esperto
2. **Alert sono orientativi** - Vanno correlati con clinica ostetrica
3. **Workup è suggeritivo** - Adattare in base a contesto clinico e linee guida locali
4. **Follow-up pediatrico** - Essenziale per villite e infezione congenita sospetta

---

## 📱 Technical Stack

- HTML/CSS/JavaScript (no dependencies)
- Calcoli automatici (peso vs EGA, percentuali)
- Alert real-time
- Export referto (copia/incolla da browser)

---

**Strumento sviluppato per uso interno nella SC di Anatomia Patologica dell'ASST Fatebenefratelli-Sacco, Milano.**

**Uso didattico e professionale nel contesto della pratica patologica.**
