# MateEN — Banca de probleme

Conținutul (problemele) pentru aplicația **MateEN** — pregătire pentru Evaluarea Națională la matematică.

Fișierul `problems.json` este servit către aplicație prin CDN (jsDelivr):

```
https://cdn.jsdelivr.net/gh/djaghah/mateen-problems@main/problems.json
```

## Cum adaug probleme noi
1. Editez `problems.json` (adaug probleme în `types[].problems[]`).
2. `git add . && git commit -m "adaug probleme" && git push`
3. (opțional, pentru update instant) deschid o dată în browser:
   `https://purge.jsdelivr.net/gh/djaghah/mateen-problems@main/problems.json`

Aplicația ia conținutul automat — **fără republish pe Google Play**.

## Structură
- `chapters[]` — capitole (ex. „III · 3.1")
- `types[]` — tipuri de probleme (ex. „Apartamente cu 3 și 5 camere")
- `problems[]` — enunț, `inputs` (cu `answer`), `hints`, `solution`
