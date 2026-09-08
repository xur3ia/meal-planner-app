# Meal Planner – GitHub Pages / PWA

Diese Version ist für GitHub Pages und iPhone/Safari vorbereitet.

## Enthaltene Dateien

```text
meal-planner/
├── index.html
├── manifest.json
├── sw.js
├── .nojekyll
└── icons/
    ├── apple-touch-icon.png   # 180×180, iPhone/iPad
    ├── icon-192.png          # PWA
    ├── icon-512.png          # PWA
    └── icon-maskable-512.png # Android/PWA maskable
```

## Auf GitHub veröffentlichen

1. Auf GitHub ein neues Repository erstellen, z. B. `meal-planner`.
2. Alle Dateien und den Ordner `icons` **genau in dieser Struktur** hochladen.
3. Repository öffnen: **Settings → Pages**.
4. Unter **Build and deployment** bei Source **Deploy from a branch** wählen.
5. Branch **main** und Ordner **/(root)** auswählen und speichern.
6. Nach kurzer Zeit zeigt GitHub die öffentliche HTTPS-Adresse an, typischerweise:
   `https://DEIN-NAME.github.io/meal-planner/`

Die relativen Pfade in dieser Version funktionieren auch bei einer GitHub-Project-Page unter `/meal-planner/`.

## Auf dem iPhone installieren

1. Die GitHub-Pages-Adresse in **Safari** öffnen.
2. Einmal vollständig laden, damit der Service Worker die App-Dateien cachen kann.
3. In Safari auf **Teilen** tippen.
4. **Zum Home-Bildschirm** wählen.
5. Als Name z. B. `Meal Planner` verwenden und hinzufügen.

Danach startet die App vom Home-Bildschirm im Standalone-Modus. Nach dem ersten erfolgreichen Laden kann die App-Shell auch offline geöffnet werden.

## Wichtig zu den Daten

Profile, Rezepte und Wochenplan werden weiterhin nur über `localStorage` auf dem jeweiligen Gerät gespeichert. GitHub speichert diese Daten nicht. Daten auf PC und iPhone werden daher nicht synchronisiert.

## Änderungen veröffentlichen

Wenn du später `index.html`, `manifest.json` oder `sw.js` änderst, lade die neuen Dateien in dasselbe Repository hoch. Bei größeren PWA-Änderungen sollte zusätzlich die Cache-Version in `sw.js` erhöht werden, z. B. von `meal-planner-v2` auf `meal-planner-v3`.
