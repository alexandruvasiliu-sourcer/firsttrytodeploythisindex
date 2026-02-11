# 🏠 Gestiune Apartamente - Aplicație PWA

## Versiune 2.0 - Progressive Web App

Aplicație profesională pentru gestionarea apartamentelor la închiriat cu:
- ✅ **Persistență garantată a datelor** (IndexedDB)
- 🔔 **Notificări automate** pentru termene importante
- 💾 **Backup și restaurare** completă
- 📱 **Instalare pe orice dispozitiv** (Windows, Mac, Linux, iPad, iPhone, Android)
- 📊 **Calcul automat** al tuturor utilitățilo

---

## 📋 Cuprins

1. [Instalare și Configurare](#instalare-și-configurare)
2. [Utilizare pe iPad](#utilizare-pe-ipad)
3. [Utilizare pe Windows](#utilizare-pe-windows)
4. [Funcționalități Principale](#funcționalități-principale)
5. [Backup și Restaurare](#backup-și-restaurare)
6. [Rezolvare Probleme](#rezolvare-probleme)

---

## 🚀 Instalare și Configurare

### Varianta 1: Instalare ca PWA (RECOMANDAT)

#### Pe iPad (Safari):

1. **Deschide aplicația în Safari**
   - Navighează la adresa unde ai încărcat fișierele
   - Sau deschide direct `index.html` din Files

2. **Instalează pe ecranul principal**
   - Apasă pe butonul "Share" (pătratul cu săgeata în sus) din toolbar
   - Scroll în jos și selectează "Add to Home Screen"
   - Introdu un nume (ex: "Apartamente")
   - Apasă "Add"

3. **Lansează aplicația**
   - Găsește iconița nouă pe ecranul principal
   - Apasă pentru a deschide aplicația în mod standalone
   - Va arăta și se va comporta ca o aplicație nativă!

#### Pe Windows (Chrome/Edge):

1. **Deschide aplicația în browser**
   - Dublu-click pe `index.html`
   - Sau drag & drop fișierul în Chrome/Edge

2. **Instalează aplicația**
   - Vei vedea un banner "Instalează aplicația" în aplicație
   - SAU apasă pe iconița + din bara de adrese (la dreapta)
   - Click pe "Install" / "Instalează"

3. **Folosește aplicația instalată**
   - Se va deschide într-o fereastră separată, fără bara browserului
   - Va apărea în Start Menu și poate fi fixată în Taskbar
   - Se va comporta exact ca o aplicație Windows obișnuită!

### Varianta 2: Utilizare directă în browser

Dacă nu vrei să instalezi, poți folosi aplicația direct în browser:
- Pe iPad: deschide în Safari și adaugă la favorite
- Pe Windows: deschide în Chrome/Edge și adaugă la bookmarks

---

## 📱 Utilizare pe iPad

### Notificări pe iPad

**IMPORTANT pentru iOS:**
- Notificările funcționează DOAR dacă ai instalat aplicația pe ecranul principal (vezi pasul 2 de mai sus)
- După instalare, mergi în tab-ul "⚙️ Setări"
- Apasă "Activează notificări" și acceptă permisiunea
- Notificările vor apărea ca notificări sistem iOS normale

**Limitări iOS:**
- Notificările pot fi mai puțin consistente decât pe Android
- Dacă nu primești notificări, verifică Settings > Safari > Advanced > Experimental Features și activează "Push API"

### Touch și Gesturi

Aplicația este optimizată pentru iPad:
- **Tap** pentru a deschide detalii apartament
- **Scroll** orizontal pe tab-uri dacă sunt multe
- **Pull to refresh** nu este necesar - datele se actualizează automat

---

## 💻 Utilizare pe Windows

### Instalare ca aplicație Windows

După instalare din browser (vezi mai sus), aplicația va:
- Apărea în Start Menu
- Putea fi fixată în Taskbar
- Rula într-o fereastră separată
- Avea propriul shortcut

### Notificări pe Windows

- Notificările vor apărea ca notificări Windows native
- Se vor afișa în Action Center
- Poți configura sunetele din Windows Settings

---

## 🎯 Funcționalități Principale

### 1. Gestionare Apartamente

**Adăugare apartament:**
- Click pe "➕ Adaugă apartament nou"
- Completează: nume, chiria lunară, întreținerea
- Salvează

**Vizualizare detalii:**
- Click pe orice apartament din grid
- Vezi toate informațiile: chirie, întreținere, status, chiriaș

**Adăugare chiriaș:**
- Deschide detalii apartament
- Click "➕ Adaugă chiriaș"
- Completează: nume, data intrării, indexuri inițiale contoare
- Salvează

### 2. Citire Contoare

**Când să folosești:**
- În perioadele de citire (21-26 ale lunii)
- Când primești pozele contoarelor de la chiriași

**Cum funcționează:**
- Deschide apartamentul
- Click "📊 Citire contoare"
- Introdu indexurile curente
- Aplicația calculează AUTOMAT:
  - Consumul pentru fiecare utilitate
  - Costul electricității (1.16 RON/kWh)
  - Costul gazelor (formula cu 10.813 × 0.25620 × 1.21)
  - Costul apei (3 componente: potabilă + canalizare + meteorică)
  - Total utilități
  - Total cu chirie

### 3. Notificări Automate

Aplicația te notifică automat pentru:

**Citire contoare:**
- Electricitate: în prima zi (22) a perioadei 22-26
- Gaze și apă: în prima zi (21) a perioadei 21-25

**Încasare chirie:**
- Cu 2 zile înainte de data când chiriașul a intrat în apartament

**Plăți facturi:**
- Cu 1 zi înainte de:
  - Întreținere (15)
  - TV+Internet (10)
  - Electricitate (23)
  - Gaze și apă (28)

### 4. Istoric

- Vezi toate operațiunile din ultimele 12 luni
- Filtrează după apartament
- Export în Excel posibil (vezi secțiunea Backup)

### 5. Rapoarte

- Venit lunar total estimat
- Rata de ocupare (%)
- Detalii pe fiecare apartament
- Zile de ocupare pentru fiecare chiriaș

---

## 💾 Backup și Restaurare

### ⚠️ IMPORTANT - CITEȘTE CU ATENȚIE

Datele tale sunt salvate în **IndexedDB** - o bază de date în browser care **NU se șterge** când ștergi cache-ul normal. Totuși, este ESENȚIAL să faci backup regulat!

### Cum să faci Backup

1. **Mergi în tab-ul "⚙️ Setări"**
2. **Secțiunea "💾 Backup și Restaurare"**
3. **Click "⬇️ Exportă toate datele"**
4. **Salvează fișierul JSON** într-un loc sigur:
   - Pe iPad: salvează în iCloud Files
   - Pe Windows: salvează pe Desktop sau OneDrive
   - **RECOMANDARE:** Fă backup săptămânal!

### Când să faci Backup

- Săptămânal (ideal duminica seara)
- Înainte de orice actualizare majoră a browserului
- Înainte să resetezi dispozitivul
- Înainte să dezinstalezi aplicația

### Cum să restaurezi datele

1. **Mergi în "⚙️ Setări"**
2. **Click "⬆️ Importă date"**
3. **Selectează fișierul JSON de backup**
4. **Confirmă că vrei să înlocuiești datele actuale**
5. **Datele vor fi restaurate instantaneu!**

### Sincronizare între iPad și Windows

**MOMENTAN:** Folosește Export/Import manual:
1. Pe dispozitivul 1: Exportă datele
2. Transferă fișierul JSON (email, WhatsApp, AirDrop, etc.)
3. Pe dispozitivul 2: Importă datele

**ÎN VIITOR:** Vom adăuga sincronizare automată prin Google Drive/Dropbox

---

## 🔧 Rezolvare Probleme

### Problema: "Datele mele au dispărut!"

**Cauze posibile:**
1. Ai șters datele browserului (Clear Browsing Data > Site Data)
2. Browser-ul a fost resetat
3. Aplicația rulează în modul Incognito/Private

**Soluție:**
- Restaurează din backup (vezi secțiunea de mai sus)
- **Prevenie:** Fă backup săptămânal!

### Problema: "Nu primesc notificări"

**Pe iPad:**
1. Verifică că ai instalat aplicația pe Home Screen (nu doar bookmark)
2. Mergi în Setări > Safari > Advanced > Experimental Features
3. Activează "Push API" și "Notifications API"
4. În aplicație: Setări > Activează notificări
5. Acceptă permisiunea când apare

**Pe Windows:**
1. Verifică că ai permis notificările în browser
2. Chrome: Settings > Privacy and Security > Site Settings > Notifications
3. Windows: Settings > System > Notifications > [Chrome/Edge]
4. În aplicație: Setări > Activează notificări

### Problema: "Aplicația e lentă"

**Soluții:**
1. Închide alte tab-uri din browser
2. Restart browser/dispozitiv
3. Șterge cache-ul browserului (ATENȚIE: nu șterge Site Data!)
4. Verifică că ai ultimele actualizări de browser

### Problema: "Nu pot exporta/importa date"

**Verificări:**
1. Browser-ul permite descărcări (nu e blocat)
2. Ai spațiu suficient pe dispozitiv
3. Fișierul JSON de import este valid (deschide-l într-un editor text)

### Problema: "Calculele nu par corecte"

**Verificări:**
1. Indexurile introduse sunt corecte?
2. Consumul este pozitiv? (index nou > index vechi)
3. Verifică formulele în cod:
   - Electricitate: consum × 1.16
   - Gaze: consum × 10.813 × 0.25620 × 1.21
   - Apă: (consum × 9.97 × 1.21) + (consum × 7.33 × 1.21) + (1.380 × 10.12 × 1.21)

---

## 📊 Detalii Tehnice

### Tehnologii folosite:
- **Frontend:** HTML5, CSS3, JavaScript (ES6+)
- **Bază de date:** IndexedDB (persistentă, nu se șterge cu cache)
- **PWA:** Service Worker pentru offline și notificări
- **Manifest:** Pentru instalare ca aplicație

### Compatibilitate:
- ✅ **iPad:** Safari 16.4+ (iOS 16.4+)
- ✅ **iPhone:** Safari 16.4+ (iOS 16.4+)
- ✅ **Windows:** Chrome 90+, Edge 90+
- ✅ **Mac:** Chrome 90+, Safari 16.4+
- ✅ **Android:** Chrome 90+
- ✅ **Linux:** Chrome 90+, Firefox 90+

### Securitate:
- Toate datele sunt stocate LOCAL pe dispozitivul tău
- Nicio informație nu este trimisă pe internet
- Nu există server backend
- Nu există trackere sau analytics
- Codul este open-source și poate fi auditat

---

## 🆘 Suport

Dacă întâmpini probleme care nu sunt acoperite în acest ghid:

1. Verifică că folosești un browser compatibil și actualizat
2. Încearcă să reîncarci pagina (Ctrl+F5 / Cmd+Shift+R)
3. Verifică consola browserului pentru erori (F12 > Console)
4. Fă backup și reinstalează aplicația

---

## 📝 Licență și Drepturi de Autor

Aplicație creată pentru gestionarea eficientă a apartamentelor la închiriat.
Versiune 2.0 PWA - Februarie 2026

**Proprietar:** [Numele tău]

Toate drepturile rezervate. Această aplicație este destinată uzului personal.
Pentru distribuire comercială, contactează proprietarul.

---

## 🎉 Mulțumiri

Aplicație dezvoltată cu pasiune pentru a simplifica gestionarea apartamentelor
și pentru a elimina stresul legat de termene și calcule.

**Folosire plăcută!** 🏠
