# Fallstudie WISS Modul 123
Yanis Sebastian Zuercher & Dominik Koenitzer

26.06.24

## Inhaltsverzeichnis
- Übersicht der Kapitel und Seitenzahlen

## Einführung
- Kurze Beschreibung des Projekts und der Ziele
## Planung
### Netzwerkplan
![netzwerkdiagram](images/Netzwerkdiagram.drawio.png)
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
  - Benutzer01: Jason Bichsel
  - Benutzer02: Benicio Von Felten
  - Benutzer03: Dominik Könitzer
  - Benutzer04: Perret Pascal
  - Benutzer05: Amza Fatlum
  - Benutzer06: Narcisa Knott
  - Benutzer07: Thomas Waelti
  - Benutzer08: Aleksandar Travanov
  - Benutzer09: Marc Bahnmüller
  - Benutzer10: Patrick Meier
  - Admin: Yanis Sebastian Zürcher
## Installation des Windows Server 2019 in einer VM
**Schritt 1:** Neue VM erstellen

Im VirtualBox Manager auf "Neu" geklickt, um eine neue virtuelle Maschine zu erstellen.

![VM_Installation_Anleitung](images/vm_installation/1.png)
<hr>

**Schritt 2:** VM konfigurieren

- Name: Windows Server 2019
- Speicherort der VM angegeben
- ISO-Datei für Windows Server 2019 ausgewählt
- "Unattended Installation überspringen" aktiviert

![VM_Installation_Anleitung](images/vm_installation/2.png)
<hr>

**Schritt 3:** Hardware konfigurieren

- RAM zugewiesen: 14662 MB
- CPUs zugewiesen: 12
- Es sollte im grünen Bereich sein, wie im Bild dargestellt.

![VM_Installation_Anleitung](images/vm_installation/3.png)
<hr>

**Schritt 4:** Virtuelle Festplatte erstellen

- Festplattengrösse: 120 GB

![VM_Installation_Anleitung](images/vm_installation/4.png)
<hr>

**Schritt 5:** VM-Einstellungen überprüfen und erstellen

- Einstellungen überprüft und auf "Fertigstellen" geklickt

![VM_Installation_Anleitung](images/vm_installation/5.png)
<hr>

**Schritt 6:** VM starten

- Windows Server 2019 VM ausgewählt und auf "Starten" geklickt

![VM_Installation_Anleitung](images/vm_installation/6.png)
<hr>

**Schritt 7:** Windows Setup starten

- Sprache, Zeit- und Währungsformat und Tastaturlayout ausgewählt
- Auf "Jetzt installieren" geklickt

![VM_Installation_Anleitung](images/vm_installation/7.png)

![VM_Installation_Anleitung](images/vm_installation/8.png)
<hr>

**Schritt 8:** Betriebssystem auswählen

- Edition: Windows Server 2019 Standard Evaluation (Desktop Experience) ausgewählt

![VM_Installation_Anleitung](images/vm_installation/9.png)
<hr>

**Schritt 9:** Lizenzbedingungen akzeptieren

- Lizenzbedingungen akzeptiert

![VM_Installation_Anleitung](images/vm_installation/10.png)
<hr>

**Schritt 10:** Installationsart auswählen

- "Benutzerdefiniert: Nur Windows installieren (erweitert)" ausgewählt

![VM_Installation_Anleitung](images/vm_installation/11.png)
<hr>

**Schritt 11:** Laufwerk zur Installation auswählen

- Nicht zugewiesenen Speicherplatz (120 GB) ausgewählt und auf "Weiter" geklickt

![VM_Installation_Anleitung](images/vm_installation/12.png)
<hr>

**Schritt 12:** Windows installieren

- Installationsprozess gestartet, Fortschritt verfolgt

![VM_Installation_Anleitung](images/vm_installation/13.png)
<hr>

**Schritt 13:** Administrator-Konto einrichten

- Passwort für das Administratorkonto festgelegt

![VM_Installation_Anleitung](images/vm_installation/14.png)
<hr>

**Schritt 14:** Windows Setup abschließen

- Nach Abschluss des Setups, Anmeldebildschirm erreicht

![VM_Installation_Anleitung](images/vm_installation/15.png)



## Einrichtung der Dienste
### DHCP-Server
#### Installationsschritte:

**Schritt 1:** Öffnen des Server Managers

Im Server Manager habe ich auf "Add roles and features" geklickt, um die Rolle des DHCP-Servers hinzuzufügen.

![1](images/dhcp/1.png)
<hr>

**Schritt 2:** DHCP-Server Rolle auswählen

Ich habe die Rolle "DHCP Server" ausgewählt und installiert.

![7](images/dhcp/2.png)
<hr>

