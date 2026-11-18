# claude-meta

Claude programėlė Meta Ray-Ban Display akiniams (Web App, vienas `index.html`, be priklausomybių).

Klausimą parašai ranka su Neural Band (arba padiktuoji), atsakymas rodomas ekrane.

## Kaip įsidėti

1. Susikurk API raktą: https://console.anthropic.com → API keys. Tai atskira nuo Claude prenumeratos, mokama pagal naudojimą.
2. Rekomenduojama: raktui skirk atskirą workspace su mažu mėnesio limitu (pvz. 5 USD).
3. Meta AI programėlėje: Settings → App connections → Developer mode apps → pridėk URL:

   ```
   https://puse05etato.github.io/claude-meta/?key=sk-ant-TAVO-RAKTAS
   ```

4. Akiniuose atidaryk programėlę, nusitaikyk į lauką „Ask Claude…", suspausk pirštus ir rašyk.

Be `?key=` programėlė veikia kaip teksto įvedimo testas: parodo, ką parašei.

## Valdymas

- **Ask Claude… / Send**: klausimas. Po rašymo skydelio patvirtinimo išsiunčiama automatiškai, jei ne, spausk Send.
- **▲ ▼**: atsakymo slinkimas.
- **New**: naujas pokalbis (išvalo kontekstą).
- **Model**: Haiku → Sonnet → Opus. Galima ir per URL: `&model=sonnet` arba pilnas modelio ID.

## Saugumas

- Raktas saugomas tik akinių naršyklės `localStorage` ir siunčiamas tiesiai į `api.anthropic.com`. Šiame repo rakto nėra ir neturi būti.
- Raktas yra URL dalis, todėl jį mato Meta AI programėlė, kurioje URL įrašytas. Dėl to naudok atskirą raktą su limitu ir, jei kas, jį atšauk konsolėje.
- Kad veiktų nemokamas GitHub Pages, repo turi būti viešas.

## Keitimas

Viskas yra `index.html`. Sistemos instrukcija (atsakymų ilgis, kalba) yra kintamajame `SYSTEM`, modelių sąrašas `MODELS`.
