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

L'addioneur/Soustracteur a pour but de renvoyer le resultat de l'addition ou de la soustration entre deux bits, ces dernier doivent respecter les tables de verité suivance 

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




