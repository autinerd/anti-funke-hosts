English version [below](#anti-funke-hosts-file)

# Anti-Funke-Hostsdatei

Diese Datei blockiert alle Verbindungen zu Webseiten, die entweder der Funke Mediengruppe gehören oder eine Verbindung mit dieserA hosts file which blocks all services from Funke Verlag. haben.

## Installation

### uBlock Origin und andere Werbeblocker-Addons

- Füge `https://raw.githubusercontent.com/autinerd/anti-funke-hosts/master/funke-hosts` zu den benutzerdefinierten Filterlisten hinzu

### Windows (ohne weitere Tools, benötigt Adminrechte)

- Inhalt der Datei `funke-hosts` in die Datei `%WINDIR%\System32\etc\hosts` einfügen

### Linux/macOS (ohne weitere Tools, benötigt root-Rechte)

- Inhalt der Datei `funke-hosts` in die Datei `/etc/hosts` einfügen

### Android (mit Rootrechten)

- Installiere [AdAway](https://github.com/AdAway/AdAway) oder ähnliches auf das Gerät, danach füge den Link von [oben](#ublock-origin-und-andere-werbeblocker-addons) in die Liste der Hostsdateien hinzu.

### Android (ohne Rootrechte)

- Installiere [Blockada](https://github.com/blokadaorg/blokada) auf das Gerät, im Menü unter "Werbeblocker" füge den Link von [oben](#ublock-origin-und-andere-werbeblocker-addons) in die Liste der Hostslisten hinzu

### Pi-Hole

- Auf der Adminoberfläche unter "Group management" > "Adlists" füge den Link von [oben](#ublock-origin-und-andere-werbeblocker-addons) zu den Listen hinzu.

### AdGuard Home

- Auf der Weboberfläche unter "Filter" > "DNS-Sperrliste" > "Sperrliste hinzufügen" > "Eigene Sperrliste" den Link von [oben](#ublock-origin-und-andere-werbeblocker-addons) einfügen.

### iOS ([AdGuard](https://apps.apple.com/de/app/adguard-adblock-privacy/id1047223162))

Nicht vergessen den Content Blocker für Safari zu aktivieren

#### Ohne Subscription
  - Öffne die AdGuard settings -> Safari Protection -> User rules
  - Lade die [ios-adguard.txt](https://raw.githubusercontent.com/autinerd/anti-funke-hosts/master/ios-adguard.txt) runter
  - importiere diese Datei in die User Rules

#### Mit Subscription
  - Füge `https://raw.githubusercontent.com/autinerd/anti-funke-hosts/master/funke-hosts` zu den benutzerdefinierten Filterlisten hinzu


## Unterstützen

Wenn Sie eine Domain finden, die nicht auf der Liste ist, aber zu Funke gehört oder aber eine Domain, die nicht zu Funke gehört aber auf der Liste ist, öffnen Sie einfach ein Issue oder ein Pull Request.

Beachten Sie, dass Domains, die auch mit "www." verfügbar sind (wie b\*\*d.de -> www.b\*\*d.de), in die Datei `www-hostnames` gehören, andere in die `hostnames`.

Bei Pull Requests: Nach dem Hinzufügen von Domains bitte `python ./generate_hostfile.py` ausführen.

Natürlich hilft auch ein Teilen dieser Liste an Bekannte und Freunde!

# Anti Funke hosts file

This file blocks all connections to sites which are from Funke Verlag or have a connection with them.

## How to install

### Windows (without further tools, needs admin permissions):

- Paste the content of the file `funke-hosts` into `%WINDIR%\System32\etc\hosts`

### Linux/macOS (without further tools, needs admin permissions):

- Paste the content of the file `funke-hosts` into `/etc/hosts`

### uBlock Origin and other adblock add-ons

- Add `https://raw.githubusercontent.com/autinerd/anti-funke-hosts/master/funke-hosts` to the custom filter lists.

### Android (with root access)

- Install [AdAway](https://github.com/AdAway/AdAway) or similar on your phone, then add the link from [above](#ublock-origin-and-other-adblock-add-ons) to the list of hosts-files.

### Android (without root access)

- Install [Blockada](https://github.com/blokadaorg/blokada) on your phone, then add the link from [above](#ublock-origin-and-other-adblock-add-ons) to the lists in "Ad blocker"

### Pi-hole

- In your [Pi-hole](https://pi-hole.net/) admin interface under "Group management" > "Adlists" add `https://raw.githubusercontent.com/autinerd/anti-funke-hosts/master/funke-hosts` to your blocklists and update Gravity.

### AdGuard Home

- In your AdGuard Home web interface add `https://raw.githubusercontent.com/autinerd/anti-funke-hosts/master/funke-hosts` as a new blocklist at "Filter" > "DNS blocklist"

### iOS ([AdGuard](https://apps.apple.com/de/app/adguard-adblock-privacy/id1047223162))

Don't forget to activate the Content Blocker for Safari

#### without subscription
  - open the AdGuard settings -> Safari Protection -> User rules
  - download [ios-adguard.txt](https://raw.githubusercontent.com/autinerd/anti-funke-hosts/master/ios-adguard.txt)
  - import this file to the User Rules

#### with Subscription
  - Add `https://raw.githubusercontent.com/autinerd/anti-funke-hosts/master/funke-hosts` to the custom filter lists.


## Contributing

When you find a domain which belongs to Funke Verlag and it's not on the list or there is a domain on the list which doesn't belong to Funke Verlag, feel free to open an issue or do a pull request.

Please be aware, that domains which have a "www." counterpart (like b\*\*d.de -> www.b\*\*d.de) has to be in the `www-hostnames`, other domains in the `hostnames` file.

For pull requests: After adding the domains, please run `python ./generate_hostfile.py`

Of course sharing the list helps a lot as well!
