Resume-Website

Dieses kleine statische Template ist dafür gedacht, als persönliche "Resume"-Seite genutzt zu werden und kann direkt via GitHub Pages gehostet werden.

Struktur:
- index.html — Hauptseite
- css/styles.css — Styles

Schnellstart (lokal):
1. Öffne `index.html` in deinem Browser (Doppelklick oder "Öffnen mit").

GitHub Pages veröffentlichen:
1. Erstelle ein neues Repository auf GitHub oder benutze ein bestehendes.
2. Kopiere die Dateien in das Repo (`resume-site/*`).
3. Push mit PowerShell (Beispiel):

```powershell
cd path\to\repo
git init
```markdown
# Resume-Website

Dieses kleine statische Template ist als persönliche "Resume"-Seite gedacht und lässt sich einfach über GitHub Pages hosten.

## Projektstruktur
- `index.html` — Hauptseite
- `css/styles.css` — Styling
- `assets/` — Bilder (Avatar, Logos etc.)

## Schnellstart (lokal)
1. Öffne `index.html` in deinem Browser (Doppelklick oder "Öffnen mit").
2. Ändere Inhalte in `index.html` (Name, Links, Texte).

## Deployment: GitHub Pages
1. Erstelle ein neues Repository auf GitHub (z. B. `Hope12345678.github.io`) oder nutze ein bestehendes.
2. Kopiere die Dateien in das Repo-Root oder klone das Repo lokal und kopiere die Dateien hinein.
3. Beispiel (PowerShell):

```powershell
cd path\to\repo
git init
git add .
git commit -m "Add resume site"
git branch -M main
git remote add origin https://github.com/<dein-benutzername>/<repo>.git
git push -u origin main
```

4. In GitHub: Repository → Settings → Pages: wähle Branch `main` / Ordner `/ (root)`.

GitHub Pages stellt automatisch ein HTTPS-Zertifikat aus. Wenn du eine eigene Domain verwendest (siehe unten), kann das bis zu einigen Minuten dauern.

## Custom Domain (CNAME)
- Wenn du eine eigene Domain (z. B. `lmoeller.me`) verwenden willst, lege im Projekt-Root eine Datei `CNAME` mit genau deiner Domain (eine Zeile) an oder trage die Domain in den Pages-Einstellungen ein.
- DNS-Setup beim Registrar:
	- Apex/root (`example.com`): A-Records zu GitHub Pages IPs: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`.
	- Subdomain (z. B. `www`): CNAME → `<username>.github.io`.
- Hinweis: Wenn du Cloudflare nutzt, setze die Proxy-Option vorübergehend auf "DNS only" (graue Wolke), bis GitHub das Zertifikat ausstellt.

## Assets (Bilder, Avatar)
- Lege Bilder im Ordner `assets/` ab (z. B. `assets/avatar.png`).
- Wurde ein Bild nicht angezeigt, kann es daran liegen, dass die Datei nicht committet wurde. Beispiel:

```powershell
git add assets/avatar.png
git commit -m "Add avatar asset"
git push origin main
```

- Direkter Test der URL: `https://<deine-domain>/assets/avatar.png` sollte die Datei liefern (HTTP 200).

## Theme & Personalisierung
- Schriftart: Inter (Google Fonts) ist bereits eingebunden.
- Theme toggle: Dark/Light wird per Button gesteuert und in `localStorage` gespeichert.

## Schnell-Checks / Troubleshooting
- Seite lädt nicht per HTTPS: prüfe DNS und Cloudflare-Proxy.
- Bild fehlt (404): prüfe Groß-/Kleinschreibung im Dateinamen und ob die Datei committed wurde.

## License
This project is a small personal site template — passe es frei an.

---
Änderungen/Anpassungswünsche? Öffne einfach `index.html`/`css/styles.css` und sag mir, welche Bereiche ich weiter polieren soll.
```