**Schritt 3:** DHCP-Manager öffnen

Nach der Installation habe ich im Server Manager auf "Tools" geklickt und dann "DHCP" ausgewählt.

![6](images/dhcp/3.png)
<hr>

**Schritt 4:** Neuen Bereich hinzufügen

Im DHCP-Manager habe ich auf "IPv4" rechtsgeklickt und "New Scope..." ausgewählt.

![2](images/dhcp/4.png)
<hr>

**Schritt 5:** Bereich benennen

Ich habe den Bereich "Scope1" genannt und eine Beschreibung "1" hinzugefügt.

![3](images/dhcp/5.png)
<hr>

**Schritt 6:** IP-Adressbereich festlegen

Ich habe den Start-IP-Bereich auf `192.168.1.100` und den End-IP-Bereich auf `192.168.1.200` festgelegt. Die Subnetzmaske ist `255.255.255.0`.

![4](images/dhcp/6.png)
<hr>

**Schritt 7:** Ausschlüsse und Verzögerung

Ich habe keine Ausschlüsse hinzugefügt und die Standardverzögerung beibehalten.

![5](images/dhcp/7.png)
<hr>

**Schritt 8:** Lease-Dauer festlegen

Ich habe die Lease-Dauer auf 8 Tage eingestellt.
![10](images/dhcp/8.png)
<hr>

**Schritt 9:** DHCP-Optionen konfigurieren

Ich habe ausgewählt, dass ich die DHCP-Optionen jetzt konfigurieren möchte.

![8](images/dhcp/9.png)
<hr>

**Schritt 10:** Standard-Gateway konfigurieren

Ich habe die IP-Adresse des Routers als `192.168.1.1` hinzugefügt.

![9](images/dhcp/10.png)
<hr>

**Schritt 11:** DNS-Server konfigurieren

Ich habe `192.168.1.10` und `8.8.8.8` als DNS-Server hinzugefügt.

![11](images/dhcp/11.png)
<hr>

**Schritt 12:** WINS-Server konfigurieren

Ich habe keine WINS-Server hinzugefügt.

![12](images/dhcp/12.png)
<hr>

**Schritt 13:** Bereich aktivieren

Ich habe ausgewählt, dass der Bereich jetzt aktiviert wird.

![13](images/dhcp/13.png)
<hr>

**Schritt 14:** Assistent beenden

Ich habe den Assistenten gefinished.

![14](images/dhcp/14.png)
<hr>

#### Ausschlüsse und Reservierungen

**Schritt 1:** Neue Reservierung hinzufügen

Im DHCP-Manager habe ich auf "Reservations" rechtsgeklickt und "New Reservation..." ausgewählt.

![15](images/dhcp/15.png)
<hr>

**Schritt 2:** Reservierung für Laptop01

Ich habe eine Reservierung für `Laptop01` mit der IP-Adresse `192.168.1.100` und der MAC-Adresse `90:5b:cd:69:7b:c2` erstellt. Beschreibung: `Benutzer01 - Jason Bichsel`.

![16](images/dhcp/16.png)
<hr>

**Schritt 3:** Reservierung für Laptop02

Ich habe eine Reservierung für `Laptop02` mit der IP-Adresse `192.168.1.101` und der MAC-Adresse `ab:12:14:56:00:36` erstellt. Beschreibung: `Benutzer02 - Benicio Von Felten`.

![17](images/dhcp/17.png)
<hr>

**Schritt 4:** Reservierung für Laptop03

Ich habe eine Reservierung für `Laptop03` mit der IP-Adresse `192.168.1.102` und der MAC-Adresse `5c:e:3:59:1e:b0:62` erstellt. Beschreibung: `Benutzer03 - Dominik Koenitzer`.

![18](images/dhcp/18.png)
<hr>

**Schritt 5:** Reservierung für Laptop04

Ich habe eine Reservierung für `Laptop04` mit der IP-Adresse `192.168.1.103` und der MAC-Adresse `77:1e:17:03:ca:5b` erstellt. Beschreibung: `Benutzer04 - Perret Pascal`.

![19](images/dhcp/19.png)
<hr>

**Schritt 6:** Reservierung für Laptop05

Ich habe eine Reservierung für `Laptop05` mit der IP-Adresse `192.168.1.104` und der MAC-Adresse `16:79:be:6e:70:60` erstellt. Beschreibung: `Benutzer05 - Amza Fatlum`.

![20](images/dhcp/20.png)
<hr>


  
## DNS-Server
#### Installationsschritte:

**Schritt 1:** Öffnen des Server Managers

Im Server Manager habe ich auf "Add roles and features" geklickt, um die Rolle des DNS-Servers hinzuzufügen.

