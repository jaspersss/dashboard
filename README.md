# 📱 Terrein App Buitenzorg

Welkom bij de repository van de **Terrein App Buitenzorg**! Dit is een razendsnelle, mobiel-geoptimaliseerde web-applicatie (PWA) speciaal gebouwd voor de kampstaf en beheerders die over het scoutcentrum lopen. Geen grote kalenders of ingewikkelde menu's, maar direct antwoord op de vraag: *"Wie staat er nú op het terrein?"*

## 🌟 Wat doet deze app?
De app leest live de iCal-bestanden (uit Labelbooking) van het kampterrein uit en transformeert deze tot een overzichtelijke, app-achtige interface voor op de smartphone. Met één blik op het scherm zie je:
- Welke stafleden er vandaag dienst hebben.
- Welke groepen er op welke velden (🏕️) of in welke gebouwen (🏠) staan.
- Details zoals groepsgrootte, reserveringsstatus en aankomst-/vertrektijden.
- Een grote groene knop om de groep direct te bellen.

## ✨ Features
* **Mobile-First Design:** Ontworpen om op een telefoonscherm te gebruiken, inclusief een vaste navigatiebalk onderaan om snel tussen dagen te wisselen.
* **Direct Bellen (Smart Phone Extraction):** De app zoekt in de notities van de reservering naar (internationale) telefoonnummers, formatteert deze netjes naar een werkend formaat (bijv. `+316...`), en genereert een klikbare bel-knop.
* **Slimme Relatieve Datums:** Tijdsaanduidingen worden menselijk gemaakt. In plaats van stugge datums zie je *Vandaag*, *Morgen*, *Afgelopen maandag* of *Overmorgen*.
* **Razendsnel (Proxy Racing):** Om de wachttijden van gratis CORS-proxy's te omzeilen, vuurt de app het verzoek op meerdere servers tegelijk af. De server die als eerste antwoordt, wordt gebruikt. 
* **Caching (Offline Fallback):** Data wordt 5 minuten lokaal op de telefoon bewaard. Switch je even naar Whatsapp en weer terug? De app laadt in 0.1 seconde. Valt je 4G weg in het bos? Dan toont hij de laatst bekende data.
* **Velden & Gebouwen Logica:** Herkent automatisch of een locatie een gebouw of een kampeerveld is en voegt hier de juiste icoontjes aan toe.

## 📲 Installatie op je telefoon (Voor de staf)
Omdat de app is gebouwd als een *Progressive Web App* (PWA), kun je hem installeren alsof het een echte app uit de App Store is, zonder dat het opslagruimte kost!

**Op iPhone (Safari):**
1. Open de link van de applicatie.
2. Tik onderin beeld op het **Deel-icoontje** (het vierkantje met het pijltje omhoog).
3. Scroll naar beneden en kies **Zet op beginscherm**.
4. Tik op **Voeg toe**. De app staat nu tussen je andere apps!

**Op Android (Chrome):**
1. Open de link van de applicatie.
2. Tik rechtsboven op de **drie puntjes**.
3. Kies **Toevoegen aan startscherm**.
4. Tik op **Toevoegen**.

## 🛠️ Techniek & Hosting
Dit project is gebouwd als een **Single Page Application (SPA)**.
- **Talen:** HTML5, CSS3, en Vanilla JavaScript (ES6).
- **Geen database:** Alles wordt *on-the-fly* berekend en gerenderd in de browser.
- **Hosting:** Gehost via **GitHub Pages**. Volledig serverless.

## ⚙️ Configuratie (Voor beheerders)
Wil je instellingen wijzigen? Open het HTML-bestand en zoek naar het configuratie-blok bovenaan in het `<script>` gedeelte:

* **iCal Links:** Wijzig de `planningUrl` en `reservationUrl` als de geheime tokens vanuit Labelbooking ooit vernieuwd worden.
* **Proxy Lijst:** De `proxies` array bevat de servers die worden gebruikt om CORS-blokkades te omzeilen. Mochten deze offline gaan, kunnen hier nieuwe publieke proxy's worden toegevoegd.

---
*Gemaakt met ❤️ voor de staf van Scoutcentrum Buitenzorg.*
