<p align="center">
  <img src="assets/logo-wordmark.svg" alt="Grootboek" width="420">
</p>

<p align="center">
  Een persoonlijke vermogenstracker die als app op je iPhone werkt.<br>
  Geen server, geen account — je gegevens blijven van jou.
</p>

---

## Wat is dit?

**Grootboek** is een lichtgewicht webapp om je vermogen bij te houden: de verdeling
tussen cashposities en beleggingen, hoe dat zich over tijd ontwikkelt, en groei­
percentages per periode. Alles in één statisch HTML-bestand, te openen in elke
browser en te installeren op je iPhone-startscherm als een "echte" app.

## Functies

- 📊 **Dashboard** — totaal vermogen met verdeling cash vs. beleggingen, in € en %
- 🕰️ **Tijdreizen** — spring naar elk eerder vastgelegd moment via de ledger-tijdlijn
- ✏️ **Achteraf aanpassen** — bewerk elke historische invoer, ook met terugwerkende kracht
- 📈 **Groeigrafiek** — hoe je vermogen groeit of krimpt over de volledige tijdlijn
- 📅 **Periodevergelijking** — groei over 1M / 3M / 6M / YTD / 1J / all-time, zowel
  voor je totale vermogen als los per cash en beleggingen
- 💾 **Persistente opslag** — invoer blijft bewaard tussen sessies

## Aan de slag

### Optie 1 — direct openen
Open `index.html` in Safari op je iPhone (bijv. via iCloud Drive, AirDrop, of gehost
op GitHub Pages — zie hieronder).

### Optie 2 — als app op je startscherm zetten
1. Open `index.html` in **Safari** op je iPhone
2. Tik op het **Deel-icoon** onderin
3. Kies **"Zet op beginscherm"**
4. Klaar — je hebt nu een app-icoon dat volledig los van de browserbalk werkt

### Optie 3 — automatisch hosten via GitHub Pages (aanbevolen)
Deze repo bevat al een GitHub Actions-workflow die alles automatisch regelt.

1. Zet deze repository op GitHub (als je 'm nog niet gepusht hebt)
2. Ga naar **Settings → Pages**
3. Zet **Source** op **"GitHub Actions"**
4. Push een commit naar `main` (of run de workflow handmatig via **Actions → Deploy naar GitHub Pages → Run workflow**)
5. Na een halve minuut staat je app live op `https://<gebruikersnaam>.github.io/<repo-naam>/`
6. Open die URL in Safari op je iPhone en zet 'm via **Deel → Zet op beginscherm**

Elke keer dat je naar `main` pusht, wordt de site automatisch opnieuw gepubliceerd.

## Projectstructuur

```
grootboek/
├── index.html          # de volledige app (HTML/CSS/JS in één bestand)
├── manifest.json        # web app manifest voor het homescreen-icoon
├── .github/
│   └── workflows/
│       └── deploy.yml    # automatische deploy naar GitHub Pages
├── assets/
│   ├── logo.svg          # app-icoon (vector)
│   ├── logo-wordmark.svg # logo met tekst, voor README/branding
│   ├── apple-touch-icon.png
│   ├── icon-192.png
│   └── icon-512.png
├── LICENSE
└── README.md
```

## Techniek

- Puur **HTML, CSS en vanilla JavaScript** — geen build-stap nodig
- [Chart.js](https://www.chartjs.org/) voor de donut- en lijngrafiek (via CDN)
- Data wordt lokaal per gebruiker persistent opgeslagen (geen externe database)
- Typografie: [Inter](https://fonts.google.com/specimen/Inter) en
  [IBM Plex Mono](https://fonts.google.com/specimen/IBM+Plex+Mono)

## Eigen categorieën

Standaard staan er een aantal cash- en beleggingsrekeningen klaar. Je kunt
rekeningen hernoemen, toevoegen of verwijderen via het invoerpaneel onderin de app
— er hoeft niets in de code aangepast te worden.

## Licentie

Dit project valt onder de [MIT-licentie](LICENSE) — vrij te gebruiken en aan te passen.
