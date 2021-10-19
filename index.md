<style>
img
{
    display:block;
    float:none;
    margin-left:auto;
    margin-right:auto;
    width:60%;
}
</style>

## Analyse Topologique de données sur le site de Gallica: une ethnographie numérique

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
4. Obtenir des clusters avec la méthode Kmeans

Information sur les clusters:
![clusterinfo](https://user-images.githubusercontent.com/49370075/137926384-df53c9ea-d368-42a7-a1c0-ddde4c6ccb6a.png)
![clusterinfo1](https://user-images.githubusercontent.com/49370075/137926393-93fc17d8-da71-4051-9e43-6aa9a38c22f3.png)


Exemple de clusters:
![cluster0](https://user-images.githubusercontent.com/49370075/137926304-f54e6599-8f2c-4802-a340-d7fdb06498b3.png)
![cluster1](https://user-images.githubusercontent.com/49370075/137926326-df4e5c6f-3cab-43e5-ac79-9eff35ff9508.png)
![cluster2](https://user-images.githubusercontent.com/49370075/137926337-0c2fb684-9e2d-4f71-85af-769e0795b5e3.png)
![cluster4](https://user-images.githubusercontent.com/49370075/137926348-6dd24605-0e2c-40ac-a8b7-812c52a48056.png)
