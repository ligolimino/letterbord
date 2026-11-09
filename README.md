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
| `uitlijning=links` / `rechts` | rijen die niet vol zijn links of rechts (standaard: midden) |
| `icoon=lezen` / `luisteren` / `schrijven` / `geen` | ander icoontje (standaard: oor bij klank, leesblad bij grote letter, potlood bij schrijven) |

Voorbeeld: `https://ligolimino.github.io/letterbord/?bord=getallen&modus=schrijven`

### Een eigen bord

Het eenvoudigst: op de createpagina (`ligolimino.github.io/create/`, kies
*Letterbord*). Die maakt een link met `rijen=`:

`?rijen=ng,nk,sch|-|sl,sp,st&modus=schrijven`

- Elke rij gescheiden door `|`, de tekens door komma's.
- Een rij met alleen `-` is een lichte lijn, met `=` een donkere lijn.
- Klinkers worden vanzelf turquoise, de andere tekens donkerblauw.
- Getallen gebruiken de opnames uit `audio/getallen/`, de rest die uit
  `audio/klanken/`.
- Staat `rijen=` in de link, dan wordt `bord=` genegeerd.

## Goed om te weten

- Is er voor een letter nog geen schrijffilmpje, dan toont het bord de grote
  letter. Een nieuw filmpje in `assets/video/schrijven/` wordt vanzelf gebruikt.
- Getallen vanaf 10 krijgen geen schrijffilmpje: ze verschijnen groot.
- De klank start samen met het beeld: zodra het venster open is, of zodra
  het filmpje begint.
- Op een breed scherm staat elk tiental op één rij; op een smal scherm
  (gsm, tablet rechtop, Genially) in twee rijen van vijf.
- De tegels vullen het vak zo goed mogelijk. Wat overblijft is lege rand in
  één richting: maak het insluitvak in Genially in die richting kleiner.
- Het icoontje staat naast een korte laatste rij, aan de lege kant. Is de
  laatste rij vol, dan komt er een smalle strook onder.
- Alle klanken van het bord worden bij het openen al geladen, zodat ook de
  eerste klik meteen klinkt. De stilte vooraan in een opname wordt daarbij
  overgeslagen; de opnames zelf blijven ongewijzigd.
- De vaste borden (`bord=letters`, `cijfers`, `getallen`) staan bovenaan
  het script in `index.html` (`BORDEN`).
