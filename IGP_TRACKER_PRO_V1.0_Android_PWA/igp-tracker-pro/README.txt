IGP TRACKER PRO 1.0 – Android Progressive Web App
=================================================

INHALT
index.html, styles.css, app.js, manifest.webmanifest, sw.js, icons/

FUNKTIONEN
- Hundeprofile (Name, Rasse, Geburtsdatum, Ausbildungsstand, Notizen)
- GPS-Fährten legen und aufzeichnen, Wegstrecke, Zeit, GPS-Genauigkeit
- Winkel und Gegenstände während des Legens markieren
- Späteren Suchweg für eine gespeicherte Fährte aufnehmen
- Liegezeit, Legeweg und Suchweg anzeigen; GPS-Spuren grafisch vergleichen
- Trainingskalender, Übungen und Bewertungen
- Offline-Datenbank mit IndexedDB
- Export/Import einer vollständigen JSON-Datensicherung

INSTALLATION AUF ANDROID
1. ZIP-Datei entpacken und alle Dateien in einen Ordner legen.
2. Ordner auf einen HTTPS-fähigen Webhost laden (z. B. GitHub Pages,
   Netlify oder eigener Webserver mit HTTPS). Nur index.html lokal
   öffnen genügt für GPS und PWA-Installation NICHT.
3. In Android Chrome die HTTPS-Adresse öffnen.
4. Browsermenü ⋮ > "App installieren" bzw. "Zum Startbildschirm hinzufügen".
5. Standortfreigabe erlauben. Nach dem ersten Laden ist die Oberfläche offline nutzbar.

LOKALER PC-TEST
In diesem Ordner ein Terminal öffnen, dann:
  python -m http.server 8000
Danach http://localhost:8000 in Chrome öffnen.
Hinweis: localhost am PC erlaubt PC-GPS, nicht automatisch das
GPS eines per WLAN verbundenen Android-Smartphones. Android benötigt HTTPS.

WICHTIGE GRENZEN
- Android Chrome kann Geolocation bei Displaysperre/App-Wechsel unterbrechen.
  Bei einer aktiven Fährte Bildschirm anlassen. Kein Hintergrund-GPS garantiert.
- Die Karte zeigt GPS-Spuren maßstabsgetreu auf einem eigenen Koordinatengitter,
  KEINE Satellitenkarte oder OpenStreetMap-Kacheln.
- GPS ist nicht zentimetergenau; Markierungen entsprechen der Handyposition.
- Browserdaten löschen bzw. Chrome deinstallieren kann alle Einträge vernichten.
  Deshalb regelmäßig unter "Daten" ein JSON-Backup exportieren.
- Keine Server, keine Cloud-Synchronisation, keine Nutzerkonten.
- Nicht die Software des Drittanbieters Knurrix.
