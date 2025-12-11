# Basic Homelab

Vous trouverez ici la documentation sur comment réaliser un homelab de base. Le but étant de séparer le réseau de compagnie en deux; un public et un privé. Le segment privé supportera un serveur gitolite et sera uniquement filaire. Le segment public sera accessible par wi-fi. Le tout passeras par un miniPC avec OpnSense qui sera le pare-feu et le routeur du réseau.

## Voici le schéma du réseau expliqué ci-dessus

![](screenshot/schemafinal.png)

# Installation des OS pour le client et le serveur
Balena etcher est un outil facile à utiliser pour formater le périphérique qui va contenir l'OS (une carte SD ou une clé USB)  que vous voulez installer. Voici le lien : [Balena etcher](https://etcher.balena.io/)
## Client: Manjaro OS

Lien pour le téléchargement: [Manjaro OS](https://manjaro.org/)

Allez dans votre bios et dites lui de boot à partir de la clé USB qui contient l'OS

Si vous avez bien configuré le BIOS vous allez être dirigé automatiquement à cette fenêtre lors de l'ouverture de votre ordinateur.
![](screenshot/Manjaro/1.png)

Pour démarrer l'installation cliquez sur "Boot with open source driver"

![](screenshot/Manjaro/2.png)

1. Lancer l'installation

![](screenshot/Manjaro/3.png)

1. Choix de la langue
2. Suivant

![](screenshot/Manjaro/4.png)

Normalement le BIOS de votre ordinateur devrait vous donner la bonne région et zone. Sinon simplement les changer pour votre fuseau horaire.
1. suivant

![](screenshot/Manjaro/5.png)

Choisissez votre clavier
1. Suivant

![](screenshot/Manjaro/6.png)

Si votre ordinateur a plusieurs disques choisissez celui sur lequel vous voulez installer l'OS.
1. Effacer le disque pour partir à neuf
2. Suivant

![](screenshot/Manjaro/7.png)

Création d'utilisateur. Faites attention de ne pas oublier ces informations.
1. Suivant

![](screenshot/Manjaro8.png)

1. J'ai choisi de ne pas installer de suite Office car j'utilise nano et vim. Le choix vous appartient.
2. Suivant

![](screenshot/Manjaro/9.png)

Ce n'est pas Windows alors prenez le temps de lire si tout semble concorder avec vos besoins et ensuite cliquer sur Installer pour démarrer l'installation.

![](screenshot/Manjaro/10.png)

1. Installer Maintenant

![](screenshot/Manjaro/11.png)

L'installation est en cours.

![](screenshot/Manjaro/12.png)

1. Assurez-vous que "Redémarrer maintenant" est coché.
2. Terminé

### LORS DU REDÉMARRAGE IL FAUT ENLEVER LA CLÉ USB QUI CONTIENT L'OS POUR NE PAS ÊTRE DIRIGER ENCORE VERS L'INSTALLATION

## Serveur: Ubuntu Server

Lien pour le téléchargement: [Ubuntu Server](https://ubuntu.com/download/server)

Allez dans votre bios et dites lui de boot à partir de la clé USB qui contient l'OS
Si vous avez bien configuré le BIOS vous allez être dirigé automatiquement à cette fenêtre lors de l'ouverture de votre ordinateur.

![](screenshot/Ubuntuserver/1.png)

Appuyez sur "Entrée" pour continuer. Choisissez la première option.

![](screenshot/Ubuntuserver/2.png)

Choisissez la langue de votre choix. Anglais est un bon choix aussi.

![](screenshot/Ubuntuserver/3.png)

1. Vous pouvez appuyer sur "Identifier le clavier" et l'installeur saura trouver votre clavier de choix.
2. Terminé

![](screenshot/Ubuntuserver/4.png)

1. Ubuntu Server
2. Terminé

![](screenshot/Ubuntuserver/5.png)

Choisissez votre bonne interface réseau.
1. Terminé

![](screenshot/Ubuntuserver/6.png)

Pas besoin de gérer ça pour ce qu'on va faire.
1. Terminé

![](screenshot/Ubuntuserver/7.png)

J'ai laissé l'adresse du mirroir par défaut.
1. Terminé

![](screenshot/Ubuntuserver/8.png)

1. Choisissez le disque que vous voulez.
2. Laissez l'option LVM group de coché
3. Terminé

![](screenshot/Ubuntuserver/9.png)

Vérifiez que tout est OK.
1. Terminé

![](screenshot/Ubuntuserver/10.png)

Le pop-up vous annonce que l'installation va commencer.
1. Continuer

![](screenshot/Ubuntuserver/11.png)

1. N'oubliez pas ces informations.
2. Terminé

![](screenshot/Ubuntuserver/12.png)

On ne payera pas pour Ubuntu Pro alors cochez "Skip for now" et continuez.

![](screenshot/Ubuntuserver/13.png)

### Cette étape est importante, il faut absolument utiliser le serveur openSSH pour facilement se connecter au serveur Ubuntu à partir de la machine client ###

1. Assurez-vous que l'option est coché.
2. Terminé

![](screenshot/Ubuntuserver/14.png)

Bravo, Ubuntu est installé!
1. Redémarrer maintenant

![](screenshot/Ubuntuserver/15.png)

N'oubliez pas de retirer votre clé USB sinon vous allez avoir cette erreur.

Voici donc comment installer Manjaro OS sur un poste Client et Ubuntu Server sur une machine serveur.
