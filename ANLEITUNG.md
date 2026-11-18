# derfranchiser.com – Online stellen mit GitHub Pages + All-Inkl

Kosten: 0 € Hosting. Zeitaufwand: ca. 30 Minuten + Wartezeit für DNS.

## Vor dem Livegang
- `impressum.html`: alle [eckigen Klammern] ersetzen. Ohne vollständiges Impressum nicht live schalten.
- `datenschutz.html`: [eckige Klammern] ersetzen (Firmendaten, Stand).
- LinkedIn-URL im Footer von `index.html`.
- Foto: als `img/kris.jpg` hochladen (Anleitung im Kommentar im Abschnitt ÜBER MICH).

## Schritt 1 – Repository anlegen
1. github.com → Konto anlegen → oben rechts **+ → New repository**.
2. Name: `derfranchiser` · Sichtbarkeit: **Public** (Pflicht im kostenlosen Plan) → **Create repository**.
3. **uploading an existing file** → den INHALT des Ordners `derfranchiser-website` hineinziehen
   (nicht den Ordner selbst – `index.html` muss oben liegen) → **Commit changes**.
   Hinweis Mac: Die Dateien `CNAME` und `.nojekyll` sind wichtig. `.nojekyll` ist im Finder unsichtbar –
   mit **Cmd + Shift + .** einblenden und mit hochladen.

## Schritt 2 – GitHub Pages einschalten
1. Im Repository: **Settings → Pages**.
2. Source: **Deploy from a branch** · Branch: **main** · Ordner: **/ (root)** → **Save**.
3. Nach 1–2 Minuten erreichbar unter `https://DEINNAME.github.io/derfranchiser/` → am Handy testen.
4. Unter **Custom domain** steht `derfranchiser.com` (kommt aus der Datei CNAME). Falls leer: eintragen → Save.

## Schritt 3 – DNS bei All-Inkl (KAS)
KAS → **Tools → DNS-Einstellungen** → bei derfranchiser.com **bearbeiten**.

1. Vorhandene **A-Einträge** für `derfranchiser.com` (ohne www) löschen bzw. ändern auf diese vier:
   - A → 185.199.108.153
   - A → 185.199.109.153
   - A → 185.199.110.153
   - A → 185.199.111.153
2. Eintrag für **www**: Typ **CNAME** → Ziel `DEINNAME.github.io.`
   (DEINNAME = dein GitHub-Benutzername; vorhandenen A-Eintrag für www vorher löschen)
3. **MX-Einträge (E-Mail) NICHT anfassen.**
4. Speichern. Wirksam meist nach 15 Min., max. 24 Std.

## Schritt 4 – HTTPS
GitHub → Settings → Pages → sobald „DNS check successful“ erscheint: **Enforce HTTPS** anhaken.
(Das Zertifikat kann bis zu 24 Std. dauern; vorher ist das Häkchen ausgegraut.)

## Pflege
Datei auf GitHub anklicken → Stift-Symbol → Text ändern → **Commit changes** → nach ca. 1 Min. live.
Fehler gemacht? Datei → **History** → alte Version wiederherstellen.
