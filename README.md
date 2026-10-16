# RackRNG 🖥️

Een gratis RNG-tycoon in je browser over serverhardware. Roll CPU's, RAM, storage, switches en routers, bouw je serverrack uit tot 42U, verdien geld en studeer af om je carrière op te bouwen. Electronics-ICT edition.

**▶️ Speel:** https://matsasseloos.github.io/rackrng/

Alles draait in **RackOS**, een nep-besturingssysteem: één bureaublad met je rack en roll-console, en apps die je opent als vensters (slepen, vergroten, minimaliseren). Op de gsm werkt het met een tabbalk onderaan.

## Hoe speel je?
- 🎲 **Roll** voor een willekeurig onderdeel, van Common tot Quantum, en voor wie veel geluk heeft: **Secret**. Hoe zeldzamer, hoe meer het oplevert. Zeldzame items kunnen ook overclocked zijn of een **mutatie** hebben.
- 🗄️ Zet het in je **rack**. Elke U heeft een CPU-, RAM- en storage-slot. Alle drie dezelfde tier = **Perfect match**.
- 🌐 Een **router** en **switches** versterken je hele rack.
- 📶 Upgrade je **verbinding** van 56k-modem naar glasvezel voor snellere rolls.
- ⬆️ **Upgrades**: luck, multithreading, gouden rolls, auto-roll met Hot-Swap, en nog veel meer.
- 🛍️ **RackShop**: elk vol uur 3 nieuwe boosts met een vaste prijs. Gebruik ze meteen of bewaar ze in je **gereedschapskist**. Ook rack-skins.
- 🎓 **Carrière**: verdien €1T in één run en studeer af voor ECTS. Elk diploma vraagt iets meer, en met je ECTS koop je nodes in een skill tree met 5 takken. Je rang groeit van Stagiair tot CTO.
- 🎰 **Casino** met blackjack en crash, gewoon met in-game geld.
- ⚡ **Random events**: Patch Tuesday, Black Friday, stroomuitval, ransomware, …
- 📊 **Stats** en een **catalogus** van alle items die je al vond.
- ⚙️ **Instellingen**: zet meldingen per soort uit en schakel effecten uit die je te druk vindt.

**Handig:** `spatie` = roll, `B` = koop, `E` = beste uitrusting, `1`–`9` = apps openen. Shift+klik op een upgrade koopt zoveel niveaus als je kunt betalen. Shift+klik in Opslag zet een item meteen op de beste plek. Vergrendel je beste items zodat ze nooit verkocht worden.

Je voortgang wordt lokaal in je browser bewaard. Via **Save** in het RackOS-menu maak je een back-up of speel je verder op een ander toestel.

## Technisch
- Eén bestand (`index.html`), puur HTML/CSS/JavaScript, geen frameworks of build-stap. Installeerbaar als app (PWA).
- Opslag via `localStorage`. Saves bewaren item-ID's, zodat balanswijzigingen ook voor bestaande spelers gelden.
- Alle balans (kansen, prijzen, upgrades, boosts, events, casino, carrière) staat bovenaan in het script in config-tabellen.

## Beta / testversie
Nieuwe features worden eerst getest op **/beta/**: https://matsasseloos.github.io/rackrng/beta/
- `beta/index.html` is een aparte kopie van de game met een **eigen save** (`rackrng-save-beta`), dus de echte voortgang van spelers wordt nooit aangeraakt.
- Test-tools in het RackOS-menu: geld erbij, alle upgrades max, glasvezel, random event, ECTS en diploma's erbij, en je echte save kopiëren naar de beta.
- Geen app-installatie of offline-cache in de beta, zodat je altijd de nieuwste versie ziet.

**Klaar met testen?** Zet de nieuwe code in de root-`index.html` zonder de beta-aanpassingen (`SAVE_KEY`, `UI_KEY`, `IS_BETA`, het BroadcastChannel, de test-tools, de BETA-tag, de uitgeschakelde service worker) en verhoog `VERSION` in `sw.js`.
