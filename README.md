# TP2MGL870

1. Objectif du laboratoire : L’objectif du laboratoire est d’implémenter un pipeline pour entraîner un modèle d’AiOPs pour la détection des anomalies.
 Le laboratoire a pour objectifs :

a. Sefamiliariser avec la manipulation des logs
b. Sefamiliariser avec les convertisseurs de logs (parseur) 
c. Comprendre les concepts de détection d’anomalie en utilisant l’IA. 
d. Sefamiliariser avec le développement de modèles AiOPs. 
e. Sefamiliariser avec l’évaluation de modèles de l’AiOPs. LogHub est une plateforme connue de logs disponibles pour expérimentation et recherche. 
Ces données sont disponibles à télécharger dans le répertoire Github suivant : https://github.com/logpai/loghub Pour l’objectif du laboratoire, choisissez deux projets de LogHub. Le résultat du laboratoire est une présentation, un rapport et un lien vers Github pour votre code. 

2. Compréhension des logs : La première étape est la compréhension de la structure des logs des deux projets que vous avez choisis. Expliquez en vos propre mots (vous pouvez utiliser des figures en cas de besoin) le format des lignes de logs, ce que les logs représentent (e.g., l’enregistrement de données), et comment identifier les différentes unités dans les logs (e.g., une unité peut être un thread, un job). Pour inspiration, je vous refère à l’explication des traces de Google Cluster : https://drive.google.com/file/d/10r6cnJ5cJ89fPWCgj7j4LtLBqYN9RiI9/view . À noter que vous n’êtes pas obligé de faire toute une documentation détaillée, juste quelques paragraphes ou schémas pour expliquer votre compréhension seraient assez suffisants.

3. Préparation des données : La deuxième étape consiste à convertir les logs en format numérique compréhensible par des modèles d’IA. Pour ceci, il faut convertir les instructions de logs en templates, ensuite en un ensemble d’événements. Pour ceci, il faut utiliser l’un des parseurs existant dans le répertoire suivant : https://github.com/logpai/logparser . Une fois les templates et les variables sont identifié, il faut transformer les séquences (varient selon les deux projets sélectionnés) en une matrice dont les colonnes représentent les événements (E1, E2, …, En) et les lignes représentent le nombre d'instances d’un événement dans la séquence d’événement.Décrivez dans votre rapport les étapes suivies, un aperçu des résultats obtenus et un lien vers votre répertoire Github pour la totalité des résultats, et référez chacune des étapes aux endroits du code qui les implémentent. Afficher certaines statistiques sur vos données. En particulier, des statistiques et distributions liés aux pannes (e.g., job failure or thread failure) selon les projets que vous avez choisis. Ceci est pour mieux comprendre vos données et le taux des anomalies dans vos données. Choisissez une manière de représenter les données visuellement (e.g., barplot).

4. Construction du modèle AiOPs : En utilisant le modèle de régression logistique (Logistic Regression) et la forêt aléatoire (Random Forest), entraînez deux modèles d’AiOPs et mesurer leurs performances en utilisant les métriques : Précision, Rappel et AUC. Choisissez et justifiez votre méthode d’évaluation. Avant d'entraîner les modèles, assurez vous d’éliminer les corrélations. Identifier le modèle le plus performant.


5. Interprétation du modèle AiOPs : Identifiez les variables (événements) les plus importantes pour la détection d’anomalie. Expliquez les résultats obtenus.
