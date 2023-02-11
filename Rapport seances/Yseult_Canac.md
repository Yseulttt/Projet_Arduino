Rapport de séances d'Yseult Canac
==
Séance du 16 décembre :
-- 
* Schematisation de la maquette (voir photo)![Maquette](https://user-images.githubusercontent.com/120583392/208371088-4b3ca3a4-0e2e-434f-ba41-54d8d0e72067.jpeg)

* Début du code : Affectation des lasers aux I/O de la carte Arduino (laser1, laser2,laser3…), définition de ces I/O comme de entrée (INPUT) et affectation du résultat des entrées à des variables (l1, l2, l3…)

Séance du 6 janvier : 
--
* Carte mentale décrivant les fonctionalités de la compteuse 
* Recherche du code sur le composant écran LSD et intégration dans le code

Séance du 13 janvier : 
--
* codage de l’écran lcd qui désormais affiche : « Votre cagnotte : » + la cagnotte.
* insertion du micro servo moteur au code
Ci-joint l'avancée du code : [Code_Compteuse_Piece.ino.zip](https://github.com/Yseulttt/Projet_Arduino/files/10415652/Code_Compteuse_Piece.ino.zip)

Séance du 4 février :
--
* Codage de l'encodeur rotatif : On peut s'en servir pour choisir le montant que l'on souhaite récupérer. Le chiffre en question augment de 0.10€ à chaque impulsion et se bloque a 5€ qui est le montant maximum. Ensuite, en appuyant sur l'encodeur la valeur se bloque et est stockée dans une variable, qui sera utilisée dans la suite du code. 
* Complément du code de l'écran lcd (le montant a choisir s'affiche sur l'écran).

Séance du 11 fevrier :
--
* Integration de la division euclidienne qui permet de savoir combien de pièces de chaque type il faut rendre. Le but est de rendre le plus de grosses pièces possible pour avoir le moins de monnaie. (exemple pour les pièces de deux euros : On divise le montant à rendre par 2 et en prenant la partie entière de ceci, on obtient le nombre de pièces de 2€ à rendre. Ensuite, on attribue à la variable contenant le montant à rendre le modulo par 2 de lui même. Ceci permettra de diviser ce qui reste par 1 et ainsi de suite pour toute les pièces.).
* Rencontre d'un problème : on ne peut pas faire un modulo avec des doubles. J'ai donc trouver une autre manière de faire la division euclidienne. Il ne reste plus qu'à le coder...
* Branchements des IR sensors
* Rencobtre d'un autre problèmes : Il n'y a pas assez I/O sur la carte arduino UNO. On va donc utiliser une carte plus grande.
