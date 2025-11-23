# QuarantineMode

Easily get your website offline or build on your sites without letting your users see the changes!

## ❔ How to use?
Just type in this command in Github Codespaced or Visual Studio Code:

gh Cdespaces:
```
git clone https://github.com/Lokrogaming/quarantineMode.git
```
VS Code:

```
cd ~\Documents
mkdir Github Codes
cd ~\Documents\Github\Codes
git clone https://github.com/Lokrogaming/quarantineMode.git
```

## 📋 Under which circumstances may I use it?
Please paste this code in your website:

```html
<p>The <a href="https://github.com/Lokrogaming/quarantineMode">quarantineModeSystem</a> <"copied or edited"> from <a href="https://lokrogaming.github.io">Lokrogamer</a>
```
## 📂 Structure

```
📁 quarantineMode
 ┣ 📂 modules
 ┃  ┣ 📂 blocker
 ┃  ┃  ┣ 📂 JS
 ┃  ┃  ┃  ┗ 📜 jsModule.js
 ┃  ┃  ┗ 📂 JSON
 ┃  ┃     ┗ 📘 quarantineMode.json
 ┃  ┣ 📂 errorPage
 ┃  ┃  ┣ 📂 JS
 ┃  ┃  ┃  ┗ 📜 script.js
 ┃  ┃  ┗ 📂 HTML
 ┃  ┃     ┗ 🌐 index.html
 ┃  ┃
 ┃  ┣ 📂 Config
 ┃  ┃  ┗ ⚙️ config.json 
 ┃  ┗ 📂 example 
 ┃     ┗ 🌐 module.html
 ┣📄README.md
 ┗🧾 LICENSE   
```
## 🧾 How to use
After you correctly cloned the repository, open "modules => Config => Config.json". You should see this:
```json
[{
    "maintenanceRedirect":"https://lokrogaming.github.io/error?reason=maintenance&refferer=${currentPage}", //default redirection link
    "quarantineRedirect":"https://lokrogaming.github.io/error?reason=503"//default redirection link
}]
```
If you have a custom errorpage, please put the link into the placeholder.

## 📝 How to implement
**Recommendation**:
Copy and paste the code from **module.js** and paste it in the `<script></script>` section in yout HTML Code. 
Paste the code from **module.html** in the `<body></body>` section in the exact same file.

## 🎨 How to use the errorPage
The errorcode is provided through the link. 
E.g.: "https://lokrogaming.github.io/error.html?reason=[errorCode]"
You (as developer) can define errorcodes in this datasheet:
````json
// Title-Mapping
    const errorTitles = {
      "404": "Seite nicht gefunden",
      "403": "Zugriff verweigert",
      "401": "Nicht autorisiert",
      "500": "Interner Serverfehler",
      "502": "Bad Gateway",
      "503": "Service nicht verfügbar",
      "504": "Gateway Timeout",
      "timeout": "Zeitüberschreitung",
      "network": "Netzwerk-Fehler",
      "javascript_disabled": "JavaScript deaktiviert",
      "invalid_input": "Ungültige Eingabe",
      "missing_parameter": "Fehlender Parameter",
      "not_found": "Element nicht gefunden",
      "db_error": "Datenbankfehler",
      "syntax_error": "Verarbeitungsfehler",
      "unknown": "Unbekannter Fehler",
      "no_error": "Kein Fehler erkannt",
      "session_expired": "Zeitlimit erreicht",
      "rickroll": "Du wurdest gerickrolled",
      "maintenance": "Wartungsmodus"
    };

    // Subtitle-Mapping
    const errorSubtitles = {
      "404": "Die angeforderte Seite wurde nicht gefunden.",
      "403": "Bitte melde dich an oder prüfe deine Berechtigungen.",
      "401": "Bitte erneut einloggen.",
      "500": "Versuche es später erneut.",
      "502": "Der Server hat keine gültige Antwort erhalten.",
      "503": "Der Service ist derzeit nicht verfügbar.",
      "504": "Der Server hat zu lange gebraucht, um zu antworten.",
      "timeout": "Die Verbindung hat zu lange gedauert.",
      "network": "Du bist offline. Bitte überprüfe deine Internetverbindung.",
      "javascript_disabled": "Bitte aktiviere JavaScript, um die Seite zu nutzen.",
      "invalid_input": "Die eingegebenen Daten sind ungültig.",
      "missing_parameter": "Ein erforderlicher Parameter fehlt.",
      "not_found": "Das angeforderte Element existiert nicht.",
      "db_error": "Fehler bei der Datenbankverbindung.",
      "syntax_error": "Es gab einen Fehler in der Verarbeitung der Anfrage.",
      "unknown": "Ein unbekannter Fehler ist aufgetreten.",
      "no_error": "Alles funktioniert einwandfrei ✅",
      "session_expired": "Du wurdest getrennt um Bandbreite zu sparen und inaktive Nutzer zu reinigen. Bitte öffne die Seite erneut",
      "rickroll": "Du wurdest soeben Opfer eines Streiches! Aber wait... Ist es wirklich April?",
      "maintenance": "Die Seite befindet sich in der Wartung"
    };
```
