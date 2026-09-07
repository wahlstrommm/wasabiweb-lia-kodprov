# Kodprov — LIA

Hej, och kul att du är intresserad av en LIA-plats hos oss!

Det här är ett litet kodprov. Det ska inte ta dig mer än ungefär **2–4 timmar** — lägg
inte en hel helg på det. Vi är inte ute efter en massa funktioner eller en perfekt
design. Vi vill se **tydlig, strukturerad och ren kod**, och vi vill lära känna dig lite
som utvecklare.

Ta det lugnt, ha kul, och fråga hellre en gång för mycket än en gång för lite. Hör du av
dig med en fråga är det ett plus, inte ett minus.

---

## Om AI-verktyg

Använd gärna AI — vi gör det själva varje dag, och vi tänker inte låtsas som något
annat. Det vi bryr oss om är att du förstår koden du lämnar in, för du kommer få
förklara den för oss efteråt (se *Efter inlämning* längst ner).

Skriv i `SVAR.md` vad du använde AI till och vad du fick ändra på i det du fick tillbaka.
"Ingenting, det funkade direkt" är ett helt okej svar — men titta efter en gång till
innan du skriver det.

---

## Del 1 — Uppgiften: ett frukt-arkiv

Du ska bygga en liten webbplats med **två vyer**:

1. En **arkivsida** som visar en lista med frukter.
2. En **detaljsida** som visar mer information om *en* frukt när man klickar på den.

Datan får du av oss: `data/fruits.json` ligger redan i projektet. Den är exporterad ur
ett äldre system och är inte perfekt — precis som riktig data sällan är. Läs igenom
filen innan du börjar koda.

### Vad som ska fungera

- [ ] **Arkivsidan** (`index.html`) hämtar frukterna från `data/fruits.json`, loopar
      igenom dem och ritar ut ett kort per frukt med bild, namn och en länk vidare till
      detaljsidan.
- [ ] **Detaljsidan** (`fruit.html`) öppnas med fruktens id i URL:en, till exempel
      `fruit.html?id=3`. Sidan läser av `id` ur URL:en, hittar rätt frukt i datan och
      visar dess information.
- [ ] **Räkna ut något från datan** på arkivsidan och visa det — inte hårdkodat, utan
      uträknat från frukterna när sidan laddas. Välj själv vad som känns rimligt: antal
      frukter, genomsnittligt kaloriinnehåll, högsta eller lägsta värde.
- [ ] **Sortera listan** på ett sätt du kan motivera. Vilket sätt spelar mindre roll än
      att du kan säga varför.

### Om datan

Filen är som den är. Vi har inte städat den åt dig, och vi tänker inte tala om vad som
är fel i den. Bestäm själv hur din kod ska bete sig när något saknas eller ser konstigt
ut, och skriv en rad i `SVAR.md` om vad du valde och varför.

En sak värd att veta: det finns mer än ett rimligt svar på hur din uträknade siffra ska
räknas. Landa i ett, och motivera det.

### Du väljer själv

- **Teknik:** använd det du är mest bekväm med. HTML, CSS och JavaScript i webbläsaren,
  eller PHP på servern — båda går bra. Hämtar du datan i webbläsaren gör du det med
  `fetch`; kör du PHP läser du filen server-side. Du får använda ett ramverk om du vill,
  men det är inget krav och inget vi värderar högre.
- **Struktur:** dela upp koden så tydligt du kan. Nedan finns ett förslag på hur du
  *skulle kunna* lägga upp projektet — men det är bara inspiration. Vi är nyfikna på hur
  **du** väljer att strukturera.

```
index.html          -> arkivsidan (alla frukter)
fruit.html          -> en enskild frukt
css/style.css
js/main.js          -> hämtar och listar frukterna på arkivsidan
js/fruit.js         -> logiken för den enskilda fruktsidan
data/fruits.json    -> datan om varje frukt (den får du av oss)
images/             -> fruktbilder (eller placeholders)
```

### Kör projektet lokalt

Om du kör HTML och JavaScript: **dubbelklicka inte på `index.html`**. Öppnad direkt från
filsystemet (`file://`) blockerar webbläsaren `fetch` mot lokala filer, och du får ett
CORS-fel som ser ut som ett fel i din kod men inte är det. Starta en liten lokal server
i projektmappen i stället, till exempel något av:

```bash
npx serve .
php -S localhost:8000
python3 -m http.server 8000
```

Använder du VS Code går det lika bra med tillägget **Live Server**.

### Om du hinner och vill (frivilligt)

Det här är inte ett krav — men vill du visa mer, plocka gärna något av:

- En **sökruta eller ett filter** på arkivsidan.
- **Responsiv** layout som funkar på mobil.
- **Felhantering** — vad händer om hämtningen misslyckas, eller om någon skriver in ett
  `id` som inte finns?
- Hämta frukterna från ett **publikt API** (t.ex. [Fruityvice](https://www.fruityvice.com/))
  i stället för den lokala filen.

---

## Del 2 — Några frågor om dig

Svara kort i `SVAR.md`. Det finns inga rätt eller fel här — vi är bara nyfikna på hur du
tänker. Filen ligger redan i projektet, ifylld med frågorna.

---

## Inlämning

1. **Skapa ett eget nytt git-repo** (GitHub, GitLab eller liknande) och lägg din kod där.
2. Fyll i **`SVAR.md`** och committa den i samma repo.
3. **Skicka oss länken** till repot.

Har du inget git-konto går det bra att skicka en **zip** med projektmappen och svaren i
stället — men vi ser gärna ett repo om du kan.

**Vi vill se din commit-historik.** Sikta på minst fem commits som visar hur lösningen
växte fram, med meddelanden som säger vad du gjorde. Små, begripliga commits berättar mer
om hur du jobbar än själva koden gör. En enda "klar"-commit på slutet är också ett svar,
men inte det vi hoppas på.

Gör du repot **privat**, bjud in oss så vi kommer åt det — hör av dig så säger vi vilket
användarnamn.

**Deadline:** _[fyll i datum]_. Hinner du inte, säg till i förväg så löser vi det.

---

## Efter inlämning

Vi hör av oss inom _[fyll i, t.ex. en vecka]_ efter deadline, oavsett hur det går.

Går vi vidare bokar vi ett kort samtal på ungefär 20 minuter där vi öppnar din kod
tillsammans och du får berätta hur du tänkte. Vi kommer också be dig ändra något litet i
koden medan vi tittar. Det är inget prov i att kunna allt utantill — vi vill bara se dig
resonera i din egen kod. Har du byggt det du lämnat in har du inget att oroa dig för.

Lycka till! 🍎🍌🍇
