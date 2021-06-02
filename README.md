# Hosting

Server, ze kterého se servírují stránky uživatelům.

### Příklady

- [Netlify](https://www.netlify.com/)
- [GitHub Pages](https://pages.github.com/)
- [Heroku](https://www.heroku.com/)
- [Vercel](https://vercel.com/)
- [Endora](https://www.endora.cz/)

## Doména

Pojmenování serveru v zapamatovatelné podobě.

### DNS

Záznamy párující domény s číselnými adresami serverů. Pro czechitas by byla doména czechitas.cz a adresa, kde je web hostovaný `51.68.166.161`.

### Příklady služeb pro registraci a správu domény

- [Active24](https://www.active24.cz/)
- [Endora](https://www.endora.cz/)
- [Forpsi](https://www.forpsi.com/)
- [GoDaddy](https://uk.godaddy.com/)

## Verzování kódu

Prostor pro zálohování zdrojových souborů a jejich sdílení v týmu.

### Příklady

- [GitHub](https://github.com/)
- [GitLab](https://about.gitlab.com/)
- [Bitbucket](https://bitbucket.org/product/)

## Ukázka nastavení projektu

1. Na GitHub nahráváme zálohu zdrojových kódů, například soubory s příponou jsx, které jsou určené pro nás, pro vývojáře a pro Webpack.

1. Soubory proženeme Webpackem, který vytvoří složku s html, css, js, obrázky, která je určená pro prohlížeč. Tu dáme na hosting od Netlify.

1. Předchystaná doména končící na `.netlify.app` se nám nelíbí, a tak si na Active24 zaregistrujeme doménu jinou. Té nastavíme DNS záznamy, aby směřovaly na adresu Netlify serveru.

1. Uživatel zadá do prohlížeče naši doménu.

1. Prohlížeč se zeptá DNS, jakému serveru si má říct obsah.

1. Je odkázán na Netlify, od kterého v zápětí dostane html a další související soubory.

1. Netlify máme nastaveno tak, že pozná nový kód na GitHubu, automaticky na něj pustí Webpack a uloží si novou složku dist, kterou nově servíruje uživatelům místo staré verze. Doména už není potřeba znovu nastavovat.
