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
git add .
git commit -m "Add resume site"
git branch -M main
git remote add origin https://github.com/<dein-benutzername>/<repo>.git
git push -u origin main
```

4. Aktiviere GitHub Pages in den Repo-Einstellungen: Branch `main` / `root`.

Personalisierung: Ersetze die Platzhalter in `index.html` (Name, Links, Texte) und passe `css/styles.css` an.
