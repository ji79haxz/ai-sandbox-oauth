# AI Sandbox OAuth

Dieses öffentliche GitHub-Repository enthält die **Informationsseiten für die Google-OAuth-Anwendung „ai-sandbox rclone“**. Die Anwendung verbindet mithilfe von [rclone](https://rclone.org/) Google Drive mit meiner privaten Linux-Umgebung (AI-Sandbox).

## Warum gibt es dieses Repository?

Google verlangt für die Veröffentlichung einer externen OAuth-Anwendung eine **öffentliche Homepage und Datenschutzerklärung**. Hier liegen nur diese Informationen. Die Dateien aus Google Drive, OAuth-Tokens und die eigentliche rclone-Konfiguration befinden sich **nicht** hier.

Das Repository ist bewusst von meiner privaten Wissensbasis und dem Google-Drive-Ordner `AI Data Storage` getrennt.

## Dateien

| Datei | Bedeutung |
| --- | --- |
| [docs/index.md](docs/index.md) | Öffentliche Beschreibung der Anwendung |
| [docs/privacy.md](docs/privacy.md) | Datenschutzerklärung zum Google-Drive-Zugriff |
| [docs/_config.yml](docs/_config.yml) | Einfaches Layout für GitHub Pages |
| README.md | Diese verständliche Einrichtungsanleitung |

## 1. GitHub Pages einschalten

1. Im Repository **Settings → Pages** öffnen.
2. Unter **Build and deployment → Source**: **Deploy from a branch** wählen.
3. Branch **main** und Ordner **/docs** auswählen und auf **Save** tippen.
4. Warten, bis die Veröffentlichung fertig ist, und die Seiten **ohne GitHub-Anmeldung** testen.

Nach erfolgreicher Veröffentlichung sind das die erwarteten URLs:

- **Homepage:** https://ji79haxz.github.io/ai-sandbox-oauth/
- **Datenschutzerklärung:** https://ji79haxz.github.io/ai-sandbox-oauth/privacy.html

Wichtig: Diese Adressen funktionieren erst, wenn GitHub Pages aktiviert und der Build erfolgreich ist.

## 2. In Google Cloud Console eintragen

Im richtigen Google-Projekt unter **Google Auth Platform → Branding**:

- **Application home page:** `https://ji79haxz.github.io/ai-sandbox-oauth/`
- **Application privacy policy link:** `https://ji79haxz.github.io/ai-sandbox-oauth/privacy.html`
- **Authorized domains:** den passenden Domainanteil nach Googles Formular hinzufügen. Wenn Google einen Eigentumsnachweis verlangt, ist eine separate Verifizierung erforderlich; GitHub Pages garantiert diesen Nachweis nicht.

Einstellungen speichern. Unter **Audience** prüfen, ob **Publish app** jetzt aktiv ist, und den Status gegebenenfalls auf **In production** stellen. Damit entfällt normalerweise die im Testmodus geltende siebentägige Ablaufbegrenzung der Autorisierung. Eine von Google gegebenenfalls verlangte App-Verifikation ist davon zu unterscheiden.

**Wichtig:** Das Veröffentlichen der OAuth-App macht keine Drive-Dateien öffentlich.

## 3. Sicherheit und Betrieb

- Die GitHub-Pages-Seiten sind **öffentlich**, aber rein informativ.
- Dort dürfen **niemals** Zugangsdaten, OAuth-Tokens, die Datei `rclone.conf`, Google-Drive-Inhalte oder private Logs gespeichert werden.
- Die rclone-Verbindung und deren Credentials bleiben auf der AI-Sandbox.
- Die Option `root_folder_id` begrenzt den angezeigten Ordnerbaum, aber **nicht** die tatsächlichen Google-OAuth-Rechte.
- Der Dateizugriff für den Benutzer `codex` wird unabhängig vom OAuth-Projekt über Linux-Rechte gesteuert.

## Änderungen

Wenn sich Zweck oder Google-Drive-Berechtigungen ändern, die zwei öffentlichen Seiten aktualisieren. Die Website verwendet keine eigene Datenbank, keine dynamische Anmeldung und keine externen Analyse-Skripte.

Quellen: [rclone – Google Drive](https://rclone.org/drive/) · [GitHub Pages – Veröffentlichungsquelle konfigurieren](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)

*Privates, unabhängiges Projekt; keine offizielle Verbindung zu Google, GitHub oder rclone.*
