# create-docker-host

## Man benötigt:

* Ubuntu 18.04 Server als Basis
* git und ansible installiert: ``apt install git ansible``
* Passwortlosen SSH-Zugang auf Port 22, wenn man nicht direkt an der Konsole sitzt.

## Inbetriebnahme:

* ``git clone https://github.com/linuxmuster-ext-docker/create-docker-host.git``
* ``cd create-docker-host``
* ``ansible-playbook dockerhost.yml``

Jetzt hat man einen einfachen Dockerfähigen Server mit Grundabsicherung:

## Wichtige installierte Pakete:

* docker-ce aus den Docker-Repositorys
* docker-compose direkt von Github
* ufw
* nginx
* dehydrated

## Anmerkungen: 

* ufw hat als default policy deny, erlaubt sind per default nur die Ports 80, 443 und 22. Man muss davon abweichende Ports von Containern also später explizit freigeben, damit nicht versehentlich beim Starten von Containern Dienste unbeabsichtigt exposed werden.
* **Die SSH Anmeldung per Passwort wird durch das Playbook deaktviert**, man muss also vorher sicherstellen, dass man mit einem SSH Key auf den Server kommt.
