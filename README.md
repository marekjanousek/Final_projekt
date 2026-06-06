# Assassin's Creed III web

Komplexní prezentační web na téma Assassin's Creed III vytvořený pomocí čistých webových technologií.

**Živý web:** po nasazení na GitHub Pages použij odkaz ve tvaru `https://<github-username>.github.io/<repo-name>/`

## Použité technologie

- HTML5
- CSS3
- Vanilla JavaScript (ES6)
- Google Fonts (`Rajdhani`)
- Visual Studio Code (doporučeno)

## Adresářová struktura

```text
README.md
robots.txt
sitemap.xml
css/
  style.css
js/
  main.js
img/
  ac3.jpg
  ConnorKenway.jpg
  HaythamKenway.jpg
index.html
historie.html
postavy.html
gameplay.html
dokumentace.html
.gitignore
```

## Technický rozbor

### 1) Výkon

Teoreticky:
- Minimalizace HTTP požadavků redukuje počet souborů, které musí prohlížeč načíst.
- `loading="lazy"` odkládá načítání obrázků mimo obrazovku, čímž se zkracuje počáteční doba vykreslení.

Kód:
```html
<img src="img/ConnorKenway.jpg" alt="Connor Kenway" loading="lazy">
```
Vysvětlení: obrázek se načte až tehdy, když je v zorném poli, což zlepšuje výkon stránky.

### 2) SEO

Teoreticky:
- Meta tagy pomáhají vyhledávačům pochopit obsah stránky.
- `sitemap.xml` ukazuje strukturu webu vyhledávačům.
- `robots.txt` definuje, že web může být indexován.

Kód:
```html
<meta name="description" content="Komplexní web o Assassin's Creed III">
<meta property="og:title" content="Assassin's Creed III web">
<meta property="og:description" content="Komplexní web o Assassin's Creed III">
```
Vysvětlení: tyto tagy zlepšují zobrazení ve výsledcích vyhledávání a při sdílení na sociálních sítích.

### 3) Přístupnost

Teoreticky:
- Sémantické HTML (`header`, `nav`, `main`, `section`) pomáhá čtečkám obrazovky.
- Atributy ARIA zlepšují orientaci v navigaci.
- `alt` text je důležitý pro nevidomé uživatele.

Kód:
```html
<nav role="navigation" aria-label="Hlavní navigace">
  <a href="index.html">Domů</a>
  ...
</nav>
```
Vysvětlení: čtečky obrazovky umí rozpoznat hlavní navigaci a lépe ji popsat uživatelům.

### 4) Sociální sítě

Teoreticky:
- Open Graph a Twitter Card tagy řídí náhledy při sdílení odkazu.

Kód:
```html
<meta property="og:image" content="img/ac3.jpg">
<meta name="twitter:card" content="summary_large_image">
```
Vysvětlení: Facebook, LinkedIn a X zobrazí titul, popis a obrázek podle těchto tagů.

### 5) UI/UX

Teoreticky:
- Responzivní design umožňuje dobré zobrazení na mobilu i desktopu.
- Intuitivní navigace vedle sebe udržuje možnosti přehledné.

Kód:
```css
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 20px;
}
```
Vysvětlení: tato mřížka umožňuje automatické rozložení karet podle šířky obrazovky.

### 6) AI Integrace

- AI pomáhá s kontrolou cesty k souborům, návrhem dokumentace a vysvětlením technických kroků.

Kód:
```html
<!-- AI pomohla vytvořit optimalizaci -->
```
Vysvětlení: AI asistence byla použita jako podpora při návrhu struktury webu a technických poznámek.

## AI deník

Použité promptové příkazy a výsledky:

Prompt: „zkontroluj mi cesty v projektu a oprav odkazy na CSS/obrázky“
Výsledek: identifikoval/a chyby v relativních cestách a navrhl/a opravy pro funkční zobrazení.

Prompt: „přidej SEO a sociální meta tagy do všech stránek“
Výsledek: doplněny Open Graph, Twitter Cards a robots.txt bez změny vzhledu.

Prompt: „přidej přístupnost a ARIA atributy“
Výsledek: v menu a hlavním obsahu přidán popis role a lepší orientace pro čtečky obrazovky.

Prompt: „přidej komentáře ke kódu“
Výsledek: byly přidány komentáře ke kódu pro lepší porozumění.

Prompt: „připrav projekt pro GitHub Pages“
Výsledek: přesun HTML souborů do kořene, aktualizace cest a přidané .gitignore.

Tato AI asistence zrychlila kontrolu projektu, eliminovala chyby v cestách a doplnila vysvětlující dokumentaci.

## Instalace a spuštění

1. Otevřete složku `projekt` ve Visual Studio Code.
2. Doporučeno: nainstalovat rozšíření Live Server.
3. Spusťte `index.html` pomocí Live Server nebo otevřete soubor v prohlížeči.

Alternativně:
- Otevřete `projekt/html/index.html` přímo ve svém prohlížeči.
