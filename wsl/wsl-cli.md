
## 🐧 WSL2 – Les commandes essentielles

### 🔹 GÉNÉRAL

|Commande|Utilité|
|-|-|
|`wsl`|Entrer dans Linux|
|`exit` ou `Ctrl+D`|Quitter WSL|
|`wsl -l -v`|Voir les distributions installées|
|`wsl --shutdown`|Arrêter WSL et libérer la RAM|

### 🔹 LANCER / ARRÊTER UNE DISTRIBUTION

|Commande|Utilité|
|-|-|
|`wsl -d <DistroName>`|Lancer une distrib spécifique|
|`wsl -t <DistroName>`|Arrêter une distrib|
|`wsl --set-default <DistroName>`|Définir la distrib par défaut|


### 🔹 COMMANDES À SAVOIR DANS WSL (Linux)

|Commande|Utilité|
|-|-|
|`sudo apt update && sudo apt upgrade -y`|Mettre à jour tout|
|`sudo apt install <paquet>`|Installer un logiciel|
|`sudo apt remove <paquet>`|Désinstaller un logiciel|
|`df -h`|Espace disque disponible|
|`free -h`|Mémoire utilisée|
|`lsblk`|Voir les disques|
|`ip a`|Voir les adresses IP|


### 🔹 ACCÉDER AUX FICHIERS DEPUIS WINDOWS

|Commande / Action|Utilité|
|-|-|
|`\\\\wsl$\\<DistroName>` (dans l'Explorateur)|Accéder aux fichiers Linux|
|`explorer.exe .` (dans WSL)|Ouvrir le dossier courant dans Windows|
|`notepad.exe fichier.txt` (dans WSL)|Ouvrir un fichier avec Notepad|


### 🔹 SAUVEGARDER / RESTAURER

|Commande|Utilité|
|-|-|
|`wsl --export <DistroName> C:\\backup\\<DistroName>.tar`|Sauvegarder une distrib|
|`wsl --import <DistroName> C:\\WSL\\ C:\\backup\\<DistroName>.tar --version 2`|Restaurer une distrib|


