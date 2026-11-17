# Els apunts de català

Web de Llengua i literatura catalana de Batxillerat: apunts, esquemes, resums i trucs per als alumnes.

Web senzill fet només amb HTML i CSS. No cal instal·lar res: obre `index.html` amb el navegador per veure'l.

## Què hi ha a la carpeta

| Fitxer / carpeta | Per a què serveix |
|---|---|
| `index.html` | Pàgina d'inici amb els 4 blocs i la llista de temes |
| `estil.css` | Colors, fonts i disseny de tot el web (no cal tocar-lo) |
| `temes/` | Una pàgina per a cada tema, amb el nom `tema-NÚMERO.html` (ara hi ha `tema-17.html`) |
| `materials/` | Aquí hi deses els PDF |

Per editar els fitxers n'hi ha prou amb el Bloc de notes, tot i que és més còmode un editor gratuït com [Visual Studio Code](https://code.visualstudio.com/).

## Afegir un material a un tema

Obre la pàgina del tema (per exemple `temes/tema-17.html`). Dins hi ha un comentari amb un bloc `<li> … </li>` a punt per copiar. Enganxa'l dins de la llista `<ul class="materials">` de l'apartat que vulguis (Apunts, Esquemes i resums, Trucs per no equivocar-te o Per practicar), esborra la línia «Aviat hi trobaràs…» d'aquell apartat i canvia'n:

1. **L'adreça** (`href="..."`):
   - PDF: desa'l a `materials/` i escriu `href="../materials/nom-del-fitxer.pdf"`
   - Enllaç o document de Google: enganxa l'adreça completa, `href="https://..."`
2. **El tipus**: `PDF`, `Enllaç`, `Google`, `Vídeo`…
3. **El títol** i, si vols, la nota de sota.

> Consell: posa noms de fitxer sense espais, accents ni majúscules (`tema-1-apunts.pdf`).
>
> Documents de Google: al botó **Comparteix**, tria «Qualsevol persona amb l'enllaç» perquè l'alumnat el pugui obrir.

## Crear una pàgina de tema nova

1. Dins de `temes/`, copia `tema-17.html` i canvia-li el nom amb el número del tema (per exemple `tema-3.html`).
2. Obre-la i canvia el títol (`<title>`, que acaba sempre amb «· Els apunts de català», i `<h1>`), la línia «Tema 17 · …», la descripció, la línia «Inici / …» i els materials.
3. Etiqueta PAU: si el tema no és de PAU, esborra `<span class="pau">Contingut PAU</span>`.
4. Canvia la classe del `<body>` segons el bloc, perquè agafi el color correcte:
   - `bloc-llengues` — Llengües i parlants (temes 1–5)
   - `bloc-comunicacio` — Comunicació (temes 6–8)
   - `bloc-literaria` — Educació literària (temes 9–14)
   - `bloc-reflexio` — Reflexió sobre la llengua (temes 15–20)
5. A `index.html`, busca el tema a la llista del bloc i converteix-lo en enllaç. Per exemple, per al tema 3 canvia
   `<div class="tema">` per `<a class="tema" href="temes/tema-3.html">`, i el `</div>` del final de la mateixa línia per `</a>`.

Els temes que encara no tenen pàgina surten en gris amb la paraula «Aviat».

## Publicar-lo gratis a GitHub Pages

1. Crea un compte a [github.com](https://github.com).
2. Botó **New repository**. Posa-li un nom (per exemple `catala-batxillerat`), marca'l com a **Public** i crea'l.
3. Al repositori, clica **Add file → Upload files** i arrossega-hi **tot el contingut** d'aquesta carpeta (`index.html`, `estil.css`, i les carpetes `temes` i `materials`). Clica **Commit changes**.
4. Ves a **Settings → Pages**. A «Branch», tria `main` i la carpeta `/ (root)`, i desa.
5. En un parell de minuts el web serà a `https://el-teu-usuari.github.io/catala-batxillerat/`

Per actualitzar-lo més endavant, torna a fer **Add file → Upload files** amb els fitxers modificats o nous: substitueixen els antics.
