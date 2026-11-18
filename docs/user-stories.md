# User Stories – Delfinen

## US1 – Opret medlem (F1)

**Prioritet: 1 – Estimat: M**

Som formand kan jeg oprette et nyt medlem med navn, fødselsdato og aktivitetsform, så klubben kan registrere sine medlemmer.

**Acceptkriterier:**
- Når formanden indtaster navn og fødselsdato, kan der vælges mellem aktivt og passivt medlemskab.
- Ved aktivt medlemskab kan der vælges mellem motionist og konkurrencesvømmer.
- Ved passivt medlemskab registreres medlemmet som passivt.
- Systemet afviser en ugyldig fødselsdato.

**Accepttest:**
- Et nyt medlem oprettes med navn og fødselsdato.
- Der vælges aktivt medlemskab og motionist eller konkurrencesvømmer.
- Et medlem med passivt medlemskab oprettes som passivt.
- En ugyldig fødselsdato indtastes, og systemet afviser oprettelsen.

## US2 – Vælg svømmediscipliner (F2)

**Prioritet: 2 – Estimat: S**

Som formand kan jeg vælge én eller flere svømmediscipliner til en konkurrencesvømmer, så klubben ved, hvilke discipliner svømmeren er aktiv i.

**Acceptkriterier:**
- Der kan vælges én eller flere discipliner til en konkurrencesvømmer.
- De valgte discipliner gemmes på medlemmet.
- Der skal vælges mindst én disciplin for at oprette en konkurrencesvømmer.
- Motionister skal ikke have tilknyttet discipliner.

**Accepttest:**
- En konkurrencesvømmer oprettes med butterfly og crawl.
- Begge discipliner gemmes på medlemmet.
- En konkurrencesvømmer forsøges oprettet uden en disciplin, og systemet afviser oprettelsen.
- En motionist oprettes uden discipliner.

## US3 – Tildel medlemsnummer (F3)

**Prioritet: 3 – Estimat: S**

Som formand vil jeg have, at systemet automatisk tildeler hvert nyt medlem et unikt medlemsnummer, så medlemmerne kan identificeres.

**Acceptkriterier:**
- Systemet tildeler automatisk et medlemsnummer, når et nyt medlem oprettes.
- Alle medlemmer skal have et unikt medlemsnummer.
- Et medlemsnummer må ikke genbruges, hvis et medlem meldes ud.

**Accepttest:**
- Et nyt medlem oprettes, og systemet tildeler et medlemsnummer.
- Flere medlemmer oprettes, og alle får forskellige medlemsnumre.
- Et medlem meldes ud, og medlemsnummeret bruges ikke igen. Test passed.

## US4 – Se medlemsoversigt (F4)

**Prioritet: 4 – Estimat: M**

Som formand kan jeg se en oversigt over alle medlemmer, så jeg har overblik over klubbens medlemmer.

**Acceptkriterier:**
- Medlemsoversigten viser medlemsnummer, navn, alder, junior/senior og aktivitetsform.
- Medlemmer under 18 år vises som juniorer.
- Medlemmer på 18 år eller derover vises som seniorer.
- Medlemskategorien ændres automatisk, når et medlem fylder 18 år.

**Accepttest:**
- Flere medlemmer oprettes med forskellige aldre og aktivitetsformer.
- Medlemsoversigten åbnes, og alle oplysninger vises.
- Et medlem under 18 år vises som junior.
- Et medlem på 18 år eller derover vises som senior. Test passed.

---

## Kassereren

## US5 – Se kontingent for medlem (F5)

**Prioritet: 5 – Estimat: M**

Som kasserer kan jeg se hvert medlems årlige kontingent, så jeg ved, hvor meget hvert medlem skal betale.

**Acceptkriterier:**
- Systemet beregner automatisk kontingentet ud fra medlemskabstype og alder.
- Aktiv junior: 1.000 kr.
- Aktiv senior: 1.600 kr.
- Aktiv senior på 60 år eller derover: 25 % rabat fra 1.600 kr.
- Passivt medlem: 500 kr. uanset alder.

**Accepttest:**
- Forskellige medlemmer oprettes:
    - Passivt medlem.
    - Aktiv junior.
    - Aktiv senior.
    - Aktiv senior på 60 år eller derover.
- Systemet beregner kontingentet for hvert medlem.
- Alle kontingentbeløb vises korrekt. Test passed.

## US6 – Se forventet kontingentindtægt (F6)

