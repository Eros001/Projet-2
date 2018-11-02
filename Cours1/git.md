2. Git et GitHub
2.1. Introduction
Ce cours t'introduira à Git et Github, deux fantastiques outils qui permettent de faire des sauvegardes efficaces d'un projet, et de travailler à plusieurs sur le même dossier.

Dans cette leçon, nous allons te montrer comment installer Git, comment s'en servir, et comment le faire marcher. Pour ceci, nous allons nous aider de l'excellent cours sur OpenClassrooms de Marc Gauthier, sur Git et GitHub.

2.1.1. Ce que tu vas apprendre dans cette ressource
2.2. Historique
Git est un outil de versionning de code, c'est à dire que c'est une commande qui permet de faire des sauvegardes, avec commentaires d'un projet. Ainsi, il est facile de revenir d'une version de sauvegarde à l'autre, et c'est même optimisé pour les projets où tout le monde travaille sur le même fichier !

En gros, c'est la même chose quand vous faîtes une grosse présentation PPT. Vous faites tellement de modifications dessus que vous vous retrouvez à la fin avec le nom "VF_avec_retours_Jean01_final.ppt". Le versionning vous permet d'avoir toutes les versions sauvegardées, et de revenir à celles que vous voulez à tout moment, et de nous éviter ces tracas.

Voilà à quoi Git sert : à mieux gérer ses versions entre les fichiers d'un projet (bonus : Git marche pour tous les fichiers d'un dossier concerné, donc c'est encore plus puissant que CTRL + S). Et GitHub permet de mettre en ligne ton projet, comme ça vous pourrez travailler facilement en équipe dessus.

Pour information, Git a été créé en 2005 par Linus Torvald, qui a (entre autres) créé le système d'exploitation Linux.

2.3. Le cours
2.3.1. Installer Git
Avant de pouvoir se servir de Git, il faut l'installer. Cela tombe bien, il y a un chapitre éponyme dans le cours sur OC.

2.3.2. Première introduction à Git
J'ai fait une petite vidéo d'introduction à Git, que tu pourras retrouver ci-bas :




Ensuite, tu peux suivre le cours de Marc Gauthier jusqu'à la partie Récupérez des modifications. Nous verrons dans la formation THP comment faire les branches et autres joyeusetés 😇

2.4. Points importants à retenir
2.4.1. Les commandes pratiques
Voici un récap des commandes de base :

$ git init : il faut TOUJOURS commencer par initialiser git avec cette commande. Avec cette commande, le répertoire courant est considéré comme un repository git
$ git add [fichier] : ajoute aux sauvegardes le fichier mentionné. Protip : si tu as plusieurs fichiers à ajouter, tu peux utiliser $ git add . qui ajoute au repository tous les fichiers du dossier
$ git commit -m [commentaire] : créé un commit (commit = sauvegarde suivie d'un commentaire).
$ git status : te dit le status actuel de git.
2.4.2. Lire l'historique
$ git log : permet de voir l'historique et de voir tous les commits. Les commits sont rangés avec :

SHA : liste de chiffres et lettres qui indentifient de façon unique le commit.
Auteur
Date
Message donné durant le commit : avec ce message, tu vas comprendre ce que faisait le commit. C'est pour cela qu'il est important d'avoir un bon nom.
Pour quitter le log, il faut appuyer sur Q.

2.4.3. Se positionner sur un commit donné
Imaginons que veut vérifier un truc sur un vieux commit. On va utiliser la commande $ git checkout, utilisée comme ceci :

$ git checkout 45581cebdd2cae494f80f44010af9e4a86c9b8fa : on dit à git de se positionner sur ce sha précis.
$ git checkout master : une fois que l'on a fini de se balader, il faut revenir à la version présente de notre repository avec cette commande
⚠️ ALERTE ERREUR COMMUNE
$ git checkout ne marche que si tu n'as pas de modification non sauvegardée. Si tu es entre deux commits, git checkout ne marchera pas. Du coup il te faudra soit faire une sauvegarde (== faire un commit), soit effacer tout pour revenir au commit d'avant.

$ git checkout n'est pas une commande pour revenir en arrière et faire des modifications sur les anciens commits. Si tu fais ça, tu vas te retrouver avec une erreur qui a donné lieu à l'un des threads les plus célèbres de Stack Overflow. Pour tout effacer et revenir en arrière, le chapitre suivant sera là pour toi.

2.4.4. Revenir en arrière
J'ai fait des trucs, mais cela ne me convient pas. Comment revenir sur en arrière ? (inspiré par cette excellente réponse de Stack Overflow)

2.4.4.1. Effacer pour revenir au commit d'avant
La fonction $ git reset --hard permet de revenir au commit précédent, en effaçant tout. C'est une commande pratique quand on veut essayer de nouvelles choses à la volée, puis de revenir en arrière comme si de rien n'était ✌️

2.4.4.2. Tout effacer et revenir à un ancien commit
On peut faire ceci avec : $ git reset --hard 45581cebdd2cae494f80f44010af9e4a86c9b8fa, avec 45581c le SHA sur lequel tu veux revenir.

2.5. Pour aller plus loin
Au vu des apologies que l'on lui donne, le cours de OpenClassrooms sur Git est un très bon point pour aller plus loin. Il explique notamment la notion de branches et de fusions.

Aussi, voici un cours sur Git de la Viking Code School. Il explique bien les bases de Git et est une bonne alternative au notre.
1. Introduction
Ce projet te permettra de mettre en avant ce que tu as vu sur le terminal, Git, et Github. C'est un projet assez simple, mais qui te permettra de te faire découvrir l'univers du code avant de passer à la suite. Il sera pas à pas, c'est à dire que nous allons t'accompagner lors de ce projet.

Dans ce premier projet, tu vas créer ton premier repository le mettre en ligne sur GitHub, et intéragir avec à partir de ton ordinateur. Oh yeah !

2. Le contenu du projet
2.1. Créer le repo sur GitHub
Si ce n'est pas fait, va créer un compte sur GitHub, puis va créer un nouveau repository.

Au moment de la création, GitHub te demandera :

le Repository name : donne-lui un nom du genre git-thp
une description, optionnelle : laisse-la vide
s'il sera public ou privé : public (sauf si tu as envie d'upgrade ton compte et le rendre privé)
si tu veux initialize with a README : non, nous allons l'ajouter à la main
📚 INSTANT CULTURE GÉ
Un README est un fichier que l'on retrouve toujours dans un repository Git. Il permet à une personne qui débarque sur le projet de mieux le comprendre, de voir comment il marche, d'avoir une documentation exhaustive. Par exemple, tu peux voir ici la page de React JS, un framework de JavaScript, avec son README qui explique ce que fait React JS. Dans ce premier dossier, le README sera juste un texte pour dire que c'est un projet d'introduction à GitHub, Git, et le terminal.

