## Analyse Topologique de données sur le site de Gallica:     une ethnographie numérique

### 1. Comment tracer une cartographie des disciplines en fonction des parcours des usagers?

word2vec embedding = méthode par réseaux de neurones qui permet de vectoriser les disciplines donc d’inférer espace métrique des disciplines où “mots” = disciplines et “phrases” = parcours

ex. Parcoursdisc = (Disc1; Disc2; Disc3; Disc2; …)

=> distances entre paires de disciplines -> génère un espace à environ 200 dimensions


{% include PCATSNE.html width="50" height="50" %}

### 2. Identifier divers types de parcours au sein de cet espace conceptuel

Classification des parcours par analyse topologique :
1. Tracer les parcours dans l’espace inféré précédemment
2. Calculer le diagramme de persistance pour chaque parcours i.e. extraire ses 
caractéristiques topologiques (si c’est droit, tortueux, s’il y a des cycles, si c’est concave 
ou convexe, si c’est très localisé ou très étendu)
3. Calculer les distances topologiques entre paires de parcours (entropie de persistance)
4. Cluster

Exemple de clusters:
