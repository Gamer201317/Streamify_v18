# Streamify

Jouw persoonlijke streamingdienst — geen server, geen abonnement, alleen jouw bestanden.

> 💻 Open deze app op je iPad: `https://jouwnaam.github.io/streamify`

---

## Wat is Streamify?

Streamify is een **Progressive Web App (PWA)** die je lokale videobestanden toont als een echte streamingdienst. Je selecteert je bestanden op je iPad en Streamify maakt er een mooie bibliotheek van.

- ✅ Offline gebruik (werkt in het vliegtuig!)
- ✅ Geen account nodig
- ✅ Geen server, je bestanden blijven op je eigen apparaat
- ✅ Automatische series, collecties en covers op basis van bestandsnamen
- ✅ iPad geoptimaliseerd

---

## Hoe gebruik je Streamify?

Je kunt bestanden importeren als **losse bestanden** (handig op iPad, waar je geen hele mappen kunt selecteren) of als **mediamap** met submappen. Beide manieren werken door elkaar.

### 1. Films

Een film is elk videobestand zonder speciale prefix en zonder seizoen/aflevering in de naam. Zet een afbeelding met dezelfde naam ernaast voor een cover.

```
Movies/
├── Inception.mp4
└── Inception.jpg          ← cover (optioneel)
```

Of als losse bestanden:

```
Inception.mp4
Inception.jpg
```

### 2. Series

Een serie wordt herkend aan een **seizoen/aflevering** in de bestandsnaam. Het deel **voor** dat patroon is de serienaam. Zet een afbeelding met die serienaam ernaast voor een cover.

Ondersteunde patronen:

- `S01E01`, `S01E02`, `S02E01`
- `1x01`, `2x05`
- `Ep 1`, `Ep 2`
- `Episode 1`, `Episode 2`

```
Series/
└── Breaking Bad/
    ├── cover.jpg           ← seriecover (altijd "cover")
    ├── S01E01.mp4
    ├── S01E02.mp4
    └── S02E01.mp4
```

Of als losse bestanden:

```
Breaking Bad S01E01.mp4
Breaking Bad S01E02.mp4
Breaking Bad.jpg          ← cover
```

> 💡 **Serieherkenning:** alles met dezelfde naam voor `S01E01` wordt één serie. Dus `Breaking Bad S01E01.mp4` en `Breaking Bad S02E01.mp4` belanden samen.

### 3. Collecties

Een collectie groepeert meerdere films. Zet een `#` voor de bestandsnaam. Het eerste woord na de `#` is de collectienaam. De rest van de naam is de titel van dat item. Zet een afbeelding met die collectienaam ernaast voor de cover.

```
Collections/
└── Marvel/
    ├── cover.jpg
    ├── Iron Man.mp4
    ├── Thor.mp4
    └── The Avengers.mp4
```

Of als losse bestanden:

```
#Marvel Iron Man.mp4
#Marvel Thor.mp4
#Marvel.jpg             ← cover van de collectie
```

> 💡 **Tip:** Items uit een collectie verschijnen **ook automatisch** in het Films-tabblad, zodat je ze zowel los als in de groep kunt vinden.

---

## Bestandsnaam voorbeelden

| Type | Bestandsnaam | Wat gebeurt er |
|---|---|---|
| Film | `Inception.mp4` | Wordt een film |
| Film + cover | `Inception.mp4` + `Inception.jpg` | Film met cover |
| Serie | `Friends S01E01.mp4` | Aflevering van de serie **Friends** |
| Serie + cover | `Friends S01E01.mp4` + `Friends.jpg` | Serie **Friends** met cover |
| Collectie | `#Marvel Iron Man.mp4` | Item in collectie **Marvel** |
| Collectie + cover | `#Marvel Iron Man.mp4` + `#Marvel.jpg` | Collectie **Marvel** met cover |

---

## Eerste gebruik