Une fois ceci fait, tu devrais arriver à une page incompréhensible comme celle-ci : 
![](https://www.thehackingproject.org/assets/git-1-e32560080d19aaf7a421d18f47f411d64ff940ccece7dbe06e48252337c0ea2b.jpg)
Cette page te dit juste que ton repository est prêt, mais vide et prêt à être couplé à un dossier sur ton ordinateur. Nous allons donc prendre ce repo, puis le mettre sur ton ordinateur.

Comme tu es le propriétaire de ce repo, tu as juste à le cloner, et tu pourras travailler dessus facilement. Avec ton terminal, positionne-toi dans un dossier qui contiendra les projets de THP, puis créé le dossier de ce premier projet avec mkdir. Va à l'intérieur avec la commande cd.

Une fois à l'intérieur, te voici prêt à cloner ton repo vide. Pour ceci, tu peux utiliser la fameuse commande git clone :

$ git clone https://github.com/ton_username/le_nom_de_ton_repo
Et voilà, tu as ton premier dossier, lié à un repo GitHub. À partir de là, tu pourras faire des commits, et push ces commits sur le repo GitHub.

2.2. Travailler sur le projet depuis ton ordinateur
Bon tu as ton dossier, et si l'on lui donnait un peu de pep's ? Il est vide, on va commencer par faire un README pour expliquer ce que notre dossier fait.


🤓 QUESTION RÉCURRENTE
Mais dis-donc Jamy, pourquoi je ne dois pas faire git init, qui est en théorie LA première commande à faire dans tout nouveau repo ?
Excellente question chef, on voit que tu suis ! Git init sert à dire à ton ordinateur "hey bro, ici je vais avoir un dossier qui sera git, donc je vais faire des sauvegardes fréquentes", mais comme tu as fait un clone, ton ordinateur sait déjà que c'est un dossier git. Donc pas besoin de faire git init.

2.2.1. Création du premier fichier
Avec la commande touch, crée un nouveau fichier qui s'appelle README.md. Ouvre-le avec open (sur macOS) ou xdg-open (sur Linux), ce qui devrait lancer un éditeur de texte bidon (on verra demain comment installer des éditeurs de texte de grand BGs pour faire du code de BG), écris-y les lignes suivantes :

Ceci est mon tout premier repo GitHub, waow !
2.2.2. Ajout du premier fichier
Si tu fais la commande git status, ton ordinateur devrait te dire un truc du genre : "hey ! je suis sur la branche master, sur le premier commit, et j'ai remarqué qu'il y a un nouveau fichier qui s'appelle README.md. Ce fichier n'est pas répertorié dans le dossier git quand tu fais des sauvegardes, donc fais git add si tu as envie que je le prenne en compte lors de ton prochain commit !". Trop cool, on va donc ajouter ce fichier avec git add.

2.2.3. Premier commit
Une fois que tu as ajouté ton fichier avec git add, tu peux refaire git status, et tu auras un écran similaire, mais différent. Là, ton ordinateur te dire "hey ! Je suis sur la branche master, sur le premier commit, et tu as au moins un fichier ajouté au dossier git qui est différent au précédent commit, si tu fais un commit, ce fichier sera sauvegardé !". Je te laisse faire ton premier commit avec la commande git commit. Comme commentaire, nous te conseillons "Ajout du README", qui est explicite.

Si tu fais $ git log, tu pourras voir l'historique de tes différents commits. Si tu as bien fait le commit précédent, tu devrais le voir affiché dans ton historique.

🎨 EXEMPLE ILLUSTRÉ
Là tu dois te demander la différence entre add, création de fichier, commit, et c'est vrai que l'on s'y perd. Nous allons prendre une analogie : imagine que ton projet représente une soirée, et chaque fichier correspond à une personne présente à la soirée. Git te sert de capturer des photos de la soirée, et de savoir précisément qui tu vas prendre en photo.

Les gens sur la photo
Des fois des personnes vont arriver dans la soirée (création de fichier), mais il faut dire à ton ordinateur que tu veux les prendre en photo, tu vas donc utiliser git add pour choisir qui tu vas prendre en photo. Des fois certains fichiers ne seront pas prêts pour la photo, ils seront différents par rapport à la dernière photo, mais tu ne veux pas les capturer. Quand tu feras git status, ils seront untracked, mais tu veux les laisser tels quels et ajouter d'autres fichiers avec git add.

Prendre la photo
Une fois que ton cadre est prêt et tu as bien les personnes que tu veux prendre en photo, tu peux faire git commit pour prendre la photo, avec un joli commentaire "la bande à féfé".

Tu pourras prendre une autre photo avec d'autres fichiers en faisant git add, et git commit.

2.3. Mettre ton projet en ligne
Maintenant que tu as fait ton premier commit, nous allons mettre tout ceci en ligne, et admirer le travail bien fait.

Pour ceci, rentre la commande $ git push origin master, et Git devrait te le mettre en ligne. Si tu vas sur la page de ton projet du genre : https://github.com/ton_username/le_nom_de_ton_repo, tu devrais avoir le dossier à jour, avec un super README.md !

🤓 QUESTION RÉCURRENTE
Mais dis-donc Jamy, tu me perds, ça veut quoi "Git push origin master" ?
Cette commande utilise 4 mots que nous allons décortiquer :

git : tu utilises le programme git de ton terminal. Jusqu'ici, tout va bien
push : tu fais un push, c'est à dire que tu vas pousser ton projet..
origin : .. à la remote origin de ton projet. En faisant git clone, tu as mis ta remote origin par défaut au dossier GitHub, mais tu aurais pu push vers ta remote genesis, ou ta remote my_super_name_cool. Tu peux voir tes remotes en faisant $ git remote -v.
master : sur la branche master
Ainsi, si tu avais fait $ git push heroku other_branch, tu aurais fait un git push dans ton remote heroku sur la branche other_branch.

2.4. Ajouter un fichier
Maintenant, ajoute un nouveau fichier nommé kikou.txt, ajoute-le à ton repository, fais un commit, puis push le tout sur ton remote origin. Confirme que cela a été fait en allant sur ton repo GitHub et en actualisant.

2.5. Apprécier le travail bien fait
Pfiou, c'était un beau projet ! Et bien figure toi que tu viens de finir ta première journée d'introduction au code, dans laquelle tu auras vu de belles choses :

Le terminal, et comment s'en servir
Comment gérer son projet comme un pro avec Git
Mettre son projet en ligne avec GitHub
Demain nous allons te montrer les bases de HTML/CSS, puis nous allons te demander de mettre en ligne un site, pour que la terre entière le voit. Trop cool ! Évidemment, le code de ton site sera géré comme un pro grâce à Git et GitHub.

2.6. Le shell-enge
La meilleure façon d'apprendre, c'est par la pratique. Si jamais tu veux aller plus loins dans le monde du développement, il te faudra manipuler le terminal à la perfection. Ainsi, pour t'aider à t'améliorer, nous allons te demander de faire le shell-enge.

Pendant toute cette semaine, toutes les actions de ton ordinateurs devront être faite avec le terminal, et aucune avec l'explorateur habituel. Par exemple si tu dois bouger un fichier d'un dossier à un autre, tu devras le faire avec le terminal.

Au début cela peut paraitre assez inutile, puisque tu vas prendre pas mal de temps pour chaque action, mais c'est une chose remarquable pour apprendre très rapidement à se servir du terminal. Je t'invite à faire plein de recherches Google pour connaitre les fonctions qui remplacent les fonctions de base de ton explorateur.

3. Pour aller plus loin
Cette partie est optionnelle, mais te permettra d'approfondir ton niveau des projets du jour.

Pour aller plus loin, nous allons te demander de refaire le projet ci-haut depuis le début, en ne lisant pas la marche à suivre décrite plus haut. Voici ce que tu devras faire :

Créé un repository sur Github, puis importe-le sur ton ordinateur
Crée un fichier README.md puis commit et push le sur GitHub
Créé un fichier kikou.txt puis commit et push le sur GitHub
4. Rendu attendu
À la fin de la journée, tu devras avoir :

Un repository GitHub dans lequel tu as deux fichiers : un fichier README.md et un fichier kikou.txt
