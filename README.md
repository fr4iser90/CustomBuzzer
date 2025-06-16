# CustomBuzzer
Ein elektronischer Bissanzeiger (Fishing Buzzer) basierend auf ESP32

## Projektbeschreibung
Dieses Projekt entwickelt einen modernen, elektronischen Bissanzeiger für Angler mit folgenden Hauptfunktionen:

### Grundfunktionen
- Drahtlose Bissanzeige via WiFi/BLE
- Akkubetrieben für mobile Nutzung
- Temperaturüberwachung
- Einstellbare Empfindlichkeit
- Digitale Anzeige
- Präzise Schnurlauf-Erfassung (zwei Optionen verfügbar)

### Smart Features (App-gesteuert)
- **Bissanzeige:**
  - Push-Benachrichtigungen aufs Smartphone
  - Verschiedene Alarmtöne wählbar
  - Vibration bei Biss
  - Biss-Historie mit Zeitstempel

- **Wetter & Umwelt:**
  - Lufttemperatur-Erfassung
  - Luftfeuchtigkeit-Messung
  - Luftdruck-Monitoring
  - Wettervorhersage-Integration

- **Fischfang-Statistiken:**
  - Biss-Häufigkeit pro Stunde
  - Aktivste Fangzeiten
  - Beste Wetterbedingungen
  - Fang-Tagebuch

- **Energie-Management:**
  - Akku-Status in Echtzeit
  - Energiesparmodus
  - Solar-Ladeunterstützung
  - Akku-Lebensdauer-Prognose

- **Komfort-Funktionen:**
  - Ferneinstellung der Empfindlichkeit
  - Automatische Nachtabschaltung
  - Mehrere Ruten gleichzeitig überwachen
  - GPS-Position der Angelstelle speichern

## Hardware Komponenten
### Hauptkomponenten
- ESP32 Audio Kit (ESP32-A1S) als Hauptcontroller
- KY-040 Drehgeber für Menüeinstellungen
- 3.7V 2000mAh LiPo Akku
- JST PH 2.0 Steckverbinder
- Schrumpfschlauch für Isolierung
- Lötstation für die Montage

### Sensoren & Zusatzkomponenten
- BME280 Sensor (Temperatur, Luftfeuchtigkeit, Luftdruck)
- Vibrationsmotor für haptisches Feedback
- RGB LED für Statusanzeigen
- Solar-Lademodul (optional)
- GPS-Modul (optional)

### Option 1: Optische Schnurlauf-Erfassung
- Mechanisches Röllchen mit Rillen
- IR-Sensor (z.B. TCRT5000) für Bewegungserfassung
- 3D-gedrucktes Gehäuse für Röllchen
- Optische Isolierung für bessere Erkennung

### Option 2: Magnetische Schnurlauf-Erfassung
- Röllchen mit eingebauten Neodym-Magneten
- Hall-Sensor (z.B. A3144) für Rotation
- 3D-gedrucktes Gehäuse für Röllchen
- Magnetische Abschirmung

## Status
Projekt in Entwicklung - Komponenten werden beschafft
- [ ] Hauptkomponenten
- [ ] Sensoren & Zusatzkomponenten
- [ ] Optische Erfassungskomponenten
- [ ] Magnetische Erfassungskomponenten
- [ ] 3D-Druck Dateien für Gehäuse
- [ ] App-Entwicklung

## Hinweis
Beide Schnurlauf-Erfassungsoptionen werden dokumentiert. Die finale Implementierung kann je nach Test-Ergebnissen und Präferenz gewählt werden.

## App-Funktionen (geplant)
- Cross-Platform (Android & iOS)
- Offline-Funktionalität
- Daten-Export (CSV/PDF)
- Mehrsprachige Unterstützung
- Dark/Light Mode
- Backup & Restore der Einstellungen
