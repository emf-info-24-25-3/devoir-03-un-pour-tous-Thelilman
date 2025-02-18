## REPONSES :
1. Peut-on modifier l'âge d'un chien une fois qu'il a été créé (essayez de donner 10 ans à chien3 pour vérifier) ? 

oui , on peux le modifier faut juste pas dépasser la limite du int

2. Que se passe-t-il si on modifie le nom de chien2 ?

on ne peut pas , ça va crée une erreur

3. Pourquoi tous les chiens ont tous le même nom ?

ils ont tous le même nom mais sont différent , ils ont tous "new chien" mais on des nom différent . ( chien1 , chien2,chien3,...)

4. Observez avec attention les lignes N°20 à N°26 du main() et réfléchissez : par quel miracle le chien3 à la ligne N°26 s'affiche correctement ?
   Répondez à cette question en expliquant avec précision ce qui se passe et pourquoi.

Le truc qui fait que chien3 s'affiche correctement, c'est que tu as surchargé la méthode toString() dans la classe Chien. En Java, quand tu essaies d'afficher un objet, la méthode toString() est automatiquement appelée.

Là où ça devient intéressant, c'est que même si nom est un attribut statique, la méthode toString() est appelée sur l'objet chien3. Du coup, comme tous les chiens partagent le même nom statique, c'est cette valeur commune qui est affichée. Donc, si tu modifies le nom d'un des chiens (comme dans la question 2), tous les chiens afficheront ce nouveau nom.

En résumé, chien3 s'affiche correctement parce que la méthode toString() génère l'affichage en utilisant le nom statique et l’âge spécifique de l'instance. Mais comme nom est statique, tous les chiens auront toujours le dernier nom défini.
 