1. Open de app via de link bovenaan deze pagina
2. Tik op **"Tik hier om te starten"**
3. Selecteer je videobestanden (en eventueel je cover-afbeeldingen)
4. Wacht tot de bibliotheek laadt
5. Wil je meer bestanden toevoegen? Tik opnieuw op de **+** knop — je huidige bibliotheek blijft behouden

## Mediamap opnieuw koppelen

Als je Streamify later opnieuw opent, kunnen je bestanden niet meer beschikbaar zijn (veiligheid van iOS). Tik dan op de **↺** knop op het startscherm en selecteer je bestanden opnieuw. Je voortgang, favorieten en bibliotheek blijven bewaard.

## Aan beginscherm toevoegen (aanbevolen)

1. Open de app in Safari
2. Tik het **Deel**-icoon onderin (□↑)
3. Kies **"Zet op beginscherm"**
4. Naam: Streamify → tik **Voeg toe**

Nu staat Streamify als app op je iPad, zonder adresbalk.

---

## Offline gebruik

De app slaat zichzelf automatisch op bij het eerste bezoek. Daarna werkt hij zonder internet — ideaal voor in het vliegtuig.

1. **Thuis** met WiFi: open de app één keer
2. **Onderweg**: zet vliegtuigmodus aan en open Streamify vanaf je beginscherm
3. De app en je mediabestanden werken gewoon

---

## Smart autoplay voor series

Als je een serie afspeelt, begint de volgende aflevering automatisch na 5 seconden. Wil je niet doorgaan? Tik op **Annuleren** tijdens de countdown.

---

## Metadata ophalen (posters, ratings, beschrijvingen)

Streamify kan automatisch extra informatie ophalen bij je films en series: poster, rating, jaar, genres, regisseur, cast en een korte beschrijving.

1. Vraag gratis een API-key aan bij **OMDb** (www.omdbapi.com/apikey.aspx)
2. Open in Streamify het tabblad **Instellingen**
3. Vul je OMDb API-key in en tik op **Sla API-key op**
4. Tik op **📥 Metadata ophalen**
5. Streamify zoekt elke film en serie, downloadt poster en metadata, en slaat alles lokaal op

> 💡 **Eén keer internet, daarna offline.** De metadata blijft in de app bewaard. Je hebt alleen bij het eerste ophalen internet nodig.

> ⚠️ **Let op:** de gedownloade poster en metadata worden opgeslagen in de app (IndexedDB), niet als losse bestanden naast je video's. Dat is nodig omdat een PWA in Safari/iPad niet terug kan schrijven naar je bestandssysteem.

> 🔐 **API-key veiligheid:** je OMDb API-key wordt lokaal in je browser opgeslagen. De app stuurt hem rechtstreeks naar OMDb vanuit je browser. Deel je key niet met anderen; iemand met je key kan je daglimiet gebruiken.

---

## Ondersteunde formaten

| Type | Extensies |
|---|---|
| Video | `.mp4` `.mkv` `.avi` `.mov` `.m4v` `.webm` `.ts` `.m2ts` |
| Cover | `.jpg` `.jpeg` `.png` `.webp` |

> ⚠️ **Beste formaat voor iPad:** `.mp4` met H.264 of H.265 — speelt altijd soepel af.

---

## Functies

- 📁 **Bibliotheek**: Films, Series en Collecties in aparte tabbladen
- ⭐ **Favorieten**: Tik het hartje op een poster
- 🔍 **Zoeken**: Zoek door je hele bibliotheek
- 🔄 **Vernieuwen**: Tik ↺ om je bestanden opnieuw te laden
- 📝 **Voortgang**: Hervat kijken waar je gestopt bent
- 📦 **Collectie-links**: Films tonen een badge met de bijbehorende collectie
- ⏭️ **Smart autoplay**: Volgende aflevering start automatisch

---

## Privacy

Streamify heeft **geen server**, slaat **niks online op** en heeft **geen tracking**. Al je bestanden blijven op je eigen iPad. Bibliotheek, voortgang en favorieten worden lokaal in de browser bewaard.

---

*Streamify v1.0 — Geen server. Geen abonnement. Alleen jouw bestanden.*
