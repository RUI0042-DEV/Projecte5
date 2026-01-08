# Guia de Configuració: Servidor FTP (vsftpd)

## 1. Configuració Inicial i Instal·lació

Per a aquesta activitat, s'utilitza un entorn amb Ubuntu Server configurat amb dues interfícies de xarxa: ``NAT`` per a la sortida a Internet i ``Host-only`` per permetre la comunicació amb la màquina física.

Abans d'instal·lar alguna cosa recordeu actualitzar si no sabeu com actualitzar aquest és la comanda.

```
Sudo apt update && sudo apt upgrade -y
```

Instal·lació: Executa la següent comanda com a root per instal·lar el servei: 

```
apt install vsftpd
```

> Si no saps com posar-te en root és 'Sudo su'

## 2. FTP Anònim

L'accés anònim permet que qualsevol usuari es connecti sense necessitat d'un compte personal.

Configurarem l'arxiu ``vsftpd.conf``

Un cop dins l'arxiu Cal buscar la línia ``anonymous_enable=NO`` i canviar-la a ``YES``, reiniciant el servei després.

El directori de treball per defecte és ``/srv/ftp``. Crearem una estructura organitzada:

- Crear carpetes: ``mkdir -p /srv/ftp/pub/files /srv/ftp/pub/music /srv/ftp/pub/pics``.
- Afegir fitxers de prova: Pots crear fitxers buits per provar les descàrregues: ``touch /srv/ftp/pub/files/info.txt.``  ``touch /srv/ftp/pub/pics/sun.jpg``.

