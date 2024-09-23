# Analyse temporelle de méthodes de tri

## Introduction

Ce document donne une comparaison des tris suivants:
- Tri **séléction**
- Tri **insertion**
- Tri **rapide**
- Tri **fusion**

## Méthode

Pour mesurer le temps d'exécution des algorithmes, nous utilisons la bibliothèque Python `timeit` afin d'exécuter plusieurs fois chaque fonction de tri avec des listes de tailles croissantes générées aléatoirement. Chaque fonction est exécutée 100 fois, et le temps moyen est calculé pour chaque taille de liste `n`.

Les listes testées sont de tailles croissantes allant de 1 à 500 éléments. Voici les algorithmes testés :

- **Tri sélection** : Algorithme peu efficace pour les grandes listes. Il parcourt la liste pour trouver le plus petit élément à chaque itération.
  
- **Tri insertion** : L'algorithme insère chaque nouvel élément à sa place dans une liste déjà triée.

- **Tri rapide** : Un des algorithmes de tri les plus efficaces. Partitionne la liste et tri chaque sous-liste.

- **Tri fusion** : Division de la liste en sous-listes plus petites, puis fusion une fois triées.


## Comparaison des résultats

![Figure 1](./images/Figure_1.png)
*Figure 1 : Graphique comparant les temps d'exécution des différents algorithmes de tri pour des listes de tailles croissantes. Pour 100 essais et n=10*

![Figure 2](./images/Figure_2.png)
*Figure 2 : Graphique comparant les temps d'exécution des différents algorithmes de tri pour des listes de tailles croissantes. Pour 100 essais et n=100*

![Figure 3](./images/Figure_3.png)
*Figure 3 : Graphique comparant les temps d'exécution des différents algorithmes de tri pour des listes de tailles croissantes. Pour 100 essais et n=500*

## Comparaison avec la méthode sort

![Figure 4](./images/Figure_4.png)
*Figure 4 : Graphique comparant les temps d'exécution des différents algorithmes de tri pour des listes de tailles croissantes, avec la courbe de la méthode sort incluse Pour 100 essais et n=500*

## Conclusion

Avec les résultats, nous pouvons voir que :

- Le tri sort est le plus performant, avec une valeur temporelle proche de 0 (Figure 4)
- Des 4 algo, le tri insertion semble être plus efficace pour une petite liste (Figure 1)
- L'algorithme de tri rapide est plus efficace que les tris fusion, sélection et insertion pour des listes de taille moyenne à grande.