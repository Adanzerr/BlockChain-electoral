# BlockChain-electoral

Au cours de ce projet nous allons créer une blockchain qui nous permettra de simuler un principe électoral .Cette blockchain permettrait de voter à distance tout en garantissant l'intégrité, la sécurité et la transparence de l'élection. 
Au cours de ce projet nous avons implémenter un système de cryptographie avec un principe de clé publique et privée, crée et gérer une base centralisée de déclaration et manipuler une base décentralisée de déclarations ( Blockhain ) sous forme de structure d’arbre.

Les fichiers de notre projet sont repartis de la manière suivante : Partie1.c à Partie5.c avec respectivement leurs fichiers .h contenant le prototype des fonctions et des structures.Pour tester les 5 parties, il y a 5 fichiers tests exécutable grâce au Makefile ( make test1 et ./test1 pour le test1 par exemple) .

#  -Dans la partie 1 (fichier partie1.c ) :
nous avons traité la génération de nombres premiers, de clés publiques et de clés privées.

# -Dans la partie 2:
nous avons implémenter les structures représentant les clés, les signatures et une déclaration signée.
La structure Key est constituée de deux long(p et s), celle-ci peut être soit privée (utilisé pour signer la déclaration de vote) ou publique (attester l’authenticité d’une déclaration).

# -Dans la partie 3:
nous avons gérer des structures permettant de stocker les déclarations des votes des individus et leur clé sous forme de liste chainé simple.
Nous avons implémenté plusieurs fonctions pour gérer ces listes : des fonctions de création, de suppression et de lecture et d’affichage.

# - Dans la partie 4:
Pour décider du vainqueur de l'élection on utilise une structure Hascell qui vas permettre de créer 2 tables de haschage

Cette structure aura deux utilités :
-une qui permet de compter le nombre de voie pour chaque candidat compose de la cle publique du candidat et du nombre de voie comptabilisé pour celui-ci. 
-une qui permet de vérifier si une personne a déjà voté et si elle se trouve bien sur la liste électorale.

# -Dans la partie 5:
On a dédié cette partie à l'implémentation de la blockchain.
La blockchain qui aura une forme d’arbre est constitué de plusieurs block mis à jour régulièrement par les citoyens eux même en local.
