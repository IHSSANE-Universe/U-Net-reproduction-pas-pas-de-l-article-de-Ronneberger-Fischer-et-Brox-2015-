# synthèse de l'article U-Net

Synthèse et reproduction partielle de l'article *U-Net: Convolutional Networks for Biomedical Image Segmentation* (O. Ronneberger, P. Fischer, T. Brox, 2015, [arXiv:1505.04597](https://arxiv.org/abs/1505.04597)).


## Contenu du notebook

1. Architecture et arithmétique des tailles : une tuile de 572×572 donne une sortie de 388×388, avec 23 couches convolutives. Comptage des paramètres à la main (31 030 658 pour 1 canal d'entrée et 2 classes) et schéma du U.
2. Jeu de données synthétique de cellules qui se touchent (aucun fichier externe nécessaire).
3. Carte de poids de l'équation (2) de l'article, qui renforce les filets séparant les cellules voisines.
4. Déformations élastiques (grille 3×3, écart-type de 10 pixels).
5. Initialisation de He, comparée à deux autres écarts-types sur 30 couches.
6. Découpage en tuiles : test avec un « faux modèle », l'image est reconstruite exactement.
7. Implémentation PyTorch du U-Net, de la perte pondérée et de l'entraînement.
8. Évaluation par l'IoU.


## Prérequis

Python 3, NumPy, SciPy, OpenCV, Matplotlib et PyTorch. Tout est préinstallé sur Colab.


