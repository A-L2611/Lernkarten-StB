# StB Prüfungstrainer – installierbare Web-App

**Ziel:** Vorbereitung auf die mündliche Steuerberaterprüfung am 1. März 2027.

## Dateien
- `index.html` – App-Struktur und Ansichten
- `styles.css` – responsives Design für iPhone und Desktop
- `app.js` – Lernkarten, Fachfragen, Simulation, Bewertungen und lokaler Lernstand
- `manifest.webmanifest` – Installationsmetadaten der PWA
- `sw.js` – Offline-Caching für zuvor geladene App-Dateien

## Schnellstart am Computer
Ein Service Worker und die PWA-Installation funktionieren nur über `https://` oder `localhost`. Im Projektordner kann ein lokaler Testserver gestartet werden, z. B. mit Python:

```bash
python3 -m http.server 8000
```

Dann im Browser `http://localhost:8000` öffnen. Offline-Funktionen werden nach dem ersten Laden verfügbar, sobald der Service Worker installiert wurde.

## Auf dem iPhone installieren
1. Die Dateien unverändert in einen Webhosting-Ordner hochladen, der über **HTTPS** erreichbar ist. Die Dateien müssen gemeinsam im selben Verzeichnis liegen.
2. Die URL in Safari auf dem iPhone öffnen und die Seite einmal vollständig laden.
3. Auf **Teilen** tippen und **Zum Home-Bildschirm** auswählen. Falls angezeigt, **Als Web-App öffnen** aktivieren; dann **Hinzufügen**.
4. Die App über das neue Home-Bildschirm-Symbol starten. Für Offline-Nutzung die App zunächst bei bestehender Internetverbindung öffnen.

## Funktionen
- Lernkarten mit Musterantwort und Selbsteinschätzung
- Fachfragen mit Lösungsentwurf und vier Kriterien zur Selbstbewertung
- Mündliche Simulation mit 3-Minuten-Timer, Erwartungshorizont und Bewertungsraster
- Fortschritt nach Prüfungsgebiet, Aktivitätsverlauf und JSON-Export
- Speicherung mit `localStorage` im jeweiligen Browser auf dem jeweiligen Gerät

## Grenzen und Datenschutz
- Die Bewertung ist eine **Selbstbewertung**, keine automatische KI-Bewertung und keine amtliche Prüfungsnote.
- Es gibt kein Benutzerkonto und keine Cloud-Synchronisation. Browserdaten löschen oder privater Modus können den Lernstand entfernen. Regelmäßig exportieren.
- Die erste Version verwendet keine Mikrofonaufnahme und sendet keine Lernantworten an einen Server.
- Die Lerninhalte sind beispielhafte Lernimpulse, keine Rechtsberatung. Die Rechtslage kann sich bis zum Prüfungstermin ändern. Normen und Verwaltungsauffassungen anhand der jeweils aktuellen amtlichen Quellen prüfen.

## Amtliche Startquellen
- § 37 StBerG (Prüfungsgebiete): https://www.gesetze-im-internet.de/stberg/__37.html
- § 26 DVStB (mündliche Prüfung): https://www.gesetze-im-internet.de/stbdv/__26.html
- AO: https://www.gesetze-im-internet.de/ao_1977/
- EStG: https://www.gesetze-im-internet.de/estg/
- UStG: https://www.gesetze-im-internet.de/ustg_1980/
- BFH: https://www.bundesfinanzhof.de/
- BMF: https://www.bundesfinanzministerium.de/

## Hinweise zur Rechtsaktualität
Die App zeigt keinen automatisiert synchronisierten Rechtsstand. Insbesondere Beispiele zu AO, KStG, UStG, Gesellschafts- und Berufsrecht müssen vor dem Lernen als aktuelle Rechtsaussage gegen die amtliche Fassung geprüft werden. Das Prüfungsgebietsspektrum ist an § 37 Abs. 3 StBerG orientiert; die konkrete mündliche Prüfung richtet sich nach den geltenden Vorschriften, insbesondere DVStB.

