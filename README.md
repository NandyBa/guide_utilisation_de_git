# Guide d'utilisation de Git


Git est un outil de versionning. Autrement dit c'est un outil qui vous permet:
- de conserver un historique des modifications de vos projets (pour y retourner si besoin).
- de travailler en parallèle (plusieurs collaborateurs peuvent avancer sur différents points d'un projet même sans risquer de  se gêner)
- de conserver des copies locales et distantes de vos fichiers pour travailler en remote et prévenir des pertes de données grâce à des backups

Très utilisé par les équipes tech. Il est aussi plébicité par d'autres professions notament lorsque dans leur quotidient nécessité de la modification de nombeux fichiers.

## Utilisation

### Initialisation d'un nouveau projet et première sauvegarde

Pour créer un nouveau projet Git rien de plus simple.  
Créer un nouveau dossier avec le nom de votre projet.  
Ouvrez un invité de commande et déplacez-vous dans ce nouveau dossier.  
Puis effectuez la commande suivante:

	git init

Ensuite faite vos premières modifications..
Lorsque vous souhaitez enregister vos modification.
Effectuer les commandes suivantes:

	git status
	git add .
	git status
	git commit -m "Mon premier commit"

La commande *git status* permet de consulter la liste des fichiers qui ont subit une modification depuis la dernière sauvegarde.

La commande *git add .* permet de selectionner tout les fichiers pour la sauvegarde. Vous pouvez aussi spéfichier le nom des fichiers à sauvegarder à la place du *point*.

ex:
	
	git add mon_excel.csv

ou encore avec plusieurs fichiers

	git add premier_fichier.txt deuxième_fichier.txt

La commande *git commit -m "Mon premier commit"* permet de sauvegarder les modifications. Après le -m vous pouvez spécifier le nom de votre modification. Attention n'oubliez pas les guilemets :) .

### Consulter l'historique des modifications

Essayer de faire plusieurs commit pour vous familliariser avec les commandes précédentes puis exécuter et la commande <code>git log</code> et observez le résultat.

Vous devriez voir apparaître l'ensemble des noms de vos derniers commit par ordre antidaté.