**Prioritet: 6 – Estimat: S**

Som kasserer kan jeg se den forventede samlede kontingentindtægt, så jeg kan få overblik over klubbens forventede indtægter.

**Acceptkriterier:**
- Systemet beregner den samlede forventede kontingentindtægt for alle medlemmer.
- Medlemmer, der ikke har betalt, medregnes stadig i den forventede indtægt.
- Hvis klubben ikke har nogen medlemmer, vises den forventede indtægt som 0 kr.

**Accepttest:**
- Flere medlemmer oprettes med forskellige medlemskabstyper.
- Nogle medlemmer registreres som betalt, og andre som ikke betalt.
- Systemet beregner den samlede forventede kontingentindtægt.
- Det samlede beløb vises korrekt. Test passed.

## US7 – Registrer kontingentbetaling (F7)

**Prioritet: 7 – Estimat: S**

Som kasserer kan jeg registrere, at et medlem har betalt årets kontingent, så klubben kan holde styr på betalingerne.

**Acceptkriterier:**
- Kassereren kan registrere en betaling for et medlem.
- Medlemmets betalingsstatus ændres til betalt.
- Systemet viser en fejlmeddelelse, hvis medlemsnummeret ikke findes.
- Et medlem, der allerede har betalt, skal fortsat stå som betalt.

**Accepttest:**
- Et medlem oprettes uden registreret betaling.
- Betalingen registreres, og betalingsstatus ændres til betalt.
- Et ugyldigt medlemsnummer indtastes, og systemet viser en fejlmeddelelse.
- Et medlem, der allerede har betalt, beholder sin betalingsstatus. Test passed.

## US8 – Se medlemmer i restance (F8)

**Prioritet: 8 – Estimat: M**

Som kasserer kan jeg se en liste over medlemmer i restance, så jeg kan få overblik over manglende betalinger.

**Acceptkriterier:**
- Restancelisten viser medlemmer, der ikke har betalt årets kontingent.
- Listen viser medlemsnummer, navn og det skyldige beløb.
- Medlemmer, der har betalt, vises ikke på restancelisten.
- Nye medlemmer, der endnu ikke har betalt, vises på listen.
- Hvis alle medlemmer har betalt, vises en tom liste.

**Accepttest:**
- Flere medlemmer oprettes med forskellige betalingsstatusser.
- Restancelisten åbnes.
- Medlemmer uden betaling vises med de korrekte oplysninger og beløb.
- Medlemmer, der har betalt, vises ikke på listen. Test passed.

---

## Træneren

## US9 – Se junior- og seniorhold (F9)

**Prioritet: 9 – Estimat: M**

Som træner kan jeg se juniorholdet og seniorholdet hver for sig, så jeg kan få overblik over konkurrencesvømmerne og deres discipliner.

**Acceptkriterier:**
- Juniorholdet viser konkurrencesvømmere under 18 år.
- Seniorholdet viser konkurrencesvømmere på 18 år eller derover.
- Svømmernes aktive discipliner vises på holdoversigten.
- Motionister og passive medlemmer vises ikke på holdoversigten.

**Accepttest:**
- Der oprettes konkurrencesvømmere under og over 18 år.
- Der oprettes også motionister og passive medlemmer.
- Juniorholdet og seniorholdet åbnes hver for sig.
- Svømmerne vises på det korrekte hold med deres discipliner. Test passed.

## US10 – Registrer træningsresultat (F10)

**Prioritet: 10 – Estimat: L**

Som træner kan jeg registrere en konkurrencesvømmers træningstid med dato og disciplin, så jeg kan følge svømmerens udvikling.

**Acceptkriterier:**
- Træneren kan registrere træningstid, dato og disciplin for en konkurrencesvømmer.
- Resultatet gemmes på svømmeren.
- Hvis den nye tid er hurtigere end den tidligere bedste tid, bliver den registreret som den nye bedste tid.
- Hvis den nye tid er langsommere, beholdes den tidligere bedste tid, og systemet giver besked.
- Der kan ikke registreres tider i discipliner, som svømmeren ikke er aktiv i.

**Accepttest:**
- En konkurrencesvømmer oprettes med butterfly som aktiv disciplin.
- En træningstid med dato registreres i butterfly.
- En hurtigere tid registreres, og bliver den nye bedste tid.
- En langsommere tid registreres, og den tidligere bedste tid beholdes.
- Der forsøges registreret en tid i en disciplin, som svømmeren ikke er aktiv i, og systemet afviser registreringen. Test passed.

