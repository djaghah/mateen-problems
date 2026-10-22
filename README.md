# MatEN — exercise bank / banca de exerciții

Content for the **MatEN** Android app (math practice for grades 1–8, based on the Romanian school curriculum), served through the jsDelivr CDN.
Conținutul aplicației **MatEN** (exerciții de matematică pentru clasele 1–8, după programa școlară din România), servit prin CDN-ul jsDelivr.

| File | Content |
|---|---|
| `problems.json` | the canonical bank, in Romanian (also read by app versions 1.2.0 / 1.3.0 — keep this schema) |
| `i18n/bank.<lang>.json` | translation overlays per language (`en`, `fr`, `de`, `it`, `es`, `pt`, `pt-PT`), applied by id + hash of the Romanian text, only when their `rev` is newer than the one built into the app |
| `privacy-policy.html` | the privacy policy (all languages), published with GitHub Pages |

```
https://cdn.jsdelivr.net/gh/djaghah/mateen-problems@main/problems.json
https://cdn.jsdelivr.net/gh/djaghah/mateen-problems@main/i18n/bank.en.json
```

## Update (din `maten-app`, vezi `maten-app/tools/i18n/README.md`)
1. Banca românească: `problems.json` (generatoarele din `maten-app/tools`). Un exercițiu nou se publică **împreună cu traducerile lui**: `node tools/i18n/bank-units.js` → traducere → `node tools/i18n/bank-build.js <limbă>` → `node tools/i18n/bank-check.js <limbă> --all` → copiază `maten-app/i18n-work/bank/out/bank.<limbă>.json` în `i18n/`.
2. `git add . && git commit && git push` (prin SSH, ca `djaghah`).
3. Pentru actualizare imediată: `https://purge.jsdelivr.net/gh/djaghah/mateen-problems@main/<fișier>`.

Aplicația ia conținutul singură — fără republicare în Google Play. Într-o limbă ≠ română, o bancă nouă se folosește doar când există și traducerea ei (altfel rămâne banca inclusă în aplicație).
