# 7. UML Klassendiagram

Het UML-klassendiagram laat zien hoe de verschillende onderdelen van de mobiele app van PhoneVentures met elkaar samenwerken. Je ziet welke gegevens er in het systeem staan en hoe die onderdelen met elkaar verbonden zijn. Het diagram geeft een duidelijk overzicht van:
- **Gebruikersbeheer** – bijvoorbeeld wie de gebruiker is, welke rol hij heeft en hoe hij inlogt.
- **Productregistratie** – welke producten een gebruiker heeft en wanneer ze zijn geregistreerd.
- **Chatgesprekken** – contact tussen gebruikers en medewerkers of een chatbot.
- **Reparatieverzoeken** – aanvragen voor hulp bij een kapot product.
- **Garantie-informatie** – of een product nog garantie heeft en of die verlengd kan worden.
- **Communityberichten** – berichten die gebruikers plaatsen om tips of vragen te delen.

Door dit diagram wordt het makkelijker om te begrijpen hoe de onderdelen van de app samenwerken. Zo moet een gebruiker bijvoorbeeld eerst een product registreren voordat hij een reparatieverzoek kan indienen. Ook zie je dat elke stap in het proces wordt vastgelegd in het systeem.

### Gebruiker
Dit is de persoon die het systeem gebruikt. Bijvoorbeeld een klant of een medewerker. Er staat informatie bij zoals:
- `gebruiker_id`: een uniek nummer voor de gebruiker
- `naam`: de naam van de gebruiker
- `e-mailadres`
- `wachtwoord`
- `taal`: de taal waarin de gebruiker het systeem wil gebruiken
- `rol`: of de gebruiker bijvoorbeeld klant of medewerker (support of admin) is

### Product
Dit zijn de spullen die een gebruiker heeft gekocht. Bij elk product staat:
- `registratie_id`: uniek nummer voor de registratie
- `gebruiker_id`: wie het product heeft gekocht
- `product_id`: welk product het is
- `registratie_datum`: wanneer het product is geregistreerd

### Productregistratie
Hier staat wanneer een product is aangemeld bij het systeem.
- `registratie_id`
- `product_id`
- `registratiedatum`

### Chatgesprek
Als een gebruiker contact opneemt met een medewerker of met een chatbot, komt dat hier te staan.
- `gesprek_id`
- `type`: bijvoorbeeld AI of een echte medewerker
- `starttijd` en `eindtijd`: wanneer het gesprek begon en eindigde

### Garantie
Dit geeft aan of het product garantie heeft.
- `garantie_id`
- `startdatum` en `einddatum`
- `status`: bijvoorbeeld actief of verlopen
- `verlengbaar`: kan de garantie verlengd worden? (ja of nee)

### Reparatieverzoek
Als een product kapot is, kan de gebruiker een reparatie aanvragen.
- `verzoek_id`
- `status`: bijvoorbeeld in behandeling of opgelost
- `media`: de gebruiker kan foto’s of video’s meesturen

### Communitybericht
Gebruikers kunnen berichten plaatsen in de community, bijvoorbeeld een vraag of een tip.
- `bericht_id`
- `inhoud`: de tekst van het bericht
- `datum`
- `categorie`: waar het bericht over gaat

### Hoe alles samenwerkt:
- Een gebruiker registreert een product
- Dat product krijgt een productregistratie
- De gebruiker kan via een chatgesprek hulp vragen
- Er kan ook een reparatieverzoek worden ingediend
- Voor dat verzoek kan er een garantie gelden
- En gebruikers kunnen ook actief zijn in de community
