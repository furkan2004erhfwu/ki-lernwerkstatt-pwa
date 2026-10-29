# KI-Lernwerkstatt

Eine installierbare Lern-App für BWL und künstliche Intelligenz. Sie verbindet einen Karteikarten-Trainer mit einem einfachen Kostenrechner und persönlichen Lernnotizen.

**[KI-Lernwerkstatt öffnen](https://furkan2004erhfwu.github.io/ki-lernwerkstatt-pwa/)**

## Funktionen

- Zehn Karteikarten zu KI-Grundlagen und BWL, ergänzt durch eigene Karten und einen Lernstand.
- Rechner für Token-Kosten, mögliche Zeitersparnis und Amortisation. Die voreingestellten Werte sind Beispiele und können angepasst werden.
- Notizen und Fortschritt werden lokal im Browser gespeichert. Ein JSON-Export und -Import ermöglicht Backups und den Umzug auf ein anderes Gerät.
- Dark Mode, lokale Icons und ein Service Worker für die Offline-Nutzung nach dem ersten Online-Aufruf. Es werden keine externen Bibliotheken oder Tracker eingebunden.

## Installieren und offline nutzen

Öffne den Link oben zunächst mit Internetverbindung. Wähle auf iPhone oder iPad in Safari **Teilen → Zum Home-Bildschirm**; unter Android findest du **App installieren** oder **Zum Startbildschirm hinzufügen** im Browsermenü. Auf unterstützten Desktop-Browsern erscheint eine Installationsoption in der Adressleiste oder im Menü.

Lernstand und Notizen bleiben im jeweiligen Browser bzw. in der installierten App. Sie werden nicht automatisch zwischen Geräten synchronisiert; verwende dafür den JSON-Export und -Import.

## Dateien und lokale Nutzung

`index.html` enthält die Oberfläche und Logik, `manifest.webmanifest` die Installationsangaben, `sw.js` den Offline-Cache und die PNG-Dateien die App-Icons. Für Service Worker und Installation ist HTTPS oder `localhost` erforderlich. Beispielsweise lässt sich der Projektordner mit einem lokalen HTTP-Server öffnen. Beim direkten Öffnen der HTML-Datei funktionieren die interaktiven Bereiche, aber kein Service Worker.

Bei Änderungen an Dateien, die offline zwischengespeichert werden, muss die Cache-Version in `sw.js` erhöht werden, damit neue Inhalte auf bereits installierten Geräten ankommen.

