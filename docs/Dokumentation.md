# Fallstudie WISS Modul 123
Yanis Sebastian Zuercher & Dominik Koenitzer

26.06.24

## Inhaltsverzeichnis
- Übersicht der Kapitel und Seitenzahlen

## Einführung
- Kurze Beschreibung des Projekts und der Ziele
## Planung
### Netzwerkplan
### Adressplanung (Tabellenform)
<table border="1">
    <tr>
        <th>Ressource</th>
        <th>IP-Adresse</th>
        <th>Zuweisung</th>
    </tr>
    <tr>
        <td>Hauptserver</td>
        <td>192.168.1.10</td>
        <td>Statisch</td>
    </tr>
    <tr>
        <td>Backup-Server</td>
        <td>192.168.1.20</td>
        <td>Statisch</td>
    </tr>
    <tr>
        <td>Drucker</td>
        <td>192.168.1.30</td>
        <td>Statisch</td>
    </tr>
    <tr>
        <td>Laptop01</td>
        <td>192.168.1.100</td>
        <td>DHCP</td>
    </tr>
    <tr>
        <td>Laptop02</td>
        <td>192.168.1.101</td>
        <td>DHCP</td>
    </tr>
    <tr>
        <td>Laptop03</td>
        <td>192.168.1.102</td>
        <td>DHCP</td>
    </tr>
    <tr>
        <td>Laptop04</td>
        <td>192.168.1.103</td>
        <td>DHCP</td>
    </tr>
    <tr>
        <td>Laptop05</td>
        <td>192.168.1.104</td>
        <td>DHCP</td>
    </tr>
</table>

### Berechtigungsmatrix
<table border="1">
    <tr>
        <th>Ressource</th>
        <th>Benutzer01</th>
        <th>Benutzer02</th>
        <th>Benutzer03</th>
        <th>Benutzer04</th>
        <th>Benutzer05</th>
        <th>Benutzer06</th>
        <th>Benutzer07</th>
        <th>Benutzer08</th>
        <th>Benutzer09</th>
        <th>Benutzer10</th>
        <th>Admin</th>
    </tr>
    <tr>
        <td>Dateien</td>
        <td>r</td>
        <td>rw</td>
        <td>r</td>
        <td>r</td>
        <td>rw</td>
        <td>r</td>
        <td>rw</td>
        <td>r</td>
        <td>r</td>
        <td>rw</td>
        <td>rwx</td>
    </tr>
    <tr>
        <td>Drucker</td>
        <td>Ja</td>
        <td>Ja</td>
        <td>Ja</td>
        <td>Ja</td>
        <td>Ja</td>
        <td>Ja</td>
        <td>Ja</td>
        <td>Ja</td>
        <td>Ja</td>
        <td>Ja</td>
        <td>Ja</td>
    </tr>
    <tr>
        <td>Backup-Server</td>
        <td>Nein</td>
        <td>Nein</td>
        <td>Nein</td>
        <td>Nein</td>
        <td>Nein</td>
        <td>Nein</td>
        <td>Nein</td>
        <td>Nein</td>
        <td>Nein</td>
        <td>Nein</td>
        <td>Ja</td>
    </tr>
</table>


### Namenskonzepte
- **Geräte:**
  - Hauptserver: Hauptserver
  - Backup-Server: BackupServer
  - Drucker: Drucker01
  - Laptops: Laptop01, Laptop02, Laptop03, Laptop04, Laptop05
  
- **Benutzerkonten:**
  - Benutzer01: Max Mustermann
  - Benutzer02: Erika Musterfrau
  - Benutzer03: Hans Müller
  - Benutzer04: Lisa Meier
  - Benutzer05: Paul Schmidt
  - Benutzer06: Laura Becker
  - Benutzer07: Klaus Schulze
  - Benutzer08: Julia Fischer
  - Benutzer09: Peter Hoffmann
  - Benutzer10: Anna Wagner
  - Admin: Administrator
## Installation des Windows Server 2019 in einer VM
- Grundkonfiguration (Hostname, Zeitzone, Netzwerkverbindungen)
- Schritt-für-Schritt-Anleitung mit Screenshots
# Einrichtung der Dienste
- **DHCP-Server:**
  - Installationsschritte mit Screenshots
  - Konfiguration des DHCP-Bereichs
  - Ausschlüsse und Reservierungen
  - Tests und Ergebnisse
  
- **DNS-Server:**
  - Installationsschritte mit Screenshots
  - Konfiguration der Forward Lookup Zone und Reverse Lookup Zone
  - Erstellen von DNS-Einträgen
  - Tests und Ergebnisse
  
- **Datei- und Druckdienste:**
  - Installationsschritte mit Screenshots
  - Konfiguration der Freigaben
  - Installation und Konfiguration des Druckers
  - Tests und Ergebnisse
  
- **Webserver (IIS):**
  -Installationsschritte mit Screenshots
  - Erstellen und Konfigurieren der Webseite
  - Aktivierung von HTTPS und Installation des Zertifikats
  - Tests und Ergebnisse
