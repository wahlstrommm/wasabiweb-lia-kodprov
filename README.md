# Kodprov — LIA

Hej, och kul att du är intresserad av en LIA-plats hos oss!

Det här är ett litet kodprov. Det ska inte ta dig mer än ungefär **2–4 timmar**. Vi är
inte ute efter en massa funktioner eller en perfekt design — vi vill se **tydlig,
strukturerad och ren kod**, och vi vill lära känna dig lite som utvecklare.

Ta det lugnt, ha kul, och fråga hellre en gång för mycket än en gång för lite.

---

## Del 1 — Uppgiften: ett frukt-arkiv

Du ska bygga en liten webbplats med **två vyer**:

1. En **arkivsida** som visar en lista med frukter.
2. En **detaljsida** som visar mer information om *en* frukt när man klickar på den.

### Vad som ska fungera

- [ ] **Skapa din egen datafil** `data/fruits.json` med minst **sex frukter**. Varje
      frukt ska ha åtminstone ett `id`, ett namn, en kort beskrivande text (det gör
      inget om texten är lorem ipsum), ett fält för en bild och ett **numeriskt fält**
      (t.ex. kalorier per 100 g).
- [ ] **Räkna ut något från datan** på arkivsidan och visa det — inte hårdkodat, utan
      uträknat från frukterna när sidan laddas. Välj det du tycker är rimligt, till
      exempel: hur många frukter som visas totalt, genomsnittligt kaloriinnehåll, eller
      vilken frukt som har högst/lägst värde.
- [ ] **Arkivsidan** (`index.html`) ska **hämta** frukterna från JSON-filen med `fetch`,
      loopa igenom dem och rita ut ett kort per frukt med en bild-placeholder, fruktens
      namn och en länk eller knapp vidare till detaljsidan.
- [ ] **Detaljsidan** (`fruit.html`) ska öppnas med fruktens id i URL:en, till exempel
      `fruit.html?id=3`. Sidan ska läsa av `id` ur URL:en, hitta rätt frukt i datan och
      visa dess information.

### Du väljer själv

- **Teknik:** använd det du är mest bekväm med — HTML, CSS och JavaScript, eller PHP.
  Du får använda ett ramverk om du vill, men det är inget krav (och inget vi värderar
  högre).
- **Struktur:** dela upp koden så tydligt du kan. Nedan finns ett förslag på hur du
  *skulle kunna* lägga upp projektet — men det är bara inspiration. Vi är nyfikna på hur
  **du** väljer att strukturera.

```
index.html          -> arkivsidan (alla frukter)
fruit.html          -> en enskild frukt
css/style.css
js/main.js          -> hämtar och listar frukterna på arkivsidan
js/fruit.js         -> logiken för den enskilda fruktsidan
data/fruits.json    -> datan om varje frukt
images/             -> fruktbilder (eller placeholders)
```

### Om du hinner och vill (frivilligt)

Det här är inte ett krav — men vill du visa mer, plocka gärna något av:

- En **sökruta eller ett filter** på arkivsidan.
- Hämta frukterna från ett **publikt API** (t.ex. [Fruityvice](https://www.fruityvice.com/))
  i stället för en lokal JSON-fil.
- **Responsiv** layout som funkar på mobil.
- **Felhantering** — vad händer om hämtningen misslyckas, eller om någon skriver in ett
  `id` som inte finns?

---

## Del 2 — Några frågor om dig

Svara kort i en fil som du kallar `SVAR.md`, eller i ett mail. Det finns inga rätt eller
fel här — vi är bara nyfikna på hur du tänker.

### Hur du jobbar

*(kryssa i det som stämmer bäst, och skriv gärna en rad om varför)*

**1. När du kör fast på ett problem — vad gör du *först*?**
- [ ] Läser dokumentationen
- [ ] Googlar eller frågar en AI
- [ ] Läser koden och felsöker själv
- [ ] Frågar en kollega

**2. Vad gör du för att hitta information?**
- [ ] Googlar
- [ ] Läser officiell dokumentation
- [ ] Frågar en kollega eller kompis
- [ ] Frågar en AI-assistent

### Reflektion

*(några meningar räcker)*

3. En PR (pull request) finns för att granska kod och hindra buggar från att nå
   produktion. **Ser du någon *ytterligare* fördel med att jobba med PR?**

4. Vad skulle du säga är en **styrka** du har som utvecklare?

5. Vad vill du bli **bättre** på?

6. Vad skulle du vilja **uppleva och göra** under din LIA hos oss?

### Om din lösning

*(fyll i efter att du är klar med uppgiften)*

7. Vad var **svårast** med uppgiften?

8. Om du hade **en vecka till** på den här uppgiften — vad hade du förbättrat först?

---

## Inlämning

1. **Skapa ett eget nytt git-repo** (GitHub, GitLab eller liknande) och lägg din kod där.
2. Lägg dina svar från Del 2 i en fil som heter **`SVAR.md`** i samma repo.
3. **Skicka oss länken** till repot.

Har du inget git-konto går det bra att skicka en **zip** med projektmappen och svaren i
stället — men vi ser gärna ett repo om du kan.

Ett par tips, inget krav:

- Vi blir glada om vi får se din **commit-historik** — små, begripliga commits säger en hel
  del om hur du jobbar, mer än en enda "klar"-commit på slutet.
- Gör du repot **privat**, bjud in oss så vi kommer åt det (vi säger vilket användarnamn
  när du hör av dig).

Lycka till! 🍎🍌🍇