## US11 – Registrer stævneresultat (F11)

**Prioritet: 11 – Estimat: M**

Som træner kan jeg registrere en konkurrencesvømmers stævneresultat, så klubbens deltagelse i konkurrencer bliver dokumenteret.

**Acceptkriterier:**
- Træneren kan registrere stævnets navn, dato, disciplin, placering og tid.
- Resultatet gemmes på konkurrencesvømmeren.
- Der kan ikke registreres resultater i discipliner, som svømmeren ikke er aktiv i.
- Systemet afviser en ugyldig stævnedato.

**Accepttest:**
- En konkurrencesvømmer findes i medlemslisten.
- Et stævneresultat registreres med navn, dato, disciplin, placering og tid.
- Resultatet gemmes på svømmeren.
- En ugyldig dato indtastes, og systemet afviser registreringen. Test passed.

## US12 – Se en svømmers resultater (F12)

**Prioritet: 12 – Estimat: M**

Som træner kan jeg se en konkurrencesvømmers resultater, så jeg kan følge svømmerens præstationer.

**Acceptkriterier:**
- Systemet viser svømmerens bedste træningstid og dato for hver disciplin.
- Alle registrerede stævneresultater vises med stævnenavn, dato, disciplin, placering og tid.
- Systemet viser en fejlmeddelelse, hvis medlemsnummeret ikke findes.

**Accepttest:**
- En konkurrencesvømmer oprettes med registrerede træningsresultater.
- Svømmerens resultater åbnes.
- Den bedste træningstid og dato vises for hver disciplin.
- Registrerede stævneresultater vises med alle oplysninger.
- Et medlemsnummer, der ikke findes, indtastes, og systemet viser en fejlmeddelelse. Test passed.

## US13 – Se top 5-svømmere (F13)

**Prioritet: 13 – Estimat: L**

Som træner kan jeg se de fem bedste konkurrencesvømmere inden for hver disciplin fordelt på juniorer og seniorer, så jeg kan vurdere svømmernes præstationer.

**Acceptkriterier:**
- Træneren kan vælge en svømmedisciplin.
- Systemet viser juniorernes og seniorernes top 5 hver for sig.
- Svømmerne sorteres efter hurtigste træningstid først.
- Svømmere, der ikke er aktive i disciplinen, medtages ikke.
- Svømmere uden en registreret træningstid medtages ikke.
- Hvis der er færre end fem kvalificerede svømmere, vises de svømmere, der er tilgængelige.
- Hver svømmer vises kun én gang med sin bedste tid.
- Listen viser svømmerens navn, tid og dato.

**Accepttest:**
- Flere konkurrencesvømmere oprettes med forskellige discipliner og træningstider.
- Træneren vælger butterfly.
- Systemet viser juniorernes og seniorernes top 5 hver for sig.
- Svømmerne sorteres efter hurtigste tid.
- Svømmere uden butterfly som aktiv disciplin eller uden registreret tid medtages ikke.
- Svømmere med flere resultater vises kun én gang med deres bedste tid. Test passed.

---

## Fælles funktionalitet

## US14 – Gem og indlæs data (F14)

**Prioritet: 14 – Estimat: L**

Som bruger vil jeg have, at alle medlemmer, betalinger og resultater gemmes i tekstfiler og indlæses ved opstart, så mine data ikke går tabt, når programmet lukkes.

**Acceptkriterier:**
- Systemet gemmer alle medlemmer, betalinger og resultater i tekstfiler, når programmet lukkes.
- Systemet indlæser tidligere gemte data, når programmet startes igen.
- Alle registrerede data skal være bevaret efter genstart.
- Hvis datafilerne mangler, starter programmet med en tom klub.

**Accepttest:**
- Der oprettes medlemmer, registreres betalinger og tilføjes resultater.
- Programmet lukkes, og data gemmes i tekstfiler.
- Programmet startes igen, og de tidligere data indlæses.
- Det kontrolleres, at alle oplysninger stadig findes.
- Programmet startes uden datafiler, og en tom klub indlæses. Test passed.

---

## Prioritering og estimater

Prioriteringen og estimaterne er et første forslag og skal godkendes af gruppen i fællesskab.

**Størrelser:**
- S = Under en halv dag for én person
- M = Omkring én dag
- L = To dage eller mere

## Status

Alle user stories er endnu ikke implementeret. Status opdateres løbende under projektet.