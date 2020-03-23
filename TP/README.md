# Instructions:

- Le TP doit se faire par équipes de quatre à cinq personnes. Dans certains cas spécifiques où il est impossible de former des équipes d'au moins quatre personnes, une exception peut être accordée pour former des équipes plus petites. Si tel est votre cas, veuillez m'écrire (meraihi.noureddine@uqam.ca) pour obtenir mon approbation. 

- Vous êtes autorisé à discuter du contenu du TP avec des personnes d'autres équipes. Toutefois, les solutions doivent être conçues séparément. Les copies des fichiers de solutions (rapport `pdf` et code `R/Python`) des différentes équipes doivent être rédigées séparément. Le plagiat est formellement interdit. Veuillez vous référer à la politique de l'UQAM en matière de plagiat si vous n'êtes pas sûr de bien comprendre ce qu'est le plagiat.

- Un bonus de 10% est accordé à l'équipe ayant le meilleur modèle prédictif (voir le détail plus bas)
- Un autre bonus de 10% est accordé à l'équipe présentant un rapport exemplaire, donc un rapport clair dont le format d'un article scientifique.

* La date limite pour remettre votre mission est le jeudi **7 mai 2020 à 23h59**.

* Un fichier zip ".zip" doit être remis par courriel. Ce fichier doit contenir (exactement):
1. Un rapport `.pdf` ou `.html` d'un maximum de 5 pages du style _notebook_ fait par [rmarkdown](https://rmarkdown.rstudio.com/) ou [Jupyter Notebook](https://jupyter.org/) contenant 3 sections:
    1. Une section appelée "Statistique descriptive", dans cette section (maximum 2 pages), on vous demande de faire quelques statistiques descriptives sur ce que vous remarquez/constatez sur les données que l'on vous fournit.
    2. Une section appelée "modélisation". Dans cette section, vous allez choisir **trois modèles**. Je peux aussi accepter un GLM et deux modèles vus dans le cours. Pour chaque modèle, vous allez créer une sous-section où vous expliquez pourquoi vous pensez que ces modèles sont susceptibles de donner de bons résultats (un court paragraphe). Dans chacune des sous-sections, après avoir expliqué brièvement vos arguments du choix du modèle, vous allez ensuite appliquer ces modèles sur votre base de données (je veux voir le code `R` ou `Python` qui permet d'exécuter chaque modèle).
    3. Une section appelée "modèle sélectionnés": dans cette section (pas plus qu'une page), on vous demande de sélectionner votre meilleur modèle parmi les trois modèles sélectionné précédemment. Le plus important est de montrer la technique la plus appropriée qui vous permet de choisir votre modèle. Par exemple, le MSE n'est le plus approprié à ce type de données à cause de la sudisperssion (beaucoup de 0 dans votre variable réponse `95%`).
2. Un seul fichier ("TP.R" OU "TP.py") qui contient le code `R/Python` intégral nécessaire pour exécuter toutes les expériences qui mènent à vos réponses.


    
- Assurez-vous que votre code est propre et clairement écrit. Des points peuvent être déduits si la clarté est jugée insuffisante. Cela inclut l'insertion de commentaires dans votre code R pour en assurer la lisibilité.
- Assurez-vous que votre code s'exécute sans aucune erreur. Donc au début de votre code, indiquez quelle version de `R/Python` que vous avez utilisé. Et surtout, assurez-vous de montrer clairement quel _package_ on doit installer ou importer afin que le code s'exécute comme il faut.

- Le fichier zip doit m'être envoyé par email avant la date limite. 
- Justifiez toutes vos réponses et présentez l'intégralité du raisonnement qui a conduit à vos réponses.
- Assurez-vous que les noms de tous vos coéquipiers et leur code permanent sont inscrits sur la première page de votre rapport.

# Problème à résoudre:

Votre mission est très simple puisque les données sont déjà toutes nettoyées; vous avez des données d'un assureur automobile canadien qui contiennent des informations suivantes:
- Les informations du conducteur principal du véhicule
- Des informations sur le véhicule
- Des informations sur les habitudes de conduite du conducteur principale `[variable_1, ..., variable_97]`
- Le **nombre de sinistre** `nb_sinistre` observé sur la durée de période de couverture du contrat d'assurance.
Vous devez appliquer **trois modèles** (tel qu'expliqué dans les instructions) qui vous permettent de prédire le mieux possible le nombre sinistre.

Vous avez un total de 60000 observations (assurés) sur laquelle vous allez travailler. J'ai gardé une bonne partie des données (environ 30000 observations) à laquelle vous n'avez pas accès afin de mesurer la performance votre modèle. Un bonus de 10% est accordé au meilleur modèle.
