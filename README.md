# Letterlab — letterbord

Een klikbaar bord met letters, cijfers of getallen. Bij een klik hoor je de
klank of het getal; afhankelijk van de link verschijnt ook de grote letter of
het schrijffilmpje. Er is geen databank, geen account en geen bouwstap nodig.

Opnames en filmpjes komen uit **ligolimino.github.io/assets/**:

- klanken: `audio/klanken/` (ij en ei gebruiken `ij-ei.mp3`, au gebruikt `ou.mp3`)
- getallen: `audio/getallen/`
- schrijffilmpjes: `video/schrijven/<letter of cijfer>.mp4`

## Publiceren (eenmalig)

1. Maak bij **ligolimino** een openbare repository `letterbord`.
2. Upload de **inhoud** van deze map (`index.html` en `README.md`).
3. **Settings → Pages**: branch `main`, map `/ (root)`, **Save**.
4. Na enkele minuten: `https://ligolimino.github.io/letterbord/`.

## Mogelijkheden in de link

| In de link | Betekenis |
|---|---|
| `bord=letters` | alle letters en klanken (standaard) |
| `bord=cijfers` | 0 tot 9 |
| `bord=getallen` | 0 tot 50, per tiental |
| `modus=lezen` | klik = klank |
| `modus=groot` | klik = klank + grote letter |
| `modus=schrijven` | klik = klank + schrijffilmpje (standaard) |

Voorbeeld: `https://ligolimino.github.io/letterbord/?bord=getallen&modus=schrijven`

## Goed om te weten

- Is er voor een letter nog geen schrijffilmpje, dan toont het bord de grote
  letter. Een nieuw filmpje in `assets/video/schrijven/` wordt vanzelf gebruikt.
- Bij getallen van twee cijfers wordt eerst het filmpje van het eerste cijfer
  afgespeeld en daarna dat van het tweede, naast elkaar.
- Op een breed scherm staat elk tiental op één rij; op een smal scherm
  (gsm, tablet rechtop, Genially) in twee rijen van vijf.
- Linksonder staat een klein icoon: een open boek bij lezen en groot, een
  schrijvend potlood bij schrijven.
- Een bord toevoegen of aanpassen: bovenaan het script in `index.html`
  (`BORDEN`).
