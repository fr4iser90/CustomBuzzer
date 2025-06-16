# CustomBuzzer
Ein modulares, elektronisches Bissanzeiger-System basierend auf ESP32

## System-Architektur
### Modulares Design
- **Buzzer-Modul:**
  - Eigenständig funktionsfähig
  - Akkubetrieben
  - Integrierte Anzeige und Töne
  - Kann als Einzelgerät oder im Netzwerk betrieben werden

- **Receiver-Modul:**
  - Tragbare Empfangseinheit
  - Einstellbare Empfindlichkeit
  - Eigener Akku
  - Kann mehrere Buzzer empfangen

- **Netzwerk-Modus:**
  - Mesh-Netzwerk für große Reichweite
  - Bis zu 8 Buzzer pro Receiver
  - Automatische Kanalauswahl
  - Verschlüsselte Kommunikation

### Kommunikations-Technologien
- **Kurzstrecke (bis 100m):**
  - BLE (Bluetooth Low Energy)
  - 2.4GHz Funk
  - Geringer Stromverbrauch

- **Mittelstrecke (bis 500m):**
  - LoRa Modul
  - 433MHz Funk
  - Gute Durchdringung

- **Langstrecke (bis 2km):**
  - LoRaWAN
  - Externe Antenne möglich
  - Hohe Reichweite

### Erweiterte Funktionsmodule (Optional)
- **Media-Station:**
  - Spotify Connect Integration
  - Internet Radio (z.B. Angler-Radio)
  - Bluetooth Speaker Mode
  - USB Audio Interface
  - SD-Karten Wiedergabe
  - Sprachsteuerung

- **Angler-Assistent:**
  - Mondphasen-Kalender
  - Gezeiten-Tabellen
  - Angelplatz-Bewertung
  - Köder-Empfehlungen
  - Fischarten-Erkennung (via App)

- **Umwelt-Monitoring:**
  - Wassertemperatur-Sonde
  - Sauerstoffgehalt-Messung
  - pH-Wert Überwachung
  - Strömungsgeschwindigkeit
  - Wassertiefen-Messung
  - Unterwasser-Kamera (optional)

- **Komfort-Erweiterungen:**
  - Solar-Powerbank Integration
  - USB-C Power Delivery
  - Wireless Charging
  - LED-Beleuchtung für Nachtangeln
  - Moskito-Abwehr (UV-Licht)
  - Wetterstation mit Regenradar

- **Sicherheits-Features:**
  - GPS-Tracking
  - Notruf-Funktion
  - Diebstahlschutz
  - Wasserdichtigkeit IP67
  - Akku-Überwachung
  - Temperatur-Überwachung

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

### Kommunikations-Module
- **Buzzer-Modul:**
  - ESP32 mit LoRa Modul
  - Externe Antenne (optional)
  - RGB LED für Status
  - Piezo-Buzzer für lokale Alarme
  - I2S Audio Interface (optional)
  - SD-Karten Slot (optional)
  - USB-C PD Controller (optional)

- **Receiver-Modul:**
  - ESP32 mit LoRa Modul
  - OLED Display (128x64)
  - Vibrationsmotor
  - Einstellbare Lautstärke
  - USB-C Ladeanschluss
  - Bluetooth Audio
  - WiFi für Streaming
  - 3.5mm Audio-Ausgang
  - Verstärker-Modul (optional)

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

### Zusätzliche Module (Optional)
- **Audio-Module:**
  - MAX98357 I2S Verstärker
  - PAM8403 Audio Verstärker
  - VS1053 MP3 Decoder
  - INMP441 Mikrofon

- **Sensoren:**
  - DS18B20 Wassertemperatur-Sonde
  - Atlas Scientific pH-Sensor
  - Atlas Scientific Sauerstoff-Sensor
  - Flowsensor für Strömung
  - Echolot-Modul

- **Energie-Management:**
  - TP4056 Ladecontroller
  - MPPT Solar-Controller
  - BQ25895 USB-C PD Controller
  - Wireless Charging Module

## Status
Projekt in Entwicklung - Komponenten werden beschafft
- [ ] Hauptkomponenten
- [ ] Buzzer-Modul Entwicklung
- [ ] Receiver-Modul Entwicklung
- [ ] Kommunikations-Tests
- [ ] Basis-Features
- [ ] Optional: Media-Station
- [ ] Optional: Angler-Assistent
- [ ] Optional: Umwelt-Monitoring
- [ ] Optional: Komfort-Erweiterungen
- [ ] Optional: Sicherheits-Features
- [ ] 3D-Druck Dateien für Gehäuse
- [ ] App-Entwicklung

## Technische Spezifikationen
### Reichweiten-Tests
- BLE: ~50-100m (abhängig von Umgebung)
- LoRa: ~500m (ohne externe Antenne)
- LoRa mit Antenne: ~2km (Sichtlinie)

### Stromverbrauch
- Buzzer im Standby: ~10mA
- Buzzer aktiv: ~100mA
- Receiver im Standby: ~15mA
- Receiver aktiv: ~120mA

### Akku-Laufzeit
- Buzzer: ~20h (2000mAh)
- Receiver: ~16h (2000mAh)

### Audio-Spezifikationen (Optional)
- **Media-Station:**
  - 3W Stereo Ausgang
  - 24-bit/96kHz Audio
  - Bluetooth 5.0
  - WiFi 802.11n
  - Spotify Connect
  - Internet Radio
  - USB Audio Class 2.0

### Umwelt-Sensoren (Optional)
- Wassertemperatur: -10°C bis +50°C
- pH-Wert: 0-14
- Sauerstoff: 0-20mg/L
- Strömung: 0-5m/s
- Wassertiefe: 0-50m

## App-Funktionen (geplant)
- Cross-Platform (Android & iOS)
- Offline-Funktionalität
- Daten-Export (CSV/PDF)
- Mehrsprachige Unterstützung
- Dark/Light Mode
- Backup & Restore der Einstellungen

## Zukunftspläne
- Integration von KI für Fischarten-Erkennung
- Community-Features (Angelplätze teilen)
- Wettervorhersage mit KI
- Automatische Köder-Empfehlungen
- Integration mit Angel-Apps
- Cloud-Backup der Fangdaten
