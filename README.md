[![Merge master into all branches](https://github.com/cracky22/msg-encrypt/actions/workflows/merge-master.yml/badge.svg)](https://github.com/cracky22/msg-encrypt/actions/workflows/merge-master.yml)
# msg-encrypt (⌐■_■)

msg-encrypt ist ein Programm mitdem man Textnachrichten unleserlich verschlüsseln kann (Anwendungszweck: Whatsapp / Signal).

<!--![image](https://github.com/cracky22/msg-encrypt/assets/104385850/f8c8a57e-f479-4c40-aa5b-72b8c3b1f054)-->

# Beispiel / Example
`hi` heißt verschlüsselt ```Z0FBQUFBQm1mSmtCZ3dNVjZOZjFYZHpaUjY0OTFYRmF1dzVGQmtPQjZiRVJSMF9DSHN5YWstcWpxWWlJeVh4ZVd3eXpWWTBBaTdwMkptVnlhSWVNOUdibFNOdGZDOEJCQ3c9PQ==```

# Befehle / Commands
Folgende Commands werden aktuell unterstützt:
- `encrypt` => verschlüsselt [^1] 
- `decrypt` => entschlüsselt [^1] 
- `whitemode` / `darkmode` => aktivieren via `wm` / `dm`
- `help` => [`help encrypt` / `help decrypt`] 
- `exit` => programm verlassen [^2]
- `version` => zeigt aktuell benutzte Version
- `update` => programm schaut bei start nach automatisch updates

Hinweis: Bitte die Python-Installation von [www.python.org](https://www.python.org/downloads/) verwenden

# Entwickler / Developer
Du kannst msg-encrypt mit `python msg-encrypt.py -debug` starten um Zugriff auf das debugutil zu bekommen. Das Debugutil kann mit `debug` gestartet werden.
Im Debugmodus wird sich msg-encrypt beim bearbeiten des Source-Codes nicht selbst beenden. Des weiteren hast du Zugriff auf die reine Verschlüsselung (ohne base64-encoding), solltest du an der Android-App arbeiten. Weitere Infos unter `dev-help`. Alternativ kannst du dir die Session-Logs mit dem command `logs` anzeigen lassen.

![image](https://github.com/cracky22/msg-encrypt/assets/104385850/a65efbc7-c83f-4267-bbd1-ac9d201c56a9)

[Der Fehler: `['validate_hash']: HASH INVALID!` kann beim Entwickeln auftreten, da die Entwicklerversion nicht derselben Prüfsumme wie der des letzten Releases entspricht (durch kurzfristige Änderungen)].

# Feedback an Entwickler
Das Feedback an Entwickler erfolgt über GitHub. Insbesondere die Android-Applikation verfügt seit Version v6.1.2 über eine Feedbackmöglichkeit in der App direkt. Diese Schnittstelle ist über msgserver an GitHub Issues angebunden und ermöglicht das automatisierte Erstellen von Issues.

## Versioncontrol / Versionsnummern
Aktuelle Versions-Tags sind dev-beta (Developer-Beta), Public-Beta und Stable. Die Stable wird in Zukunft verfügbar sein. Die unterschiedlichen Builds stehen für neue Features / kleine Änderungen die noch mit in der Version getestet werden sollen. Build updates werden nicht auf meiner Webseite zur Verfügung stehen, da sie meistens nur Entwickler-Tests beinhalten. Große Versionen (releases) werden sowohl auf dem öffentlichen GitHub Account als auch auf meiner Webseite verfügbar sein.

# Datenschutz / Privacy
Wir arbeiten ständig an Verbesserungen und Fehlerkorrekturen sowie neuen Features, daher erheben wir Analysedaten um das bestmögliche aus der Software herauszuholen. Neben den Analysedaten werden Daten für statistische Zwecke sowie automatisierte Fehlerberichte an unsere Server gesendet. Alle an uns gesendeten Daten enthalten keinerlei persönliche Informationen. Möglicherweise wird in der Developer-Beta als auch in der Public-Beta vermehrt bzw umfangreicheres Logging stattfinden. Das liegt daran dass diese Versionen noch in der Beta-Phase sind. Es werden beispielsweise Daten die zur Verbesserung der Performance, Rendering Infos sowie andere Metadaten gesammelt.
Aktuell (2024-06-27) werden ab 100KB (101024B) die Logs in der Android-App an mich gesendet. Bei der Python-Version erfolgt das logischerweiße beim schließen mit `exit` des Programms. Auch in Python-Beta-Versionen kann erweitertes Logging stattfinden, besonders in public-beta Versionen.

Diese Daten werden erhoben:
- `Logs`
- `Versionsinfos + Checkesummen` 
- `Fehler` => [wird automatisch gemeldet]

Das sehen Entwickler:
Versionsinfos + Checksummen + Zeitstempel:

![image](https://github.com/cracky22/msg-encrypt/assets/104385850/7b596450-d283-4f59-9eb6-5e9c1d4e0e04)


Fehler:

![image](https://github.com/cracky22/msg-encrypt/assets/104385850/6b00cdcb-bf0d-4497-a512-4fda36b6f50a)


Logs:

![image](https://github.com/cracky22/msg-encrypt/assets/104385850/1905ffeb-4f80-4637-ab7a-9eab68f91f05)

# Cross-Platform / ARM-Unterstützung
Aktuell wird die Python-Version unterstützt von:
- Windows
- Linux
- MacOS X
- MacOS *ARM
Die Android Version läuft ab API 31 (Android 12)

# Locking / Sperrung via Admintool
Wir Entwickler verfügen über Tools mit denen wir jederzeit Programme und Nutzer einzelne als auch gesamt sperren können (bspw. bei Sicherheitsvorfällen oder Verstoßen). Wir behalten uns damit das Recht vor bei nicht ordnungsgemäßer Nutzung der Software, ihnen die Erfahrung einzuschränken! Dies zählt sowohl für die Android-App als auch die Cross-Platform Variante.

# Lizenz / License
Das Programm nutzt python3. Der Code ist für nicht Mitglieder des GitHub-Repositorys NICHT zugänglich (d.h. Kompiliertes Python). Hier sind die [Nutzungsbedingungen](https://github.com/cracky22/msg-encrypt/raw/master/kernel_v5/LICENSE.txt).

# 3rd-party zeugs (Drittanbieter)
Die Python-Version verfügt über folgende Drittanbieter Bibliotheken:
- [fernet](https://pypi.org/project/fernet/)
- [cryptography](https://pypi.org/project/cryptography/)
- [hashlib](https://pypi.org/project/hashlib/)
- [pyperclip](https://pypi.org/project/pyperclip/)
- [requests](https://pypi.org/project/requests/)

Die Android-App verfügt über folgende Drittanbieter Bibliotheken:
- [crypto.js](https://cdnjs.com/libraries/crypto-js)
- [forge.js](https://cdnjs.com/libraries/forge)
- [jquery.js](https://cdnjs.com/libraries/jquery)
- [slideunlock.js](https://www.jqueryscript.net/slider/jQuery-Plugin-To-Create-Slider-To-UnLock-Sliders-slideunlock.html)
- [purify.js](https://cdnjs.com/libraries/dompurify)

[^1]: pyperclip ist nur auf Windows und Mac verfügbar, kopieren in ubuntu via Strg+c / Strg+v bzw Rechtsklick kopieren / einfügen
[^2]: Programm bitte immer so verlassen => Protokolldateien werden erst bei `exit` übermittelt