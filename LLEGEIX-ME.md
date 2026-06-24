# Tasques · App instal·lable

App de tasques per veu, **local i sense núvol**. Funciona sense connexió i es pot instal·lar a l'iPhone i a Windows. Cap dada surt del dispositiu.

## Per què cal penjar-la a una URL
Perquè sigui instal·lable i funcioni offline, els fitxers han d'estar servits per **HTTPS**. No n'hi ha prou amb obrir el fitxer directament. Tens dues opcions gratuïtes (2 minuts):

### Opció A — Netlify Drop (la més ràpida, sense compte)
1. Ves a https://app.netlify.com/drop
2. Arrossega-hi **tota la carpeta** (els 7 fitxers junts).
3. Et dona una URL `https://...netlify.app`. Aquesta és la teva app.

### Opció B — GitHub Pages
1. Crea un repositori, puja-hi els 7 fitxers.
2. Settings → Pages → Branch `main` / arrel → Save.
3. La URL apareix al cap d'un minut.

> Si tens un servidor intern a Caldea, també hi pots deixar la carpeta i obrir-la per HTTPS.

## Instal·lar-la

**iPhone (Safari):** obre la URL → botó Compartir → **«Afegeix a la pantalla d'inici»**. Queda com una app amb icona pròpia.

**Windows 11 (Chrome o Edge):** obre la URL → icona d'instal·lar a la barra d'adreces (o menú ⋮ → «Instal·la Tasques»). Queda com una app a l'escriptori i al menú d'inici.

## Recordatoris

A la campana (capçalera) actives un **avís diari** a l'hora que triïs, amb el resum de tasques d'avui i endarrerides. «Prova ara» el dispara a l'instant.

Què és realista, sense amagar-ho:
- **Windows (Chrome/Edge):** l'avís diari salta encara que tinguis l'app tancada (mentre l'ordinador i el navegador estiguin engegats).
- **iPhone:** les notificacions web només funcionen amb l'app **instal·lada** a la pantalla d'inici. L'avís programat en segon pla **no** és fiable a iOS sense un servidor de push; el que sí funciona sempre és el resum en obrir l'app i els avisos mentre la tens oberta. La pantalla «Avui» ja és el teu resum diari en obrir-la.

Si en algun moment vols recordatoris push 100% fiables a l'iPhone amb l'app tancada, això requereix un petit servidor (web-push). Es pot fer, però trencaria el model "res al núvol"; ho valorem si et compensa.

## Còpia de seguretat (exporta / importa)

Com que les dades viuen al dispositiu, convé tenir-ne còpia. A la icona de fletxa (capçalera):
- **Exporta** descarrega un fitxer `tasques-backup-AAAA-MM-DD.json` amb totes les tasques.
- **Importa** el torna a carregar. Pots **substituir-ho tot** (restaurar una còpia) o **afegir** (combinar dades de dos dispositius sense duplicar).

És també la manera de passar les tasques del despatx a l'iPhone i a l'inrevés: exporta en un, comparteix el fitxer, importa a l'altre.

## Fitxers del paquet
- `index.html` — l'app
- `manifest.webmanifest` — definició de l'app instal·lable
- `sw.js` — service worker (offline + notificacions)
- `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`, `icon-180.png` — icones

Tots han d'anar junts a la mateixa carpeta.
