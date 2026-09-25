# 🍎 Andy Apples

Een 2D-slingerspel in puur HTML. Andy de gorilla zwaait door de jungle aan lianen die met physics werken, verzamelt appels en probeert zo ver mogelijk te komen.

## Spelen

Open `index.html` in een browser. Er is geen installatie, server of internetverbinding nodig: alles (graphics, geluid en physics) zit in dit ene bestand.

## Besturing

| Actie | Toetsenbord | Muis / touchscreen |
| --- | --- | --- |
| Aan een liaan blijven hangen | `Spatie` ingedrukt houden | scherm ingedrukt houden |
| Loslaten / springen | `Spatie` loslaten | loslaten |
| Duiken (in de lucht, begint rustig en versnelt) | `Spatie` ingedrukt houden | scherm ingedrukt houden |
| Liaan grijpen | ingedrukt houden terwijl je een liaan raakt | idem |
| Pauze | `P` of `Esc` | ❚❚-knop |

## Features

- **Lianen met physics**: elke liaan is een Verlet-touw van segmenten dat schuin naar linksonder hangt (zoals in Benji Bananas), zodat je hem makkelijk grijpt. Andy's gewicht, vaart, zwaaien en loslaten werken zoals je zou verwachten.
- **Lianen overal**: in elke kolom hangen lianen over de hele hoogte van de wereld, aan takjes. Boven het plafond hangen geen lianen meer: daar vliegen alleen vogels langs en drijft af en toe een **luchtballon** met een liaan eronder (+5 🍎).
- **Speciale lianen**: ✨ turbo (extra vaart), 🎀 elastiek (rekt en veert), 🍎 fruitliaan (vol appels), 🪵 rot (breekt na even hangen), 🧊 ijs (je glijdt omlaag).
- **Snel en belonend**: een extra krachtige eerste sprong, combo's als je snel appels pakt, bonussen voor mooie sprongen, mijlpalen elke 100 m met confetti, en een **WOOHOO!** als je van een liaan zwaait.
- **Alleen vallen is game over**: wespen, eksters en vuurballen stelen appels (die je terug kunt pakken), maar laten Andy nooit vallen. Een helm beschermt je appels.
- **Zes biomes**, die steeds iets lastiger worden:
  1. 🌿 Jungle (0 m)
  2. 🐸 Moeras (450 m): wespen, rotte lianen
  3. 🦒 Savanne (1100 m): meer rotte en elastieken lianen
  4. ❄️ IJsbergen (1900 m): gladde ijslianen en eksters
  5. 🌋 Vulkaan (2900 m): vuurballen uit de lava
  6. 🌙 Sterrennacht (4100 m): alles door elkaar

  Hoe verder je komt, hoe meer gaten tussen de lianen, hoe meer vijanden en hoe minder appels.
  Bij elke nieuwe biome speelt een riedeltje en tellen appels voor meer: +0,5 / +1 / +1,5 / +2 / +3 per appel, bovenop de Appeloogst-upgrade.
- **Levendige wereld**: meerdere parallaxlagen (bergen, heuvels, boomlijn, gedetailleerde bomen, reuzenstammen, voorgrond), een zon met stralen, wolken, noorderlicht en sterren, en daarnaast vogelzwermen, vlinders, papegaaien, giraffen, springende vissen en vallende sterren.
- **Muziek en geluid**: een procedurele jungle-groove (marimba, conga's, shaker, bas) met een eigen toonsoort per biome. Muziek en geluid staan los van elkaar aan/uit.
- **Permanente upgrades**, betaald met 🍎 appels: Lange armen, Zwaaikracht, Lanceerkracht, Appelmagneet, Appeloogst, Gouden appels, Reddingsballon, Helm en Raketstart.
- **Save-systeem**:
  - De voortgang wordt automatisch opgeslagen in de `localStorage` van de browser.
  - **Exporteren** geeft een `.json`-save-bestand; **importeren** laadt zo'n bestand weer in.
  - Er is ook een **save-code** (tekst) om te kopiëren en plakken, handig op een telefoon.
  - Saves krijgen een checksum, zodat je een waarschuwing ziet als een bestand met de hand is aangepast.
  - Oude saves met bananen worden automatisch omgezet naar appels.
