## 📓 Gemini Notebook (NotebookLM) – vychytávky, tipy a praktické cvičenia (2. časť)

**Praktický sprievodca pre mierne pokročilých používateľov**  

> [!IMPORTANT]
> Gemini Notebook (predtým NotebookLM) pracuje predovšetkým s vybranými zdrojmi. **Odpoveď s citáciou ešte automaticky neznamená, že je fakticky správna.** Pri dôležitých tvrdeniach kontrolujeme pôvodný dokument, autora, dátum a konkrétnu citovanú pasáž.

> [!NOTE]
> Označenia funkcií, klávesové skratky doplnkov, tarifné limity a dostupnosť noviniek sa môžu meniť. Rozlišujeme **vstavané funkcie Googlu**, **funkcie prehliadača Chrome** a **možnosti rozšírení tretích strán**. Dokument bol zosúladený s verejne dostupnou dokumentáciou Googlu k uvedenému dátumu.

### Obsah

1. [Príprava a efektívne používanie rozhrania](#kapitola-1)
2. [Placeholdery – zástupné symboly](#kapitola-2)
3. [15 praktických promptov s konkrétnymi hodnotami](#kapitola-3)
4. [Fast Research a Deep Research](#kapitola-4)
5. [Poznámky a ich transformácie](#kapitola-5)
6. [Viditeľné vodoznaky, SynthID, C2PA a EXIF](#kapitola-6)
7. [Používanie a limity umelej inteligencie](#kapitola-7)
8. [Audio Overview a interaktívny režim](#kapitola-8)

<a id="kapitola-1"></a>
## 1. Efektívne používanie rozhrania Gemini Notebook

### Základné pracovné oblasti

| Oblasť | Účel | Typická činnosť |
|---|---|---|
| **Sources / Zdroje** | Správa dokumentov, odkazov, súborov a poznámok | Výber relevantných podkladov, štítky, Fast Research |
| **Chat / Čet** | Otázky nad vybranými zdrojmi | Analýza, porovnanie tvrdení, kontrola citácií |
| **Studio / Štúdio** | Generovanie tematických výstupov | Audio Overview, prezentácia, kvíz, správa alebo infografika |

**Odporúčaný postup:** vyberieme zdroje → sformulujeme presnú otázku → skontrolujeme citácie → pripravíme výstup → výsledok ešte raz overíme.

### Vychytávka 01 – Rýchla zmena jazyka používateľského rozhrania

Jazyk rozhrania môžeme skúsiť zmeniť parametrom `hl` v adrese:

- [Angličtina](https://notebook.google.com/?hl=en) – `https://notebook.google.com/?hl=en`
- [Slovenčina](https://notebook.google.com/?hl=sk) – `https://notebook.google.com/?hl=sk`
- [Čeština](https://notebook.google.com/?hl=cs) – `https://notebook.google.com/?hl=cs`

Parameter `hl` predstavuje požadovaný jazyk rozhrania. Jeho účinok však môže závisieť od účtu, prehliadača a dostupných lokalizácií; nemusí prepísať všetky jazykové preferencie.

**Trvalejšie nastavenie cez Google účet:**

1. Otvoríme [Jazyk Google účtu](https://myaccount.google.com/language).
2. V časti preferovaného jazyka upravíme výber.
3. Vyberieme napríklad English (United States), Slovenčina alebo Čeština.
4. Obnovíme otvorenú stránku Gemini Notebook.

**Pozor:** Jazyk tlačidiel rozhrania nie je to isté ako **jazyk generovaných výstupov**. Ten nastavujeme v **Settings → Output Language**. V jednom účte tak môžeme používať anglické rozhranie a slovenské odpovede.

**Cvičenie:** Prepínajme `?hl=en`, `?hl=sk` a `?hl=cs`. Potom necháme rozhranie v angličtine, ale výstup nastavíme na slovenčinu. Overíme jazyk jednej odpovede.

### Vychytávka 02 – Rozdelené zobrazenie v Google Chrome

**Split View** je funkcia **prehliadača Google Chrome**, nie samostatná funkcia Gemini Notebook. V jednom okne môžeme zobraziť dve webové stránky vedľa seba a porovnávať napríklad zdrojový dokument s odpoveďou v zošite.

| Platforma | Klávesová skratka |
|---|---|
| Windows a Linux | `Shift + Alt + N` |
| macOS | `Cmd + Option + N` |
| Chromebook | `Ctrl + Alt + N` |

**Postup:**

1. V Chrome otvoríme Gemini Notebook.
2. Aktivujeme Split View klávesovou skratkou alebo kontextovou ponukou karty.
3. V druhej časti otvoríme oficiálnu dokumentáciu alebo článok.
4. Kliknutím do jednotlivých častí prepíname aktívne zobrazenie.
5. Z ponuky Split View môžeme zobrazenia vymeniť, oddeliť alebo zavrieť.

V Split View je jedna časť aktívna. Príkazy ako Späť, Dopredu, Tlačiť alebo Preložiť sa vzťahujú na aktívnu časť. **Ctrl + W** zatvára aktuálnu kartu, preto nie je univerzálnym príkazom na bezpečné ukončenie iba jednej polovice Split View.

**Cvičenie:** Vľavo otvoríme [Gemini Notebook](https://notebook.google.com/), vpravo [oficiálny pomocník](https://support.google.com/gemininotebook/). Porovnáme tri kroky z dokumentácie s vlastným rozhraním.

### Tip 03 – Superpower for NotebookLM a rozšírené ovládanie

[Superpower for NotebookLM – Chrome Web Store](https://chromewebstore.google.com/detail/superpower-for-notebooklm/pghbifgajgeohldkdnlpedhcicccokla) je **rozšírenie tretej strany**. Podľa podkladov kurzu rozširuje možnosti organizácie zošitov, správy promptov, exportu, navigácie a počítadiel používania.

Príklady skratiek uvádzaných v školiacich podkladoch rozšírenia:

| Skratka | Funkcia | Pôvod |
|---|---|---|
| `Alt + Q` | Skryť alebo zobraziť panel Sources | Rozšírenie |
| `Alt + W` | Skryť alebo zobraziť panel Studio | Rozšírenie |
| `Alt + A` | Otvoriť pridávanie zdrojov | Rozšírenie |
| `Alt + P` | Otvoriť knižnicu promptov | Rozšírenie |
| `//` v poli zadania | Vyhľadať uložený prompt | Rozšírenie |

Skratky a dostupné funkcie overíme priamo v nainštalovanej verzii, pretože ich môže meniť nastavenie rozšírenia aj aktualizácia produktu. **Nie sú to oficiálne klávesové skratky NotebookLM.**

**Bezpečnostná poznámka:** Pred inštaláciou skontrolujeme oprávnenia rozšírenia a pravidlá spracovania dát. V zošitoch s citlivými firemnými alebo osobnými údajmi nainštalujeme iba doplnky schválené organizáciou.

**Cvičenie:** Pripravíme tri opakovateľné prompty, uložíme ich do knižnice rozšírenia a vyvoláme pomocou `//`. Porovnáme pohodlie používania so štandardným chatom bez doplnku.

<a id="kapitola-2"></a>
## 2. Placeholdery – zástupné symboly pre tvorbu promptov

**Placeholder** je zástupný text, ktorý pred odoslaním promptu nahradíme konkrétnou hodnotou. Najčastejšie používame zápis `[TÉMA]`, `[CIEĽOVÁ_SKUPINA]` alebo `[POČET_SLOV]`. Alternatívou sú zápisy `{TÉMA}` a `{{tema}}`. Ide o **techniku tvorby promptov, nie o vstavanú funkciu Gemini Notebook**: samotné hranaté alebo zložené zátvorky nezaručia automatické dosadzovanie údajov.

> [!TIP]
> V tomto dokumente používame štandardne **slovenské placeholdery v hranatých zátvorkách**. Pre školenie je vhodné najprv ukázať šablónu a potom predviesť jej vyplnenie na reálnych hodnotách.

### Základné placeholdery

| Anglický zápis | Slovenský zápis | Význam |
|---|---|---|
| `[TOPIC]` | `[TÉMA]` | Hlavná téma |
| `[TASK]` | `[ÚLOHA]` | Konkrétna činnosť |
| `[ROLE]` | `[ROLA]` | Rola alebo perspektíva |
| `[CONTEXT]` | `[KONTEXT]` | Súvislosti |
| `[GOAL]` | `[CIEĽ]` | Požadovaný výsledok |
| `[INPUT]` | `[VSTUP]` | Vstupné údaje |
| `[OUTPUT]` | `[VÝSTUP]` | Očakávaný výsledok |
| `[INSTRUCTIONS]` | `[INŠTRUKCIE]` | Pravidlá |
| `[EXAMPLE]` | `[PRÍKLAD]` | Vzorové riešenie |
| `[CONSTRAINTS]` | `[OBMEDZENIA]` | Obmedzenia zadania |

### Placeholdery pre zdroje a dokumenty

| Anglický zápis | Slovenský zápis | Význam |
|---|---|---|
| `[SOURCE]` | `[ZDROJ]` | Konkrétny zdroj |
| `[SOURCE_NAME]` | `[NÁZOV_ZDROJA]` | Názov zdroja |
| `[DOCUMENT]` | `[DOKUMENT]` | Analyzovaný dokument |
| `[FILE_NAME]` | `[NÁZOV_SÚBORU]` | Názov súboru |
| `[CHAPTER]` | `[KAPITOLA]` | Kapitola |
| `[SECTION]` | `[SEKCIA]` | Časť dokumentu |
| `[PAGE]` | `[STRANA]` | Číslo strany |
| `[KEYWORDS]` | `[KĽÚČOVÉ_SLOVÁ]` | Kľúčové výrazy |
| `[QUESTION]` | `[OTÁZKA]` | Otázka |
| `[DATE_RANGE]` | `[ČASOVÉ_OBDOBIE]` | Časový interval |

### Placeholdery pre formátovanie

| Anglický zápis | Slovenský zápis | Význam |
|---|---|---|
| `[LANGUAGE]` | `[JAZYK]` | Jazyk výstupu |
| `[TONE]` | `[TÓN]` | Tón komunikácie |
| `[STYLE]` | `[ŠTÝL]` | Štylistická úprava |
| `[FORMAT]` | `[FORMÁT]` | Tabuľka, text, JSON a pod. |
| `[LENGTH]` | `[DĹŽKA]` | Rozsah |
| `[WORD_COUNT]` | `[POČET_SLOV]` | Počet slov |
| `[STRUCTURE]` | `[ŠTRUKTÚRA]` | Členenie obsahu |
| `[DETAIL_LEVEL]` | `[ÚROVEŇ_DETAILOV]` | Požadovaná podrobnosť |
| `[NUMBER_OF_ITEMS]` | `[POČET_POLOŽIEK]` | Počet položiek |
| `[OUTPUT_TYPE]` | `[TYP_VÝSTUPU]` | Typ požadovaného výstupu |

### Placeholdery pre vzdelávanie, výskum a analýzu

| Anglický zápis | Slovenský zápis | Význam |
|---|---|---|
| `[AUDIENCE]` | `[CIEĽOVÁ_SKUPINA]` | Používatelia výstupu |
| `[SKILL_LEVEL]` | `[ÚROVEŇ_ZNALOSTÍ]` | Predchádzajúce znalosti |
| `[LEARNING_OBJECTIVE]` | `[VZDELÁVACÍ_CIEĽ]` | Čo sa má študent naučiť |
| `[COURSE_NAME]` | `[NÁZOV_KURZU]` | Názov kurzu |
| `[LESSON]` | `[LEKCIA]` | Konkrétna lekcia |
| `[CASE_STUDY]` | `[PRÍPADOVÁ_ŠTÚDIA]` | Praktický scenár |
| `[METHODOLOGY]` | `[METODIKA]` | Metóda analýzy |
| `[CRITERIA]` | `[KRITÉRIÁ]` | Hodnotiace kritériá |
| `[METRICS]` | `[METRIKY]` | Merateľné ukazovatele |
| `[RECOMMENDATIONS]` | `[ODPORÚČANIA]` | Požadované odporúčania |

### Univerzálny prompt s placeholdermi

~~~text
Na základe vybraných zdrojov spracuj tému [TÉMA].

Rola: [ROLA]
Cieľ: [CIEĽ]
Cieľová skupina: [CIEĽOVÁ_SKUPINA]
Úroveň znalostí: [ÚROVEŇ_ZNALOSTÍ]
Zdroj: [NÁZOV_ZDROJA]
Jazyk: [JAZYK]
Formát: [FORMÁT]
Rozsah: [POČET_SLOV] slov

Použi konkrétne príklady zo zdrojov, uveď citácie
a upozorni na informácie, ktoré sa v zdrojoch nenachádzajú.
~~~

**Konkrétne hodnoty na demonštráciu:**

| Placeholder | Nahradíme hodnotou |
|---|---|
| `[TÉMA]` | Geografické informačné systémy (GIS) |
| `[ROLA]` | Lektor geoinformatiky |
| `[CIEĽ]` | Vysvetliť rozdiel medzi QGIS, ArcGIS Pro a PostGIS |
| `[CIEĽOVÁ_SKUPINA]` | Začínajúci GIS analytici a IT pracovníci |
| `[ÚROVEŇ_ZNALOSTÍ]` | Začiatočníci |
| `[NÁZOV_ZDROJA]` | QGIS User Guide a ArcGIS Pro Documentation |
| `[JAZYK]` | Slovenčina |
| `[FORMÁT]` | Porovnávacia tabuľka s praktickými príkladmi |
| `[POČET_SLOV]` | 400 |

**Podmienka:** Názvy dokumentov v prompte musia zodpovedať skutočne dostupným alebo vybraným zdrojom. Model nemá predstierať, že čítal dokument, ktorý do zošita nebol pridaný.

<a id="kapitola-3"></a>
## 3. Pätnásť praktických promptov s konkrétnymi hodnotami

Nasledujúce šablóny vychádzajú z dodaného materiálu `obsahy.md` a používajú jednotný slovenský zápis placeholderov. Môžeme ich kopírovať priamo do chatu Gemini Notebook. **Pred použitím nahradíme všetky placeholdery hodnotami v tabuľkách a vyberieme zodpovedajúce zdroje.**

### Prompt 01 – Súhrn zdrojového dokumentu

~~~text
Zhrň najdôležitejšie informácie zo zdroja [NÁZOV_ZDROJA]
v rozsahu [POČET_SLOV] slov. Súhrn prispôsob cieľovej skupine
[CIEĽOVÁ_SKUPINA] s úrovňou znalostí [ÚROVEŇ_ZNALOSTÍ].

Identifikuj hlavné myšlienky, kľúčové fakty, dôležité čísla,
závery a odporúčania. Výstup rozdeľ na logické časti s nadpismi.
Zásadné tvrdenia podlož citáciami. Chýbajúce informácie nevymýšľaj.
~~~

| Placeholder | Konkrétna hodnota |
|---|---|
| `[NÁZOV_ZDROJA]` | Oficiálna používateľská príručka Google NotebookLM |
| `[POČET_SLOV]` | 300 |
| `[CIEĽOVÁ_SKUPINA]` | Lektori, učitelia a pracovníci vo vzdelávaní |
| `[ÚROVEŇ_ZNALOSTÍ]` | Mierne pokročilí |

**Výstup:** prehľadný súhrn vhodný na prípravu školenia.

### Prompt 02 – Kľúčové pojmy a definície

~~~text
Na základe vybraných zdrojov identifikuj [POČET_POJMOV]
najdôležitejších pojmov súvisiacich s témou [TÉMA].

Každý pojem vysvetli pre skupinu [CIEĽOVÁ_SKUPINA].
Doplň odbornú definíciu, jednoduché vysvetlenie, praktický
príklad a súvisiace pojmy.

Výsledok priprav ako tabuľku:
Pojem | Definícia | Praktický príklad | Zdroj.
Použi len informácie podložené dostupnými zdrojmi.
~~~

| Placeholder | Konkrétna hodnota |
|---|---|
| `[POČET_POJMOV]` | 15 |
| `[TÉMA]` | Geografické informačné systémy (GIS), QGIS, ArcGIS a PostGIS |
| `[CIEĽOVÁ_SKUPINA]` | Začínajúci GIS analytici a IT špecialisti |

**Výstup:** terminologický slovník s príkladmi.

### Prompt 03 – Porovnanie dvoch dokumentov

~~~text
Porovnaj dokumenty [PRVÝ_DOKUMENT] a [DRUHÝ_DOKUMENT]
z hľadiska [KRITÉRIÁ_POROVNANIA].

Identifikuj spoločné vlastnosti, rozdiely, výhody, nevýhody
a prípadné protirečenia. Vytvor podrobnú porovnávaciu tabuľku
a krátke zhrnutie praktického významu rozdielov.

Pri zásadných tvrdeniach uveď citácie z oboch zdrojov.
Ak dokumenty neposkytujú dostatok údajov, otvorene to uveď.
~~~

| Placeholder | Konkrétna hodnota |
|---|---|
| `[PRVÝ_DOKUMENT]` | QGIS User Guide |
| `[DRUHÝ_DOKUMENT]` | ArcGIS Pro Documentation |
| `[KRITÉRIÁ_POROVNANIA]` | Vektorové a rastrové dáta, súradnicové systémy, priestorové analýzy, automatizácia a export máp |

**Výstup:** porovnávacia matica s citáciami. *Poznámka: porovnávame iba oblasti skutočne pokryté importovanými dokumentmi.*

### Prompt 04 – Praktické otázky a odpovede

~~~text
Na základe zdrojov priprav [POČET_OTÁZOK] praktických otázok
a odpovedí na tému [TÉMA].

Otázky prispôsob cieľovej skupine [CIEĽOVÁ_SKUPINA]
a úrovni [ÚROVEŇ_ZNALOSTÍ]. Kombinuj pochopenie princípov,
reálne situácie a riešenie problémov.

Ku každej otázke doplň správnu odpoveď, krátky praktický
príklad a citáciu zdroja. Neuvádzaj nepodložené právne závery.
~~~

| Placeholder | Konkrétna hodnota |
|---|---|
| `[POČET_OTÁZOK]` | 10 |
| `[TÉMA]` | GDPR pri používaní umelej inteligencie |
| `[CIEĽOVÁ_SKUPINA]` | Zamestnanci a manažéri malých a stredných podnikov |
| `[ÚROVEŇ_ZNALOSTÍ]` | Začiatočníci |

**Výstup:** sada otázok pre diskusiu a samokontrolu.

### Prompt 05 – Vedomostný test s odpoveďami

~~~text
Vytvor vedomostný test s [POČET_OTÁZOK] otázkami na tému
[TÉMA] pre úroveň [ÚROVEŇ_ZNALOSTÍ].

Každá otázka má mať možnosti A, B, C a D.
Presne jedna možnosť musí byť správna. Zameraj sa na
porozumenie, použitie poznatkov a praktické situácie.

Na konci vytvor samostatný kľúč správnych odpovedí
s krátkym vysvetlením a citáciou zdroja.
~~~

| Placeholder | Konkrétna hodnota |
|---|---|
| `[POČET_OTÁZOK]` | 15 |
| `[TÉMA]` | Gemini Notebook, citácie, zdroje, Fast Research a Deep Research |
| `[ÚROVEŇ_ZNALOSTÍ]` | Mierne pokročilí |

**Výstup:** 15 testových otázok so zdôvodnením správnej odpovede.

### Prompt 06 – Praktické príklady využitia v praxi

~~~text
Z dostupných zdrojov priprav [POČET_PRÍKLADOV] praktických
príkladov využitia [TÉMA] v oblasti [OBLASŤ_VYUŽITIA].

Pri každom príklade uveď:
1. situáciu alebo problém,
2. cieľ,
3. postup riešenia,
4. potrebné nástroje,
5. očakávaný výsledok,
6. chyby, riziká a odporúčania.

Rozlišuj medzi príkladmi doloženými v zdrojoch a vlastnými
návrhmi. Návrhy jasne označ a nevydávaj ich za overenú prax.
~~~

| Placeholder | Konkrétna hodnota |
|---|---|
| `[POČET_PRÍKLADOV]` | 8 |
| `[TÉMA]` | Generatívna AI a automatizácia pracovných procesov |
| `[OBLASŤ_VYUŽITIA]` | Administratíva, marketing, zákaznícka podpora, personalistika a vzdelávanie |

**Výstup:** katalóg scenárov na implementáciu alebo školenie.

### Prompt 07 – Praktický návod krok za krokom

~~~text
Podľa dostupnej dokumentácie vytvor presný návod na úlohu
[ÚLOHA] v nástroji [NÁZOV_NÁSTROJA].

Návod prispôsob úrovni [ÚROVEŇ_ZNALOSTÍ]. Jednotlivé
kroky očísluj. Pri každom vysvetli, kde sa nachádza
funkcia, aké nastavenia použiť a ako overiť výsledok.

Doplň časté chyby a ich riešenia. Používaj terminológiu
oficiálnej dokumentácie. Nedoložené kroky označ.
~~~

| Placeholder | Konkrétna hodnota |
|---|---|
| `[ÚLOHA]` | Import CSV, čistenie údajov, odstránenie duplicít a spojenie tabuliek |
| `[NÁZOV_NÁSTROJA]` | Microsoft Excel Power Query |
| `[ÚROVEŇ_ZNALOSTÍ]` | Začiatočníci a mierne pokročilí |

**Výstup:** pracovný postup na zopakovanie v Exceli.

### Prompt 08 – Osnova online kurzu a školenia

~~~text
Z vybraných zdrojov priprav osnovu školenia [NÁZOV_KURZU]
pre skupinu [CIEĽOVÁ_SKUPINA] s úrovňou [ÚROVEŇ_ZNALOSTÍ].

Dĺžka školenia: [DĹŽKA_ŠKOLENIA] minút.
Obsah rozdeľ na kapitoly a lekcie. Ku každej lekcii doplň
cieľ, hlavné témy, praktické cvičenie a odporúčaný čas.

Zameraj sa na reálne ukážky, priebežné overenie vedomostí
a záverečné praktické zadanie. Súčet časov musí zodpovedať
celkovému rozsahu. Uveď, ktoré časti vyplývajú zo zdrojov
a ktoré sú didaktickým návrhom.
~~~

| Placeholder | Konkrétna hodnota |
|---|---|
| `[NÁZOV_KURZU]` | GIS – QGIS, ArcGIS Pro a PostGIS |
| `[CIEĽOVÁ_SKUPINA]` | GIS analytici, IT pracovníci, geografi a pracovníci verejnej správy |
| `[ÚROVEŇ_ZNALOSTÍ]` | Začiatočníci |
| `[DĹŽKA_ŠKOLENIA]` | 90 |

**Výstup:** časovo vyvážená osnova so zadaniami.

### Prompt 09 – Praktické cvičenia a domáce úlohy

~~~text
Na základe zdrojov priprav [POČET_CVIČENÍ] praktických
cvičení na tému [TÉMA] pre úroveň [ÚROVEŇ_ZNALOSTÍ].

Pri každom uveď názov, cieľ, vstupné znalosti, nástroje,
zadanie, odporúčaný postup a očakávaný výsledok.
Zoraď cvičenia od najjednoduchších po najnáročnejšie.

Doplň kritériá hodnotenia a ukážku riešenia.
Vychádzaj z prostredia [OBLASŤ_VYUŽITIA].
Ak zadanie vyžaduje neexistujúce testovacie dáta,
najprv navrhni ich štruktúru a označ ich ako modelové.
~~~

| Placeholder | Konkrétna hodnota |
|---|---|
| `[POČET_CVIČENÍ]` | 6 |
| `[TÉMA]` | SQL dopyty, JOIN, filtrovanie a agregácia údajov |
| `[ÚROVEŇ_ZNALOSTÍ]` | Mierne pokročilí |
| `[OBLASŤ_VYUŽITIA]` | Analýza obchodných údajov a reportovanie v PostgreSQL |

**Výstup:** súbor domácich úloh a hodnotiacich kritérií.

### Prompt 10 – Výhody, nevýhody a riziká

~~~text
Na základe dostupných zdrojov analyzuj riešenie
[NÁZOV_RIEŠENIA] pri jeho použití v [OBLASŤ_VYUŽITIA].

Preskúmaj technické, ekonomické, organizačné, bezpečnostné
a prevádzkové aspekty. Spracuj tabuľku:
Kritérium | Výhoda | Nevýhoda alebo riziko | Opatrenie | Zdroj.

Na konci uveď, kedy je riešenie vhodné a kedy zvažovať
alternatívy. Odlišuj doložené fakty od odhadov.
~~~

| Placeholder | Konkrétna hodnota |
|---|---|
| `[NÁZOV_RIEŠENIA]` | Zavedenie AI chatbotov a AI agentov do firemných procesov |
| `[OBLASŤ_VYUŽITIA]` | Zákaznícka podpora a automatizácia komunikácie v e-commerce |

**Výstup:** podklad na rozhodovanie.

### Prompt 11 – Chronologický prehľad udalostí

~~~text
Vytvor chronologický prehľad vývoja [TÉMA]
v období [ČASOVÉ_OBDOBIE].

Pri každej udalosti uveď dátum, opis, význam,
praktický dôsledok a citáciu zdroja.

Usporiadaj výsledky chronologicky do tabuľky.
Na konci vysvetli hlavné trendy. Neoverené dátumy
neprezentuj ako potvrdené.
~~~

| Placeholder | Konkrétna hodnota |
|---|---|
| `[TÉMA]` | Vývoj generatívnej AI, veľkých jazykových modelov a ChatGPT, Google Gemini a Claude |
| `[ČASOVÉ_OBDOBIE]` | November 2022 až október 2026 |

**Výstup:** časová os a prehľad technologických míľnikov.

### Prompt 12 – Analýza vedeckej publikácie

~~~text
Vypracuj odbornú analýzu publikácie [NÁZOV_PUBLIKÁCIE].

Identifikuj autorov, rok, výskumný problém, cieľ, otázky,
hypotézy, metodiku, výskumnú vzorku a výsledky, ak sa
tieto prvky v publikácii nachádzajú.

Kriticky vyhodnoť prínos, obmedzenia metodiky, silu dôkazov
a primeranosť záverov. Všetko podlož citáciami.
Neuvádzaj hypotézy či experimenty, ktoré článok neobsahuje.
~~~

| Placeholder | Konkrétna hodnota |
|---|---|
| `[NÁZOV_PUBLIKÁCIE]` | Attention Is All You Need (Vaswani a kol., 2017) |

**Výstup:** kritická analýza vedeckého článku.

### Prompt 13 – Rozpory medzi zdrojmi

~~~text
Porovnaj vybrané zdroje k téme [TÉMA].
Identifikuj tvrdenia, závery a odporúčania, v ktorých
sa zdroje rozchádzajú.

V tabuľke uveď: Sporná otázka | Zdroj A a tvrdenie |
Zdroj B a tvrdenie | Citácie | Možná príčina rozdielu.

Zohľadni aktuálnosť, kvalitu metodiky, mieru dôveryhodnosti
a kontext. Nerozhodni svojvoľne, ktorý zdroj má pravdu.
Oddeľ najlepšie doložené závery od otvorených otázok.
~~~

| Placeholder | Konkrétna hodnota |
|---|---|
| `[TÉMA]` | Vplyv generatívnej AI na produktivitu zamestnancov, kvalitu práce a zamestnanosť |

**Výstup:** matica rozporov a otázok na ďalšie overenie.

### Prompt 14 – Praktický kontrolný zoznam

~~~text
Na základe dokumentov priprav kontrolný zoznam pre proces
[NÁZOV_PROCESU] v prostredí [TYP_ORGANIZÁCIE].

Úlohy rozdeľ na fázy. Ku každej uveď činnosť,
požadovaný výsledok, spôsob kontroly a hlavné riziká.
Výstup vytvor ako zoznam so zaškrtávacími políčkami.

Ak podklady neobsahujú povinné požiadavky alebo ich
aktuálne znenie, označ ich na právne či metodické overenie.
~~~

| Placeholder | Konkrétna hodnota |
|---|---|
| `[NÁZOV_PROCESU]` | Zavedenie generatívnej AI do firmy v súlade s GDPR a AI Act |
| `[TYP_ORGANIZÁCIE]` | Malá alebo stredná firma poskytujúca online vzdelávanie a školenia |

**Výstup:** implementačný checklist s kontrolnými bodmi.

### Prompt 15 – Manažérsky súhrn a odporúčania

~~~text
Na základe zdrojov vytvor manažérsky súhrn na tému
[TÉMA] pre [CIEĽOVÁ_SKUPINA] v rozsahu [POČET_SLOV] slov.

Zahrň najdôležitejšie fakty, čísla, riziká, príležitosti
a dopady na rozhodovanie. Zistenia zoraď podľa významu.

Na záver odporuč 3 až 5 konkrétnych opatrení.
Pri každom vysvetli prínos a uveď zdroj.
Nezamieňaj predpoklady, odhady a potvrdené výsledky.
~~~

| Placeholder | Konkrétna hodnota |
|---|---|
| `[TÉMA]` | Ekonomické prínosy, náklady a riziká zavedenia AI nástrojov do firemných procesov |
| `[CIEĽOVÁ_SKUPINA]` | Konatelia, riaditelia a vrcholoví manažéri MSP |
| `[POČET_SLOV]` | 400 |

**Výstup:** krátky rozhodovací dokument s prioritizovanými opatreniami.

### Mini-cvičenie – kontrola placeholderov

Pred odoslaním promptu si overíme, že v ňom nezostali nevyriešené symboly typu `[TÉMA]`, že zadané zdroje naozaj existujú v zošite a že požadovaný formát zodpovedá úlohe. Rovnaký prompt potom skúsime s dvoma cieľovými skupinami a porovnáme štruktúru výsledkov.

<a id="kapitola-4"></a>
## 4. Fast Research a Deep Research

### Kedy použiť ktorý režim

**Fast Research** slúži najmä na **rýchle nájdenie konkrétnych relevantných zdrojov** z webu alebo zo súborov v Google Drive, ku ktorým máme prístup. Výsledky si môžeme pred importom prezrieť a vybrať z nich podklady vhodné do zošita.

**Deep Research** využijeme pri **komplexnejšej výskumnej otázke**, porovnávaní väčšieho množstva webových zdrojov a tvorbe rozsiahlejšej výskumnej správy. Môže prehľadávať až stovky webových stránok a výslednú správu aj zdroje ponúknuť na import. Spracovanie spravidla trvá dlhšie.

| Kritérium | Fast Research | Deep Research |
|---|---|---|
| Hlavný cieľ | Nájsť vhodné zdroje | Preskúmať problém do hĺbky |
| Typický čas | Kratší | Dlhší, často niekoľko minút |
| Vstup | Hľadaný pojem alebo konkrétna otázka | Presne ohraničená výskumná otázka |
| Web | Áno | Áno |
| Google Drive | Áno, ako voľba vyhľadávania | Nie ako samostatný zdroj vyhľadávania Deep Research v popísanom postupe |
| Výstup | Návrhy relevantných dokumentov | Výskumná správa a zoznam zdrojov |
| Kontrola pred importom | Áno | Áno |
| Hlavné riziko | Slabé alebo duplicitné zdroje | Neúplná rešerš a prehnane istá syntéza |

### Praktické situácie pre Fast Research

| Praktická situácia | Prečo používame Fast Research |
|---|---|
| Hľadáme oficiálnu dokumentáciu Pythonu 3.14 | Potrebujeme konkrétnu technickú dokumentáciu |
| Hľadáme odborné články o QGIS a ArcGIS | Chceme relevantné odborné podklady |
| Hľadáme materiály k predmetu na Google Drive | Vyhľadávame dostupné vlastné dokumenty |
| Potrebujeme najnovšie odborné publikácie o AI | Najprv identifikujeme vhodné publikácie |
| Hľadáme aktuálne informácie o GDPR a AI Act | Potrebujeme oficiálne znenia a usmernenia |
| Hľadáme návody ku Google Analytics 4 | Chceme dokumentáciu a praktické postupy |
| Hľadáme vedecké články k dizertačnej práci | Potrebujeme akademické zdroje |
| Hľadáme príručky k Excelu a Power BI | Hľadáme technické a školiace materiály |
| Hľadáme informácie o nových funkciách ChatGPT a Gemini | Identifikujeme aktuálne oficiálne zdroje |
| Hľadáme firemné smernice na Google Drive | Vyhľadávame konkrétne interné dokumenty |
| Hľadáme prezentácie na pripravované školenie | Zhromažďujeme vhodné podklady |
| Hľadáme návody ku Dockeru a Kubernetes | Potrebujeme postupy a konfigurácie |
| Hľadáme odporúčania Google Search Central | Uprednostníme metodiky Googlu |
| Hľadáme výročné správy spoločnosti | Identifikujeme primárne finančné dokumenty |
| Hľadáme odporúčania NBÚ, NÚKIB a ENISA | Vyberáme autoritatívne bezpečnostné zdroje |
| Hľadáme riešenie konkrétnej chyby Windows 11 | Potrebujeme nájsť presný návod |

### Praktické situácie pre Deep Research

| Praktická situácia | Prečo používame Deep Research |
|---|---|
| Porovnávame Python, Java a C# | Analyzujeme výkonnosť, bezpečnosť a použitie |
| Porovnávame QGIS a ArcGIS Pro | Potrebujeme syntézu funkcií, nákladov a obmedzení |
| Skúmame vplyv AI na pracovný trh do roku 2030 | Porovnávame prognózy a metodiky |
| Pripravujeme rešerš k dizertačnej práci | Identifikujeme poznatky a výskumné medzery |
| Analyzujeme konkurenciu online vzdelávania v SR a ČR | Porovnávame trh a pozície organizácií |
| Porovnávame ChatGPT, Gemini a Claude | Potrebujeme viacero kritérií a zdrojov |
| Vyberáme CRM pre malú alebo strednú firmu | Porovnávame produkty a náklady |
| Skúmame dopady AI Act a GDPR na podnik | Analyzujeme právne a procesné súvislosti |
| Pripravujeme komplexnú SEO stratégiu e-shopu | Prepájame trendy, konkurenciu a obsah |
| Porovnávame AWS, Azure a Google Cloud | Analyzujeme architektúru, ceny a bezpečnosť |
| Skúmame AI vo vzdelávaní dospelých | Syntetizujeme vedecké zistenia |
| Porovnávame SAP a Microsoft Dynamics 365 | Hodnotíme ERP, integrácie a riziká |
| Pripravujeme vstup firmy na zahraničný trh | Potrebujeme analýzu trhu a regulácie |
| Skúmame kybernetické hrozby v roku 2026 | Porovnávame bezpečnostné správy |
| Vyhodnocujeme Google Ads, Meta Ads a SEO | Skúmame metriky a návratnosť |
| Plánujeme automatizáciu procesov a AI agentov | Potrebujeme strategickú analýzu |

### Cvičenie 08 – Fast Research a selekcia zdrojov

1. Vo vyhľadávaní zdrojov vyberieme **Web → Fast Research**.
2. Zadáme tému z oblasti vzdelávania dospelých.
3. Získame aspoň 10 výsledkov.
4. Pri každom vyhodnotíme **autora, dátum, primárnosť zdroja, relevanciu a duplicitu**.
5. Importujeme iba **5 najlepších zdrojov**.
6. Overíme, či zdroje skutočne podporujú položenú otázku.

**Vzorový dopyt:**

~~~text
Vyhľadaj aktuálne odborné a oficiálne zdroje o využití
generatívnej umelej inteligencie vo vzdelávaní dospelých.
Zameraj sa na online kurzy, personalizáciu výučby
a tvorbu študijných materiálov.
Uprednostni univerzity, výskumné organizácie a primárne zdroje.
~~~

### Tip 09 – Štítky a organizácia zdrojov

Pri **5 a viac zdrojoch** môže Gemini Notebook automaticky navrhnúť štítky a kategorizáciu. Štítky môžeme podľa dostupného rozhrania dopĺňať, premenovať a upravovať.

Odporúčané štítky:

- **Oficiálna dokumentácia**
- **Vedecké publikácie a odborné články**
- **Blogy, návody a videá**
- **Vlastné poznámky a pracovné syntézy**

Štítok pomáha s organizáciou, **nie je však zárukou odbornej kvality zdroja**.

### Cvičenia 10 a 11 – Kvalita zadania pre Deep Research

**Slabé zadanie:**

~~~text
Preskúmaj, ako univerzity využívajú umelú inteligenciu vo vzdelávaní.
~~~

**Presnejšie zadanie:**

~~~text
Preskúmaj, ako európske univerzity v rokoch 2024 až 2026
využívajú generatívnu AI pri tvorbe študijných materiálov.
Porovnaj päť konkrétnych univerzít, ich pravidlá, doložené
príklady použitia a riziká ochrany osobných údajov.
Uprednostni oficiálne a primárne zdroje.
Výsledky spracuj do porovnávacej tabuľky s citáciami.
~~~

Spustíme oba varianty, porovnáme **relevanciu, čas spracovania, hĺbku výsledkov a kontrolovateľnosť citácií**. Po dokončení importujeme iba zdroje priamo súvisiace s otázkou.

### Spoločné porovnávacie cvičenie Fast vs. Deep

Rovnakú otázku použijeme v oboch režimoch:

~~~text
Aké sú najdôležitejšie možnosti využitia umelej inteligencie
vo vzdelávaní dospelých?
Zameraj sa na praktické využitie v online kurzoch,
personalizáciu učenia a tvorbu študijných materiálov.
~~~

| Hodnotíme | Čo sledujeme |
|---|---|
| Rýchlosť | Čas do získania prvých relevantných výsledkov |
| Rozsah | Počet a kvalitu použitých podkladov |
| Hĺbku | Ako presne je téma spracovaná |
| Citácie | Či vedú na tvrdenia v pôvodných dokumentoch |
| Použiteľnosť | Či výsledok podporuje konkrétne rozhodnutie |

> [!WARNING]
> Deep Research nenahrádza systematickú vedeckú rešerš podľa metodiky PRISMA ani odborné právne stanovisko. Pri vedeckých a legislatívnych témach musíme skontrolovať aktuálne primárne zdroje.

<a id="kapitola-5"></a>
## 5. Poznámky a ich transformácie

Poznámky využijeme na uloženie zistení, pracovných záverov, citácií a otvorených otázok. Materiály kurzu zachytávajú staršie usporiadanie poznámok v **Studio**. Aktuálna dokumentácia Googlu uvádza aj **poznámky priamo v Sources**, ktoré sa môžu používať ako zdroje v chate a pri generovaní výstupov.

### Vychytávka 17 – Save to note

1. V chate vygenerujeme odpoveď.
2. Skontrolujeme rozhodujúce citácie.
3. Zvolíme **Save to note**.
4. Pomenujeme a zorganizujeme uložené zistenie.

**Aktuálne spresnenie:** Staršie podklady uvádzajú, že poznámka uložená z chatu nie je editovateľná. Podľa novšej dokumentácie Googlu je **uložená odpoveď editovateľná po odstránení citácií**. Presné správanie závisí od dostupného rozhrania a typu poznámky.

### Tip 18 – Vlastná editovateľná poznámka

Podľa nového rozhrania môžeme vytvoriť poznámku v paneli **Sources → Create note**. V staršom rozhraní sa mohla nachádzať vo **Studio → Add note**.

Odporúčaná štruktúra:

~~~text
NÁZOV TÉMY

1. Hlavné zistenia
2. Dôležité čísla a definície
3. Citácie a názvy zdrojov
4. Otvorené otázky
5. Čo treba overiť
6. Odporúčané ďalšie kroky
~~~

### Vychytávka 19 – Convert to source

V starších zošitoch sa poznámky vytvorené v Studio dajú konvertovať medzi zdroje, aby sa mohli použiť pri odpovediach a tvorbe výstupov. V novšom rozhraní vznikajú poznámky priamo v Sources, takže konverzia nemusí byť potrebná.

**Bezpečný postup:** vytvoríme syntézu → porovnáme ju s pôvodnými zdrojmi → opravíme nepresnosti → až potom ju použijeme ako ďalší zdroj.

### Tip 20 – Vyhnime sa zacykleniu chýb

Keď model vytvorí nesprávnu syntézu a my ju následne použijeme ako nový zdroj, môže začať citovať vlastnú chybu. Originálne dokumenty si preto ponecháme, syntetické poznámky zreteľne označíme a citácie kontrolujeme voči primárnym podkladom.

### Vychytávka 21 – Rýchle transformácie poznámok

| Transformácia | Účel | Odporúčaný výstup |
|---|---|---|
| Zlúčenie | Spojiť poznámky | Jedna štruktúrovaná syntéza |
| Skrátenie | Odstrániť duplicity | Stručný súhrn |
| Osnova | Zmeniť text na plán | Kapitoly a lekcie |
| Spätná väzba | Kriticky vyhodnotiť text | Silné a slabé miesta |
| Študijný materiál | Pripraviť podklad na učenie | Zhrnutie, otázky a pojmy |

**Cvičenie:** Z troch článkov pripravíme dve poznámky. Jednu skrátime, druhú zmeníme na osnovu 30-minútového školenia. Pri oboch skontrolujeme minimálne tri citácie.

<a id="kapitola-6"></a>
## 6. Viditeľné vodoznaky, SynthID, C2PA a EXIF

### Viditeľný vodoznak verzus neviditeľný SynthID

Niektoré platené tarify podporujú **ovládanie viditeľného vodoznaku** na generovaných vizuálnych výstupoch. Podľa aktuálnej dokumentácie Googlu patrí táto možnosť medzi oprávnenia programu **Google AI Pro alebo Ultra** (s regionálnymi obmedzeniami); **Google AI Plus** túto výhodu nemá.

V aktuálnom rozhraní môže byť voľba **Visible watermarking** v ponuke používateľského profilu; v starších podkladoch je zachytená ako **Nastavenia → Odstrániť vodoznaky**.

> [!IMPORTANT]
> Vypnutie **viditeľného vodoznaku** nie je odstránenie **neviditeľného SynthID**. Sú to odlišné mechanizmy. SynthID je vkladaný do podporovaného AI obsahu a slúži na identifikáciu jeho pôvodu.

### Porovnanie technológií

| Technológia | Čo sleduje | Čo nepreukazuje |
|---|---|---|
| **SynthID** | Neviditeľný vodoznak vložený podporovaným AI systémom | Nie je univerzálny detektor každého AI výstupu |
| **C2PA / Content Credentials** | Overiteľné záznamy o pôvode a histórii súboru, ak ich súbor obsahuje | Nezaručuje pravdivosť samotného obsahu |
| **EXIF** | Technické metadáta – zariadenie, dátum, softvér a pod. | Samotný EXIF nie je dôkaz AI pôvodu |
| **GPTZero a podobné detektory** | Pravdepodobnostný odhad podľa vlastnej metodiky | Nie sú jednoznačným dôkazom autorstva ani používania AI |

**Kritická zásada:** Ak sa SynthID alebo C2PA nenájde, **neznamená to automaticky, že súbor nebol vytvorený AI**. Metadáta môžu chýbať, byť odstránené alebo sa nemusia používať; vodoznak nemusí byť v každom súbore podporovaný či detegovateľný.

### Cvičenie – Kontrola SynthID cez Gemini

1. Pripravíme testovací obrázok vytvorený podporovaným AI nástrojom.
2. Otvoríme [Gemini](https://gemini.google.com/).
3. Nahráme súbor a položíme overovaciu otázku.
4. Preskúmame, či nástroj identifikoval vodoznak a akú mieru istoty uvádza.
5. Výsledok zapíšeme ako **zistenie o vodoznaku**, nie všeobecný verdikt o pravosti.

**Ukážkové otázky:**

~~~text
Bol tento obrázok vytvorený alebo upravený pomocou AI od Googlu?
~~~

~~~text
Obsahuje tento súbor identifikovateľný digitálny vodoznak SynthID?
Vysvetli, čo výsledok dokazuje a čo z neho nemožno vyvodiť.
~~~

Alternatívne môžeme preskúmať službu [SynthID Detector](https://synthid.com/), ak je dostupná nášmu účtu a podporuje zvolený typ súboru. Dostupné funkcie detektora nie sú totožné s overovaním v bežnom chate Gemini.

### Cvičenie – Overenie C2PA Content Credentials

1. Pripravíme pôvodný súbor, ktorý obsahuje Content Credentials.
2. Otvoríme [Adobe Content Credentials Inspect](https://contentcredentials.org/verify) alebo kompatibilný validátor.
3. Nahráme súbor a skontrolujeme dostupný záznam o pôvode, použitých nástrojoch a úpravách.
4. Výsledok porovnáme s EXIF metadátami.
5. Rozlíšime **kryptograficky overiteľné tvrdenia o pôvode** od bežných editovateľných metadát.

Na technickú kontrolu metadát vo Windows môžeme použiť:

- [ExifTool](https://exiftool.org/) – nástroj na prácu s metadátami.
- [ExifToolGUI](https://exiftool.org/gui/) – grafické rozhranie k ExifToolu.

**Dôležité:** ExifTool vie zobraziť množstvo metadát, ale ich zobrazenie samo osebe nenahrádza **validáciu podpisov C2PA**. Na overenie integrity záznamov používame kompatibilný C2PA validátor.

### Ďalšie nástroje z podkladov

- [GPTZero](https://gptzero.me/) – doplnkový indikátor pri hodnotení textového obsahu.
- [Google DeepMind – SynthID](https://deepmind.google/models/synthid/) – technické vysvetlenie princípu.
- [Gemini – overovanie AI obsahu](https://support.google.com/gemini/answer/16722517?hl=en) – oficiálny návod.

**Etika a transparentnosť:** Vypnutie viditeľnej značky v rámci oprávnení účtu nesmie slúžiť na nepravdivé tvrdenie o pôvode obsahu. Pri práci s citlivými súbormi nepoužívame neoverené verejné detektory bez posúdenia ochrany údajov.

<a id="kapitola-7"></a>
## 7. Používanie a limity umelej inteligencie

Limity Gemini Notebook sa odvíjajú od **tarifu, typu funkcie a výpočtovej náročnosti**. Google v roku 2026 opisuje nielen počty zošitov a zdrojov, ale aj **AI usage** – spotrebu pri chate a generovaní výstupov.

### Ako zistiť zostávajúce využitie

1. Otvoríme Gemini Notebook.
2. V pravom hornom rohu vyberieme **Settings / Nastavenia**.
3. Otvoríme **Usage / Používanie**.
4. Skontrolujeme aktuálne využitie, dostupné limity a čas obnovenia.
5. Pri tvorbe Studio výstupu sledujeme prípadný ukazovateľ očakávanej spotreby.

Podľa dokumentácie sa pri niektorých výpočtových kvótach kapacita obnovuje približne v **päťhodinových intervaloch**, kým nedosiahneme týždenný limit. Ide o systém s meniacimi sa podmienkami; nekopírujeme preto staré snímky limitov ako garantované počty.

| Režim | Praktický význam |
|---|---|
| Bez predplatného / Standard | Základné limity |
| AI Plus | Vyššie využitie oproti Standard |
| AI Pro | Ďalšie navýšenie limitov; vybrané prémiové funkcie |
| AI Ultra | Najvyššie alebo rozšírené limity podľa variantu predplatného |

Presné limity a dostupnosť funkcií vždy skontrolujeme na [oficiálnej stránke tarifov](https://support.google.com/gemininotebook/answer/16213268?hl=en) a [stránke AI usage](https://support.google.com/gemininotebook/answer/17670842?hl=en).

### Praktické odporúčania na hospodárenie s limitmi

- Vyberáme len relevantné zdroje.
- Zbytočne neopakujeme rovnaký rozsiahly dopyt.
- Najprv pripravíme kvalitný prompt s rozsahom, kritériami a formátom.
- Zdĺhavé výstupy generujeme až po overení osnovy.
- Pri dostupnosti funkcie **Generate later** môžeme naplánovať odložené vygenerovanie artefaktu.

**Cvičenie:** Skontrolujeme stav AI usage, vytvoríme krátky a rozsiahly dopyt a porovnáme, čo ukazovateľ spotreby dovolí odpozorovať. Výsledok zaznamenáme bez predpokladu, že každé zadanie má rovnaké náklady.

<a id="kapitola-8"></a>
## 8. Audio Overview a interaktívny režim

### Formáty Audio Overview

| Formát | Na čo ho použijeme |
|---|---|
| **Deep Dive** | Dôkladnejšie vysvetlenie a prepojenie tém |
| **Brief** | Krátke zhrnutie podstatných informácií |
| **Critique** | Kritická a konštruktívna spätná väzba |
| **Debate** | Porovnanie rôznych pohľadov alebo argumentov |

Audio Overview podporuje **viac ako 80 jazykov vrátane slovenčiny**. To však neznamená, že všetky jazykové funkcie platia pre **Interactive Mode**.

### Cvičenie 26 – Porovnanie formátov

Z rovnakých zdrojov vytvoríme:

1. **Deep Dive** v slovenčine.
2. **Debate** v slovenčine.
3. Voliteľne **Brief** v angličtine.

Porovnáme, ktorý formát lepšie odhaľuje súvislosti, ktorý upozorňuje na rozpory a ktorý je najvhodnejší na rýchle opakovanie.

### Vychytávka – Interactive Mode

**Interaktívny režim je podľa aktuálnej dokumentácie dostupný iba v angličtine** a funguje s **novovytvorenými Audio Overviews**, pri ktorých sme zvolili príslušnú možnosť.

**Postup:**

1. V **Studio** otvoríme generovanie **Audio Overview**.
2. Vytvoríme nový prehľad a zvolíme **Interactive Mode**, ak je dostupný.
3. Spustíme prehrávanie.
4. Klikneme na **Join**.
5. Po vyzvaní položíme krátku otázku cez mikrofón.
6. Vypočujeme personalizovanú odpoveď a návrat k pôvodnému rozhovoru.

Pri už vytvorenom staršom audiu sa možnosť Join nemusí objaviť. Aj keď je bežný slovenský Audio Overview dostupný, interaktívny režim môže vyžadovať anglický jazyk.

### Praktické hlasové otázky v angličtine

Z prezentácie kurzu vyberáme tri postupne jednoduchšie varianty:

~~~text
Can you explain the most important findings from these sources
in simpler terms and give me one practical example?
~~~

~~~text
Explain the key findings from these sources simply
and give one practical example.
~~~

~~~text
Summarize these sources simply and give one example.
~~~

**Najjednoduchší variant pre účastníkov:** „Summarize these sources simply and give one example.“

**Doplňujúce otázky na precvičenie:**

~~~text
What is the main difference between these two sources?
~~~

~~~text
Can you give me an example from everyday work?
~~~

~~~text
Which finding should I remember first?
~~~

**Pozor:** Audio Overview je generovaný AI a môže obsahovať faktické chyby, zmeny hlasov alebo zvukové artefakty. Pri podstatných údajoch sa vrátime k pôvodným dokumentom.

### Oficiálna dokumentácia a užitočné nástroje

| Zdroj | Odkaz | Použitie |
|---|---|---|
| Gemini Notebook Help | https://support.google.com/gemininotebook/ | Hlavná dokumentácia |
| Vyhľadanie a pridávanie zdrojov | https://support.google.com/gemininotebook/answer/16215270?hl=en | Fast/Deep Research a štítky |
| Poznámky | https://support.google.com/gemininotebook/answer/16262519?hl=en | Editácia, vytvorenie a konverzia |
| Audio Overview | https://support.google.com/gemininotebook/answer/16212820?hl=en | Formáty a interaktívny režim |
| Jazyk výstupu | https://support.google.com/gemininotebook/answer/16261963?hl=en | Output Language |
| Plány a možnosti | https://support.google.com/gemininotebook/answer/16213268?hl=en | Tarify a vodoznaky |
| Používanie a limity AI | https://support.google.com/gemininotebook/answer/17670842?hl=en | Usage a obnova kvót |
| Chrome Split View | https://support.google.com/chrome/answer/16971124?hl=sk | Rozdelenie karty a skratky |
| Google SynthID | https://deepmind.google/models/synthid/ | Princíp neviditeľného vodoznaku |
| Overovanie v Gemini | https://support.google.com/gemini/answer/16722517?hl=en | Kontrola AI médií |
| SynthID Detector | https://synthid.com/ | Samostatný nástroj na podporované médiá |
| Content Credentials | https://contentcredentials.org/verify | Overovanie pôvodu súborov |
| ExifTool | https://exiftool.org/ | Technické metadáta |
| ExifToolGUI | https://exiftool.org/gui/ | Grafické zobrazenie metadát |
| Superpower for NotebookLM | https://chromewebstore.google.com/detail/superpower-for-notebooklm/pghbifgajgeohldkdnlpedhcicccokla | Neoficiálne rozšírenie |
| GPTZero | https://gptzero.me/ | Doplnkové orientačné posúdenie textu |

### Súvisiace materiály v repozitári

- [Prvá časť: Vychytávky, tipy a cvičenia](vychytavky_tipy_cvicenia.md)
- [Hlavný README](README.md)
- [Ťahák s promptmi](materials/04_Tahak_prompty.md)
- [Pracovný zošit účastníka](materials/02_Pracovny_zosit_ucastnika.md)
- [Riešenia a hodnotenie](materials/03_Riesenia_a_hodnotenie.md)

**Záver:** Pri práci s Gemini Notebook používame kombináciu **dobrých zdrojov, presných promptov, rozumne zvoleného režimu vyhľadávania a manuálnej kontroly dôkazov**. Samotný počet zdrojov, dĺžka odpovede ani prítomnosť citácií nie sú zárukou správneho výsledku.

