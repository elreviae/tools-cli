## 🐧 WSL2 – Les commandes essentielles

### 🔹 GÉNÉRAL

| Commande | Utilité |
|---|---|
| `wsl` | Entrer dans Linux |
| `exit` ou `Ctrl+D` | Quitter WSL |
| `wsl -l -v` | Voir les distributions installées |
| `wsl --shutdown` | Arrêter WSL et libérer la RAM |
| `wsl --status` | Voir l'état et la configuration de WSL |

---

### 🔹 INSTALLER / SUPPRIMER UNE DISTRIBUTION

| Commande | Utilité |
|---|---|
| `wsl --list --online` ou `wsl -l -o` | Voir les distributions disponibles |
| `wsl --install -d <DistroName>` | Installer une nouvelle distrib |
| `wsl --unregister <DistroName>` | Supprimer une distrib (⚠️ irréversible) |

---

### 🔹 LANCER / ARRÊTER UNE DISTRIBUTION

| Commande | Utilité |
|---|---|
| `wsl -d <DistroName>` | Lancer une distrib spécifique |
| `wsl -t <DistroName>` | Arrêter une distrib |
| `wsl --set-default <DistroName>` | Définir la distrib par défaut |
| `wsl --set-version <DistroName> 2` | Passer une distrib en WSL2 |
| `wsl --set-default-version 2` | Définir WSL2 par défaut pour les nouvelles installs |

---


### 🔹 COMMANDES À SAVOIR DANS WSL (Linux)

| Commande | Utilité |
|---|---|
| `sudo apt update && sudo apt upgrade -y` | Mettre à jour tout |
| `sudo apt install <paquet>` | Installer un logiciel |
| `sudo apt remove <paquet>` | Désinstaller un logiciel |
| `sudo apt autoremove` | Supprimer les dépendances inutiles |
| `df -h` | Espace disque disponible |
| `free -h` | Mémoire utilisée |
| `lsblk` | Voir les disques |
| `ip a` | Voir les adresses IP |
| `pwd` | Afficher le chemin du dossier courant |
| `ls -la` | Lister les fichiers (y compris cachés) |
| `cd <dossier>` | Changer de dossier |
| `sudo -i` | Devenir root temporairement |

---

### 🔹 ACCÉDER AUX FICHIERS DEPUIS WINDOWS

| Commande / Action | Utilité |
|---|---|
| `\\wsl$\<DistroName>` (dans l'Explorateur) | Accéder aux fichiers Linux |
| `explorer.exe .` (dans WSL) | Ouvrir le dossier courant dans Windows |
| `notepad.exe fichier.txt` (dans WSL) | Ouvrir un fichier avec Notepad |
| `code .` (dans WSL) | Ouvrir le dossier avec VS Code (si installé) |

---

### 🔹 SAUVEGARDER / RESTAURER

| Commande | Utilité |
|---|---|
| `wsl --export <DistroName> C:\backup\<DistroName>.tar` | Sauvegarder une distrib |
| `wsl --import <DistroName> C:\WSL\ C:\backup\<DistroName>.tar --version 2` | Restaurer une distrib |
| `wsl --export <DistroName> -` | Exporter vers la sortie standard (pour pipe) |

---

### 🔹 COMMANDES D'URGENCE / DÉPANNAGE

| Commande | Utilité |
|---|---|
| `wsl --shutdown` | Arrêter toutes les VM et libérer la RAM |
| `wsl -t <DistroName>` | Forcer l'arrêt d'une distrib spécifique |
| `wsl --status` | Vérifier l'état de WSL |
| `wsl --help` | Afficher l'aide complète |

---

### 🔹 EXÉCUTER UNE COMMANDE LINUX DEPUIS POWERSHELL

| Commande | Utilité |
|---|---|
| `wsl ls -la` | Exécuter `ls -la` dans Linux |
| `wsl sudo apt update` | Exécuter `apt update` (avec droits) |
| `wsl -- cd /home && ls` | Enchaîner des commandes Linux |

---

## 💡 Astuces complémentaires


> **RAPPEL :** Si on ferme la fenêtre WSL avec la croix `✖`, la VM continue de tourner en arrière-plan. Utilisez `wsl --shutdown` pour tout arrêter proprement.
>
> **📁 Emplacement du disque virtuel :**  
> `C:\Users\<VotreNom>\AppData\Local\wsl\{GUID}\ext4.vhdx`
>
> **:link: Accès rapide :** `\\wsl$\<DistroName>` dans l'Explorateur Windows.
>


---