![1](images/dns/1.png)
<hr>

**Schritt 2:** DNS-Server Rolle auswählen

Ich habe die Rolle "DNS Server" ausgewählt und installiert.

![2](images/dns/2.png)
<hr>

**Schritt 3:** DNS-Manager öffnen

Nach der Installation habe ich im Server Manager auf "Tools" geklickt und dann "DNS" ausgewählt.

![3](images/dns/3.png)
<hr>

**Schritt 4:** Neue Zone hinzufügen

Im DNS-Manager habe ich auf "Forward Lookup Zones" rechtsgeklickt und "New Zone..." ausgewählt.

![4](images/dns/4.png)
<hr>

**Schritt 5:** Zonentyp auswählen

Ich habe "Primary zone" ausgewählt.

![5](images/dns/6.png)
<hr>

**Schritt 6:** Zonenname eingeben

Ich habe den Zonennamen "test.local" eingegeben.

![6](images/dns/7.png)
<hr>

**Schritt 7:** Zonen-Datei erstellen

Ich habe ausgewählt, eine neue Zonen-Datei zu erstellen mit dem Namen "test.local.dns".

![7](images/dns/8.png)
<hr>

**Schritt 8:** Dynamische Updates konfigurieren

Ich habe ausgewählt, dass keine dynamischen Updates erlaubt sind.

![8](images/dns/9.png)
<hr>

**Schritt 9:** Assistent beenden

Ich habe den Assistenten gefinished.

![9](images/dns/10.png)
<hr>

**Schritt 10:** Reverse Lookup Zone hinzufügen

Im DNS-Manager habe ich auf "Reverse Lookup Zones" rechtsgeklickt und "New Zone..." ausgewählt.

![10](images/dns/11.png)
<hr>

**Schritt 11:** Zonentyp auswählen

Ich habe "Primary zone" ausgewählt.

![11](images/dns/12.png)
<hr>

**Schritt 12:** IPv4 Reverse Lookup Zone auswählen

Ich habe "IPv4 Reverse Lookup Zone" ausgewählt.

![12](images/dns/13.png)
<hr>

**Schritt 13:** Reverse Lookup Zone Name eingeben

Ich habe den Namen der Reverse Lookup Zone als "0.1.168.192.in-addr.arpa" eingegeben.

![13](images/dns/14.png)
<hr>

**Schritt 14:** Zonen-Datei erstellen

Ich habe ausgewählt, eine neue Zonen-Datei zu erstellen mit dem Namen "0.1.168.192.in-addr.arpa.dns".

![14](images/dns/15.png)
<hr>

**Schritt 15:** Dynamische Updates konfigurieren

Ich habe ausgewählt, dass keine dynamischen Updates erlaubt sind.

![15](images/dns/16.png)
<hr>

**Schritt 16:** Assistent beenden

Ich habe den Assistenten gefinished.

![16](images/dns/17.png)
<hr>

#### Erstellen von DNS-Einträgen

**Schritt 1:** Neuen Host hinzufügen

Im DNS-Manager habe ich auf die Forward Lookup Zone "test.local" rechtsgeklickt und "New Host (A or AAAA)..." ausgewählt.

![17](images/dns/18.png)
<hr>

**Schritt 2:** Host für Hauptserver hinzufügen

Ich habe einen neuen Host "Hauptserver" mit der IP-Adresse "192.168.1.10" hinzugefügt.

![18](images/dns/19.png)
<hr>

**Schritt 3:** Host für BackupServer hinzufügen

Ich habe einen neuen Host "BackupServer" mit der IP-Adresse "192.168.1.20" hinzugefügt.

![19](images/dns/20.png)
<hr>

**Schritt 4:** Host für Drucker hinzufügen

Ich habe einen neuen Host "Drucker01" mit der IP-Adresse "192.168.1.30" hinzugefügt.
![20](images/dns/21.png)
<hr>

**Schritt 5:** Host für Laptop01 hinzufügen

Ich habe einen neuen Host "Laptop01" mit der IP-Adresse "192.168.1.100" hinzugefügt.

![21](images/dns/22.png)
<hr>

**Schritt 6:** Host für Laptop02 hinzufügen

Ich habe einen neuen Host "Laptop02" mit der IP-Adresse "192.168.1.101" hinzugefüt.

![22](images/dns/23.png)
<hr>

**Schritt 7:** Host für Laptop03 hinzufügen

Ich habe einen neuen Host "Laptop03" mit der IP-Adresse "192.168.1.102" hinzugefügt.
![23](images/dns/24.png)
<hr>

#### Übersicht der DNS-Einträge

Hier ist die Übersicht der erstellten DNS-Einträge:

![24](images/dns/25.png)
<hr>


  
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
