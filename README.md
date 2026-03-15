# 📱 Terrein App - Buitenzorg (Mobiel)

De **Terrein App** is een mobiel-vriendelijke, razendsnelle web-app ontworpen voor de kampstaf van Scoutcentrum Buitenzorg. Het fungeert als een slimme, dynamische actielijst in je broekzak. De app koppelt live met het Labelbooking iCal-systeem en vertelt de staf in één oogopslag welke groepen extra aandacht nodig hebben.

## ✨ Unieke Features & Slimme Logica

### 🎨 De "To-Do" Kleurenlogica
De app berekent op de minuut nauwkeurig de status van een groep en geeft deze een kleurcode.
* 🔴 **Rood (Hoogste prioriteit):** Actie vereist! Een groep is te laat met inchecken of te laat met uitchecken ten opzichte van de huidige tijd.
* 🟧 **Oranje (To-Do vandaag):** Verwachte actie voor vandaag. De groep komt later vandaag aan, óf ze zijn momenteel ingecheckt maar vertrekken vandaag.
* 🟩 **Groen (In orde):** De groep is veilig ingecheckt en blijft nog even.
* ⬜ **Grijs (Gepland):** Groepen die in de toekomst aankomen (met aankomsttijd).
* ⚪ **Wit (Klaar):** Groepen die al zijn uitgecheckt of geannuleerd. Deze verdwijnen netjes naar de bodem.

### 🧠 Keiharde Sorteermotor
Geen rommelige lijsten meer. De app sorteert alle groepen automatisch via 3 strenge regels:
1. **Prioriteit:** Rood staat altijd bovenaan, daarna Oranje, dan Groen, Grijs en Wit.
2. **Chronologisch (Tijd):** Binnen een kleur (bijv. Oranje) staan de groepen gesorteerd op actietijd. Degene die als eerste weggaat of aankomt, staat bovenaan.
3. **Alfabetisch:** Pas als tijden exact gelijk zijn, wordt er op terreinnaam gesorteerd.

### 🛠️ Gebruiksvriendelijkheid
* **Accordeon Interface:** Om de lijst overzichtelijk te houden bij topdrukte, zijn alle groepen standaard ingeklapt. Klik op een kaart om de details (aantal personen, exacte tijden) uit te vouwen.
* **Tijd-Badges:** De status-badges tonen direct de actietijd, bijvoorbeeld: `VERTREKT VANDAAG (11:00)` of `KOMT VANDAAG (14:00)`.
* **Veilige Bel-knop:** Bevat een groep een geldig telefoonnummer in de reservering? Dan verschijnt er een grote groene bel-knop. (Slimme code voorkomt dat de accordeon onbedoeld dichtklapt als je op bellen drukt).
* **Schone Weergave:** Boekingsnummers zoals `(2024-1234)` worden automatisch uit de groepsnaam gefilterd voor een rustig beeld.

## ⚙️ Techniek
* **Proxy Racer:** Haalt data via 3 proxy-servers tegelijk op om CORS-blokkades te omzeilen. De snelste server wint. (Laadt opeenvolgend voor de stafplanning om spam-blokkades te voorkomen).
* Geen database nodig: draait 100% lokaal in de browser van je telefoon.
