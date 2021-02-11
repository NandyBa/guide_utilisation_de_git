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

Voici par exemple le résultat de <code>git log</code> sur du tutoriel que vous êtes en train de lire. 
<img src="assets/img/Consulter l'historique des modifications - git log.png">


### Les branches, vive la parallélisation

Jusqu'à présent toute des modifications que vous avez fait l'ont été à la suite les unes des autres dans un même historique. Mais imaginons maintenant que vous devez tester un nouvelle fonctionnalité pour votre projet que vous n'êtes pas sûr de garder.

Au lieu d'ajouter cette fonctionalité dans votre projet puis de devoir faire marche arrière et d'être dans la nécéssité de se rappeler de toutes les modifications que vous avez fait pour revenir à votre version avant modification avec Git vous avez à effectuer 2 commandes.

1. Crée une nouvelle branche

		git checkout -b nom_branche_nouvelle_fonctionalité

2. Effectuer vos modifications et vos commits

	Si vous voulez revenir à votre version antérieur à vos dernières modifications exécutez simplement la commande suitante:
	
		git checkout master

La commande <code>git checkout nom_de_la_branche</code> permet de se rendre sur une branche déjà existante

Si vous ajouter le paramètre <code>-b</code> cela vous permet de créer une nouvelle branche à partir de votre historique de commits actuel.

Pour consulter la liste des branches que vous avez créer vous pouvez utiliser:

	git branch
La branche qui apparaît en surbrillance est votre branche de travail.

Bien entendu vous pouvez créer plusieurs branches secondaires à partir d'une même branche.


**Supprimer une branche**

	git branch -d nom_de_la_branch_a_supprimer
Attention avant de supprimer une branche d'être sûr de plus en avoir besoin.
A noté que Git sauvegarde vos fichiers non pas un par un mais commit par commit. Par conséquent plusieurs version d'un même fichier sauvegardé avec Git prend au final moins de place sur votre disque que ces versions sauvegardées hors projet Git.
