---
Note: 4.8
Chapitre: 2 - Portes logiques
DateDeRetour: 2023-10-17
---
**Groupe :** numéro 11   
**Auteurs :** Piemontesi Gwendal, Trüeb Guillaume   
**Date :** 19 octobre 2023
***
## QUESTION 1
Le "bit de carry" dans un additionneur binaire est un bit qui indique s'il y a une retenue (carry) provenant de la somme des bits inférieurs lors de l'addition. Il est important dans l'addition de nombres car il permet de gérer les dépassements de capacité. Lorsque deux bits sont ajoutés et que le résultat dépasse la capacité d'un seul bit, le bit de carry est activé pour indiquer que la retenue doit être prise en compte lors de l'addition suivante des bits supérieurs.

## QUESTION 2
Le `modular sum` est utilisé pour calculer le checksum en additionnant les données sans tenir compte des retenues (carry) et en prenant ensuite le complément à deux du résultat. Voici les 3 étapes du `modular sum`:

1. Additionnez les données bit par bit sans considérer de retenues.
2. Si le résultat de l'addition dépasse la valeur maximale, ignorez simplement les retenues et conservez les bits les moins significatifs du résultat.
3. Prenez ensuite le complément à deux du résultat en inversant tous les bits et en ajoutant 1 au résultat inversé.

## QUESTION 3
La valeur de checksum attendue est 5.
$0xF0$ -> 1111 0000
$0x0F$ -> 0000 1111
$0xFC$-> 1111 1100
Addition sans carry -> 1111 1101
Complement à deux -> 0000 0101

## QUESTION 4
![A](../../../S0/PiecesJointes/Pastedimage20231015183438.png)

- La sortie VerifyIntegrity passera à 1 lorsque le calcul du checksum correspondant aux données d'entrée sera correct. Cela signifie que les données n'ont pas été altérées pendant la transmission.
- Si la sortie VerifyIntegrity reste à 0, cela signifie qu'une altération des données a été détectée, car le checksum calculé ne correspond pas aux données d'entrée.

