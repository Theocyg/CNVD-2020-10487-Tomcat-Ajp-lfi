# Tomcat AJP LFI (Ghostcat) - Python 3 Version

Ce script est un fork mis à jour pour Python 3 de l'exploit original pour la vulnérabilité CVE-2020-1938 (Ghostcat). Il permet de lire des fichiers arbitraires (LFI) dans les dossiers d'applications web de Tomcat (comme WEB-INF/web.xml) via le protocole AJP.

### Pourquoi ce Fork ?

L'original était écrit en Python 2, ce qui causait des erreurs majeures dans les environnements de pentest modernes comme Exegol :

    Gestion des sockets : Remplacement de bufsize par buffering pour la compatibilité socket.makefile().

    Encodage : Correction de la gestion des types bytes vs str.

    Protocole AJP : Sérialisation correcte des paquets binaires en Python 3.

### Utilisation :

```bash
python3 CNVD-2020-10487-Tomcat-Ajp-lfi.py <IP_CIBLE> -p <PORT_AJP> -f <CHEMIN_FICHIER>
```
