# -Anleitung-Samsung-Galaxy-Tab-S9-per-Thunderbolt-USB-C-als-Mac-Zweitmonitor-nutzen-
Diese Anleitung zeigt, wie man ein **Samsung Galaxy Tab S9+** mithilfe des Open-Source-Tools **Side Screen** über eine kabelgebundene Verbindung (Thunderbolt/USB-C) als extrem schnellen, latenzfreien Zweitmonitor für macOS einrichtet.
tranvuongquocdat/sidescreen/sidescreen
```

---

## Schritt 3: Verbindung herstellen & Starten

1. Lade dir die App **Side Screen** aus dem Google Play Store auf dein Galaxy Tab S9+.
2. Verbinde das Tablet über dein Thunderbolt-/USB-C-Kabel mit dem Mac.
3. Auf dem Bildschirm des Tablets erscheint eine Sicherheitsabfrage: **„USB-Debugging zulassen?“**
* *Wichtig:* Setze den Haken bei **„Von diesem Computer immer zulassen“** und bestätige mit **Zulassen**.
4. Starte die **Side Screen** App sowohl auf dem Mac als auch auf dem Tablet.

Der Mac erkennt das Galaxy Tab S9+ nun vollautomatisch über das Kabel und erstellt ein echtes, virtuelles Display. In den macOS-Systemeinstellungen unter *Displays* kannst du die Anordnung und die HiDPI/Retina-Auflösung nach deinen Wünschen anpassen.

Schritt 1: Entwickleroptionen & USB-Debugging auf dem Tablet aktivieren
1. Öffne die **Einstellungen** auf dem Galaxy Tab S9+.
2. Scrolle ganz nach unten zu **Tablet-Informationen** -> **Softwareinformationen**.
3. Tippe **7-mal schnell hintereinander** auf die **Buildnummer**, bis die Meldung *"Der Entwicklermodus wurde aktiviert"* erscheint.
4. Gehe zurück in das Hauptmenü der Einstellungen. Ganz unten befindet sich nun der neue Punkt **Entwickleroptionen**.
5. Öffne diesen und aktiviere den Schalter bei **USB-Debugging**.

Schritt 2: Tools auf dem Mac installieren (via Terminal)

Öffne das Programm **Terminal** auf deinem Mac (über die Spotlight-Suche oder unter *Programme -> Dienstprogramme*).

1. Homebrew installieren (falls noch nicht vorhanden)
Falls `brew` noch nicht auf deinem Mac installiert ist, führe diesen Befehl aus:
```bash
/bin/bash -c "\$(curl -fsSL https://githubusercontent.com)"
```
*Hinweis für Apple Silicon Macs (M1/M2/M3/M4):* Folge nach der Installation den Anweisungen im Terminal unter "Next steps", um die Umgebungsvariablen zu setzen:
```bash
echo 'eval "\((/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile && eval "\)(/opt/homebrew/bin/brew shellenv)"
```

 2. ADB und Side Screen installieren
Führe nun die folgenden Befehle im Terminal aus, um die Android-Plattform-Tools (ADB) und die Side-Screen-App für macOS zu installieren:
```bash
brew install --cask android-platform-tools
brew install --cask tranvuongquocdat/sidescreen/sidescreen
```

Schritt 3: Verbindung herstellen & Starten

1. Lade dir die App **Side Screen** aus dem Google Play Store auf dein Galaxy Tab S9+.
2. Verbinde das Tablet über dein Thunderbolt-/USB-C-Kabel mit dem Mac.
3. Auf dem Bildschirm des Tablets erscheint eine Sicherheitsabfrage: **„USB-Debugging zulassen?“**
* *Wichtig:* Setze den Haken bei **„Von diesem Computer immer zulassen“** und bestätige mit **Zulassen**.
4. Starte die **Side Screen** App sowohl auf dem Mac als auch auf dem Tablet.

Der Mac erkennt das Galaxy Tab S9+ nun vollautomatisch über das Kabel und erstellt ein echtes, virtuelles Display. In den macOS-Systemeinstellungen unter *Displays* kannst du die Anordnung und die HiDPI/Retina-Auflösung nach deinen Wünschen anpassen.
