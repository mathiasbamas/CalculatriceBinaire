# CalculatriceBinaire

## Objectif

L'objectif est de réalisé une calculatrice permettan l'addition ou la soustraction en 4 bits. La calculatrice est réalisé avec des portes logiques grace au logiciel *Logisim*.

- [x] Demi-Additioneur
- [x] Demi-Soustracteur
- [x] Additioneur
- [x] Additioneur/Soustracteur
- [x] Affichage 7 segments
- [x] Affiche erreur si un nombre est supérieur a 9
- [ ] Multiplication
- [ ] Soustraction

## Additionneur/Soustracteur 

**L'addioneur/Soustracteur** a pour but de renvoyer le resultat de l'addition ou de la soustration entre deux bits, ces dernier doivent respecter les **tables de verité** suivance 

| Additioneur                           |     
| A        | B       | R      | S       |     
| :------: | :-----: | :----: | :-----: |     
| 0        | 0       | 0      | 0       |     
| 0        | 1       | 0      | 1       |     
| 1        | 0       | 0      | 1       |  
| 1        | 1       | 1      | 0       | 

| Soustracteur                          |
| A        | B       | R      | S       |
| :------: | :-----: | :----: | :-----: |
| 0        | 0       | 0      | 0       |
| 0        | 1       | 1      | 1       |
| 1        | 0       | 1      | 0       |
| 1        | 1       | 0      | 0       |

On obtient alors sur logisim le circuit suivant 

### Demi Additioneur Soustracteur
![alt text](https://github.com/mathiasbamas/CalculatriceBinaire/blob/main/demi-AS.png "Demi Additioneur Soustracteur")

### Additioneur Soustracteur
![alt text](https://github.com/mathiasbamas/CalculatriceBinaire/blob/main/AS.png "Additioneur Soustracteur")

## Affichage 7 segments

Pour savoir quel segment allumé pour quelle valeur on a dressé dans un premier temps un tableau pour les segments indiquant leur affichage ou nom selon les valeurs des **4 bits** en entrée. 
Avec ce tableau on a ensuite dressé une **table de Karnaugh** pour chaque segment afin d’obtenir les conditions d’affichage de chaque segment en fonction des 4 bits en entrée En combinant les conditions de chaque segment on obtient le circuit pour l’affichage des nombres.

## Resultat 

Maintenant que nous avons toutes les parties du circuit principal il nous suffit de les assemblée On relie chaque chiffres qui composent les nombres a des input qui permettent de choisir une valeur en binaire (tout en affichant « E » si le chiffre choisi est supérieur a 9).
On relie le 1er bit du chiffre 1 au 1er bit du chiffre 2 dans l’additionneur/soustracteur et ainsi de suite tout en reportant la retenue de chaque additionneur/soustracteur au suivant.
On relie la retenue du dernier additionneur/soustracteur au premier additionneur/soustracteur de poids supérieur.
Le résultat de chaque chiffre passe par le circuit de retenue décimale pour enfin être affiché dans le résultat. 

### Circuit principal 

![alt text](https://github.com/mathiasbamas/CalculatriceBinaire/blob/main/circuitPrincipal.jpg "Additioneur Soustracteur")





