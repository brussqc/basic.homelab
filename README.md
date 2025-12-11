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

