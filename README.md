# 🍎 Andy Apples

Een 2D-slingerspel in puur HTML. Andy de gorilla zwaait door de jungle aan lianen die met physics werken, verzamelt appels en probeert zo ver mogelijk te komen.

## Spelen

Open `index.html` in een browser. Er is geen installatie, server of internetverbinding nodig: alles (graphics, geluid en physics) zit in dit ene bestand.

## Besturing

| Actie | Toetsenbord | Muis / touchscreen |
| --- | --- | --- |
| Aan een liaan blijven hangen | `Spatie` ingedrukt houden | scherm ingedrukt houden |
| Loslaten / springen | `Spatie` loslaten | loslaten |
| Snel duiken (in de lucht) | `Spatie` ingedrukt houden | scherm ingedrukt houden |
| Liaan grijpen | ingedrukt houden terwijl je een liaan raakt | idem |
| Pauze | `P` of `Esc` | ❚❚-knop |

## Features

- **Lianen met physics**: elke liaan is een Verlet-touw van segmenten. Andy's gewicht, zijn vaart, zwaaien en loslaten werken zoals je zou verwachten. Andy duwt ook lianen opzij waar hij doorheen vliegt.
- **Hoge wereld**: lianen hangen aan takken op allerlei hoogtes (zoals in Benji Bananas) en de camera beweegt mee omhoog en omlaag. Boven een bepaalde hoogte hangen geen lianen meer, alleen nog wolken. De generator zorgt dat de volgende liaan altijd bereikbaar is.
- **WOOHOO!**: Andy juicht als hij met flinke vaart van een liaan zwaait (stem gemaakt met formant-synthese, dus zonder geluidsbestanden).
- **Appels** liggen overal. Gouden appels zijn 5 appels waard.
- **Paddenstoelen** laten je hoog stuiteren.
- **Zes biomes**, die steeds iets lastiger worden:
  1. 🌿 Jungle (0 m)
  2. 🐸 Moeras (450 m): wespen
  3. 🦒 Savanne (1100 m): rotte lianen die breken
  4. ❄️ IJsbergen (1900 m): gladde ijslianen waar je vanaf glijdt, en vogels
  5. 🌋 Vulkaan (2900 m): vuurballen uit de lava
  6. 🌙 Sterrennacht (4100 m): alles door elkaar
  
  Hoe verder je komt, hoe groter de gaten tussen lianen, hoe meer vijanden en hoe minder appels.
  Bij elke nieuwe biome speelt een riedeltje en worden appels meer bananen waard: +0,5 / +1 / +1,5 / +2 / +3 🍌 per 🍎 bovenop de Bananenruil-upgrade.
- **Permanente upgrades**: na elke run worden appels en afstand omgezet in 🍌 bananen. Daarmee koop je upgrades: Lange armen, Zwaaikracht, Lanceerkracht, Appelmagneet, Bananenruil, Gouden appels, Reddingsballon, Helm en Raketstart.
- **Save-systeem**:
  - De voortgang wordt automatisch opgeslagen in de `localStorage` van de browser.
  - **Exporteren** geeft een `.json`-save-bestand; **importeren** laadt zo'n bestand weer in.
  - Er is ook een **save-code** (tekst) om te kopiëren en plakken, handig op een telefoon.
  - Saves krijgen een checksum, zodat je een waarschuwing ziet als een bestand met de hand is aangepast.
