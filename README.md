# RackRNG 🖥️

Een gratis RNG-browsergame over serverhardware. Roll CPU's, RAM, storage, switches en routers, bouw je serverrack uit tot 42U en verdien geld. Electronics-ICT edition.

**▶️ Speel:** https://JOUW-GEBRUIKERSNAAM.github.io/rackrng/

## Hoe speel je?
- 🎲 **Roll** voor een willekeurig onderdeel, van Common tot Quantum. Hoe zeldzamer, hoe meer het oplevert.
- 🗄️ Zet het in je **rack**. Elke U heeft een CPU-, RAM- en storage-slot. Alle drie dezelfde tier = **Perfect match ×2**.
- 🌐 Een **router** en **switches** versterken je hele rack.
- 📶 Upgrade je **verbinding** van 56k-modem naar glasvezel voor snellere rolls.
- 🛒 Koop **upgrades** (luck, multithreading, gouden rolls, …) en **rack-skins** in de shop.
- ⚡ De **boost-shop** krijgt elk vol uur nieuwe voorraad: tijdelijke boosts zoals Energiedrank (luck) of Bug bounty (inkomen), van Common tot Quantum.
- 🎰 Waag je kans in het **casino** (blackjack en crash). Gewoon met in-game geld.
- ⚡ Hou de **random events** in de gaten: Patch Tuesday, Black Friday, stroomuitval, ransomware, …

Je voortgang wordt lokaal in je browser bewaard. Met de **Save**-knop maak je een back-up of speel je verder op een ander toestel.

## Technisch
- Eén bestand (`index.html`), puur HTML/CSS/JavaScript, geen frameworks of build-stap.
- Opslag via `localStorage`, saves bewaren item-ID's zodat balanswijzigingen ook voor bestaande spelers gelden.
- Alle balans (kansen, prijzen, upgrades, events, casino) staat bovenaan in het script in config-tabellen.

## Beta / testversie
Nieuwe features eerst testen op **/beta/** (bv. `https://matsasseloos.github.io/rackrng/beta/`).
- `beta/index.html` is een aparte kopie van de game met een **eigen save** (`rackrng-save-beta`): de echte voortgang van spelers wordt nooit aangeraakt.
- 🧪-knop met test-tools: geld erbij, alle upgrades max, glasvezel, random event, je echte save kopiëren naar de beta.
- Geen app-installatie/offline-cache in de beta, zodat je altijd de nieuwste versie ziet.

**Klaar met testen?** Zet de nieuwe code in de root-`index.html` (zonder de beta-aanpassingen: `SAVE_KEY`, `IS_BETA`, het 🧪-paneel, de BETA-tag) en verhoog `VERSION` in `sw.js`.
