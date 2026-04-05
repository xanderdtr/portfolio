# Portfolio Website

Moderne single-page portfolio van Xander, gebouwd met een onderhoudbare structuur en duidelijke scheiding tussen content, styling en gedrag.

## Structuur

```text
.
├── CNAME
├── htaccess
├── index.html
├── README.md
└── assets/
		├── css/
		│   └── style.css
		└── js/
				└── main.js
```

## Architectuur

- `index.html`
	- Semantische layout met secties: Home, Over Mij, Skills, Projecten, Contact
	- Toegankelijke navigatie met skip-link en duidelijke landmarks
- `assets/css/style.css`
	- Design tokens via CSS variabelen (`:root`)
	- Responsieve layout, herbruikbare component classes, animatie states
- `assets/js/main.js`
	- Gedragslaag voor navigatie, actieve sectie, reveal animaties, skills progress en contactformulier
	- Centraal `portfolioProfile` object voor naam, e-mail, LinkedIn, GitHub, locatie en CV-link
	- Motion laag met staged hero-intro, scroll reveal stagger en subtiele hero parallax

## Onderhoud Tips

- Kleuren, radius, schaduwen en spacing pas je centraal aan in `:root` variabelen.
- Nieuwe sectie toevoegen:
	1. Voeg een nieuwe `<section id="...">` toe in `index.html`
	2. Voeg een nav-link toe die verwijst naar hetzelfde id
	3. Gebruik bestaande utility/component classes om stijl consistent te houden
- Contactgegevens en projectteksten staan op 1 plek in `index.html` en zijn daardoor snel aanpasbaar.
- Persoonlijke gegevens (naam, links, e-mail, CV) beheer je centraal in `assets/js/main.js` in `portfolioProfile`.

## Lokale Preview

Open `index.html` direct in de browser of gebruik een simpele static server (bijv. VS Code Live Server).
