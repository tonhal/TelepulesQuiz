# Településkvíz 🇭🇺

Egyszerű, böngészőben futó webalkalmazás Magyarország összes településének megtanulásához járások szerint. Nem igényel szervert — elég az `index.html`-t megnyitni a böngészőben.

## Funkciók

- **Böngészés** — a 197 járás vármegyék szerint csoportosítva, kereshetően. Egy járásra kattintva megjelenik az összes települése. Interaktív Magyarország-térkép is megnyitható.
- **Gyakorlás** — véletlenszerűen feldobott településekhez egy interaktív járástérképen kell rákattintani a helyes járásra (segítség/vármegye nélkül, valódi tudást tesztelve). A válasz után a térkép megmutatja a helyes (zöld) és a tévesen választott (piros) járást.
- **Megtanult lista** — a már tudott települések kivehetők a gyakorlásból, és bármikor visszatehetők.
- **Statisztika** — helyes/hibás/pontosság számláló, külön nullázható.
- **Profilok** — több profil hozható létre (csak név), mindegyik külön tárolja a saját megtanult településeit és statisztikáit.

## Az adatok tárolása

A profilok, a megtanult települések és a statisztikák a böngésző **`localStorage`-ában**, az adott felhasználó saját gépén tárolódnak. Semmilyen felhasználói adat nem kerül a repóba, és nincs szerveroldali tárolás — minden kliensoldali.

## Fájlok

- `index.html` — a teljes alkalmazás (HTML + CSS + JS).
- `data.js` — a települések és járások adatai (a `telepulesek.csv`-ből generálva, irányítószám-duplikátumok kiszűrve).
- `map.js` — a járások SVG-geometriája az interaktív térképhez.
- `points.js` — a települések vetített koordinátái (a gyakorlásban a válasz után egy pont mutatja a helyüket a járáson belül).
- `telepulesek.csv` — a nyers forrásadat.
- `kozig.png` — referencia közigazgatási térkép.

## Használat

Töltsd le / klónozd a repót, és nyisd meg az `index.html`-t a böngésződben.

## Adatforrások

- Járás-határok: © OpenStreetMap közreműködők, [ODbL](https://www.openstreetmap.org/copyright) licenc alatt.
