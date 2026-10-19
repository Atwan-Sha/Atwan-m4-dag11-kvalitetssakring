# Dag 11 · Sammanställning och kvalitetssäkring

*Modul 4, UI/UX & Frontendutveckling, Lexicon IT-Proffs*

## Vad du ska göra idag

Du granskar en sida som innehåller **tio avsiktliga fel** (HTML, tillgänglighet, CSS och responsivitet). Du hittar dem, rättar dem och dokumenterar varje fix i en commit. Sedan gör du samma granskning på ditt eget projekt.

## Bakgrund

Att skriva kod är hälften av jobbet. Den andra hälften är att kontrollera den. Ett bra kvalitetsarbete går efter en **checklista** och rättar ett fel i taget. Checklistan finns i `KVALITETSLISTA.md`. Gör en commit per fel, med ett meddelande som beskriver vad du rättade.

## Så arbetar du (samma som alltid)

1. **Forka** dagens repo på GitHub (*Fork → Create fork*).
2. **Klona din fork:** *Code → HTTPS → kopiera adressen*. I terminalen (Ctrl+ö i VS Code): `git clone <adressen>`. Öppna den nya mappen i VS Code och starta *Live Server*.
3. **Gör uppgiften.** Spara och kontrollera i webbläsaren efter varje steg. Gör en commit efter varje avslutat steg: `git add .` och `git commit -m "Beskriv vad du gjorde"`.
4. **Skicka upp** när du är klar: `git push`.
5. **Lämna in i Microsoft Forms.**

Fastnar du: skriv ner exakt var och vad du försökt, och ta det först i nästa handledda pass.

## Uppgiften steg för steg

### Steg 1. Gå igenom checklistan

Öppna `KVALITETSLISTA.md` och läs hela. Den är din karta.

### Steg 2. Kör validatorn och Lighthouse

Kör `index.html` och `kontakt.html` genom validator.w3.org och skriv upp felen. Kör sedan Lighthouse (DevTools, fliken Lighthouse, kryssa Accessibility, *Analyze*) på `index.html` och **skriv upp poängen** (före).

### Steg 3. Hitta de tio felen

Det finns bland annat: en saknad alt-text, ett hopp i rubrikhierarkin, en `label` som inte är kopplad, en `<div>` som fungerar som knapp, en text med för låg kontrast, ett element med fast bredd som ger horisontell scroll på mobil, en trasig länk, ett dubblerat `id`, en saknad `lang`, och en oanvänd, felstavad CSS-klass. Hitta dem alla.

### Steg 4. Rätta ett i taget

För varje fel: rätta, spara, testa, `git add`, `git commit -m "Rätta: ..."`. Tio fel ska ge minst tio commits.

### Steg 5. Testa med tangentbord

Tabba genom hela sidan. Allt ska kunna nås och du ska alltid se var du är.

### Steg 6. Testa i tre bredder

Kontrollera 360, 768 och 1280 px i DevTools.

### Steg 7. Applicera på ditt projekt

Gör samma granskning på `mitt-projekt` och skriv resultatet i `docs/kvalitetslogg.md`.

### Steg 8. Kör Lighthouse igen

Kör Lighthouse Accessibility på `index.html` igen och skriv upp poängen (efter). Den ska ha gått upp.

### Steg 9. Skicka upp

`git push` och kontrollera att GitHub Pages visar rätt version.

## AI-spåret (nivå 3: Styr och ansvara)

**Människa mot AI: vem hittar flest fel?** (cirka 30 minuter, efter att du gjort din egen lösning)

Fri användning, full loggning. Du bär ansvaret för allt du lämnar in. Det är så du lär dig vad AI är bra och dålig på, med siffror från dina egna fall.

Regler: egen lösning först, du ska kunna förklara varje rad, och du loggar i `docs/ai-logg.md` i `mitt-projekt`. Reglerna finns i `AI-REGLER.md` i `mitt-projekt`.

1. Hitta felen i övningssidan själv, med checklistan. Skriv listan innan du frågar AI.
2. Be AI granska samma sida med prompten nedan.
3. Fyll i en tabell: du hittade, AI hittade, båda, ingen, AI:s falsklarm.
4. Kör Lighthouse som tredje granskare.
5. Dra en slutsats i ai-loggen: vad ska du alltid kontrollera själv?

Prompt att utgå från:

```
Granska denna webbsida (HTML och CSS) för
validitet, tillgänglighet, responsivitet
och kodkvalitet. Lista varje fel med fil
och rad. Skriv inte om koden.

[klistra in sidans kod här]
```

**Kontrollera med:**

- Validatorn, Lighthouse och tangentbordstestet.
- Varje fel som AI listar: finns det på riktigt?

**I ditt projekt:** Låt AI granska ditt eget projekt och jämför med din kvalitetslogg.

## Kontrollista: så vet du att du är klar

- [ ] Du har hittat och rättat alla tio avsiktliga fel, med en commit per fel.
- [ ] Du har skrivit upp Lighthouse-poängen före och efter.
- [ ] Båda sidorna validerar utan fel.
- [ ] Tangentbordsnavigeringen fungerar överallt.
- [ ] Ingen horisontell scroll på 360 px.
- [ ] Din granskning av `mitt-projekt` finns i `docs/kvalitetslogg.md`.
- [ ] Allt är pushat och live-sidan visar rätt version.
- [ ] Du har gjort AI-uppgiften och skrivit en post i `docs/ai-logg.md`.

## Tips om du fastnar

- Hitta fel systematiskt, uppifrån och ned i checklistan, istället för att leta på måfå.
- Om du hittar färre än tio: kolla CSS-filerna och formuläret en gång till.
- Fastnar du på kontrast: använd samma kontrastverktyg som i modul 3.

## Ditt projekt: Dagens steg i `mitt-projekt`

Efter övningen här jobbar du vidare i ditt eget projekt (din design från modul 3). Dagens steg står i `PROJEKTSTEG.md` i ditt repo `mitt-projekt`, under **Dag 11**. Det är där ditt riktiga arbete växer. Övningen här är träningsbanan.

## Inlämning

**Deadline: imorgon klockan 09.00.** Allt lämnas in i Microsoft Forms. Du behöver inte redovisa något muntligt.

I formuläret fyller du i:

1. Länk till din fork av det här repot.
2. Länk till ditt `mitt-projekt`.
3. Reflektion: Skriv Lighthouse Accessibility-poängen före och efter på övningssidan (till exempel 82 → 100). Vilket fel var svårast att hitta, och vilken metod hittade det till slut?

## Vill du mer? (frivilligt)

- Lägg till en egen checklista för portföljen.
- Kör Lighthouse Performance och skriv ner de tre viktigaste förbättringsförslagen.
