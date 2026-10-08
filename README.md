Dev 1 : RIBBE Jules

Dev 2 : TORCHIN Maxence

Dev 3 : MEJEAN Oriane

![CFG](./CFG.png)

### Question 7

Certaines métriques de Halstead peuvent remettre en question leur validité car Halstead distingue les opérateurs et les opérandes, cette différence cause des résultats différents lors des comptages.
C'est pour cette raison que la validité peut être remise en question.

### Question 8
1. modification de la fiche de calcul
2. Les poids sont attribués de manière arbitraire en se basant sur différentes métriques, telles que la complexité, dont l’évaluation peut notamment s’appuyer sur les dépendances, le temps d’exécution, ...etc.

### Question 11
```C++
/*
 * Auteur : MEJEAN Oriane, RIBBE Jules, TORCHIN Maxence
 * Date : 08/10/2026
 * Description : Implémentation de l'algorithme QuickSort mais simplifiée.
 */
void iqsort0 ( int *a , int n )
{
    int i , j ;
    // Clause de guard : Si le tableau contient au plus un élément, il est déjà trié.
    if ( n <=1) 
        return;
    
    // Parcours le tableau pour séparer les éléments inférieurs au pivot de ceux qui lui sont supérieurs ou égaux.
    for ( i = 1 , j = 0; i < n ; i ++)
        if ( a [ i ] < a [0])
            swap (++ j , i , a );

// Place le pivot à sa position
swap (0 , j , a );
// Tri récursif de la partie située avant le pivot.
iqsort0 (a , j );
// Tri récursif de la partie située après le pivot.
iqsort0 ( a + j +1 , n -j -1);
}
```