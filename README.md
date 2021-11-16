# miner_du_muscleupcoin
Environnement WSL Windows

Toujours le même crédit à notre exccellent pjdecarlo comme notifié ici en début de readme sur le fork https://github.com/elestranobaron/muscleupcoin :

source https://www.hackster.io/pjdecarlo/how-to-make-a-cryptocurrency-using-litecoin-v0-15-source-fb5e82

On windows, the wallet will ask you where you wish to store the configuration data on first-run. By default this is stored in %AppData%/<YourCoin>. You will need to ensure that a valid .conf file from step 11 exists in that directory. See the "Get Started Guide for faithcoin" for more information.

On linux, a hidden directory is created in the user's home folder by the name of .<YourCoin>. You will want to ensure that a valid .conf exists in this directory before launching <YourCoin>-qt.

Le problème est qu'avec une version Debian à jour les paquets Berkeley pour la wallet sont trop récents, bien que tout ceci est mis en obsolescence par sqlite.
  
On utilise donc le script db4.sh qui va compiler la bonne librairie. Des difficultés au moment du patch peuvent être rencontrées c'est pour ça que c'est commenté dans le code je l'ai fait à la main il y a une dizaine de remplacements tout au plus.
  
Le fichier conf comme précisé plus haut est à coller dans le répertoire par défaut de la wallet, .coinname dans le home pour Linux.
  
Avec les paquets Qt5 et en suivant bien les etapes de compilations du core 1- autogen.sh 2- ./configure 3- ./make 4- ./make install il ne semble pourtant pas y avoir trace de la wallet qt. Donc on lance ça à la main: 1- lancement du <yourcoin>d. 2- ./mining.sh
  
et ça mine !


