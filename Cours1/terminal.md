![Partie 1](http://idata.over-blog.com/5/84/65/06/Chapitre-1.jpg)
______________________________________________________________

## **1. Le terminal**  
### **_1.1. Introduction_**  
Dans cette ressource, tu vas découvrir les bases du terminal, un outil très puissant qui permet de "parler" à son ordinateur. Nous allons voir les bases : comment intéragir avec le terminal, comment jouer avec ses premiers fichiers, et bien d'autres.    

#### **_1.1.1._ Ce que tu apprendre dans cette ressource**  
Voici la liste des questions auxquelles tu vas pouvoir répondre avec cette ressource :    

- Qu'est-ce que le terminal ?
- Que veut dire GUI et CLI ?
- Comment lancer un terminal ?
- Comment exécuter ses premières fonctions avec un terminal ?
- Pourquoi la notion de géographie est très importante dans un terminal ?
- Qu'est-ce que VIM et comment s'en servir ?  
## **1.2. Historique**  
Le terminal est ce que l'on appelle plus communément un interpréteur de commande (ou command-line interpreter (CLI) en anglais), est un outil qui permet d'interpréter les commandes qu'un utilisateur tape au clavier dans l'interface en ligne de commande.  

À la base, les ordinateurs tournaient sans interface graphique, donc les utilisateurs passaient exclusivement par les CLI. Avec l'arrivée des systèmes d'exploitation graphiques (Windows, Apple, Linux), le CLI n'a pas perdu en popularité, puisqu'il permet de faire des tâches extrêmement précises.

En gros, c'est une version texte de l'explorateur de fichiers : on peut ouvrir des dossiers, créer des fichiers, les lancer, les renommer, installer des programmes, et bien d'autres choses. On dit que c'est une **CLI** (Command Line Interface), comparée à la **GUI** (Graphical User Interface) de l'explorateur normal. Tout est fait via clavier, donc pas besoin de souris dans le terminal.

## **1.3. Le terminal**  
### **_1.3.1._** Qu'est-ce que le terminal ?
Le terminal est un outil intimidant aux premiers abords, mais au final se révèle pas compliqué. J'ai réalisé une vidéo qui explique le terminal : [Introduction au terminal][![Alt text](https://img.youtube.com/vi/VID/0.jpg)[](https://www.youtube.com/watch?v=myz_6xrDwR4)



### **_1.3.2. Comment le lancer ?_**
Sur Linux : CTRL + ALT + T
Sur macOS : CMD + SPACE, puis écrire Terminal (ou iTerm), Enter.

🚀**ALERTE BONNE ASTUCE**    
Si tu utilises Linux, passe ton terminal en anglais. Quand ce dernier te renverra une erreur, c'est bien mieux qu'elle soit en anglais. L'anglais et la langue d'internet, donc la majorité des gens qui ont eu ton problème vont le poster en anglais. Et ainsi tu auras 100 fois plus de résultats sur Google que si tu postais ton erreur en français.

### **_1.3.3. Premières fonctions ?_**
Pour faire marcher le terminal, rien de plus simple : il suffit de rentrer le texte correspondant à la fonction et cela s'exécutera. Par exemple si dans l'explorateur en GUI il suffit de double cliquer sur mon_fichier.txt pour l'ouvrir, il faudra faire dans le terminal open mon_fichier.txt (sur macOS) ou xdg-open mon_fichier.txt (sur Linux) pour l'ouvrir avec le terminal. On va tester avec notre première fonction :
______________________________________________________________
$ echo "Hello world !"
______________________________________________________________
(je commence toutes les commande du terminal avec un $, c'est une convention, et c'est plus facile à reconnaitre comme ceci)

Si tu exécutes cette commande le terminal devrait te renvoyer Hello world ! ([cette phrase est un grand classique de la programmation](https://fr.wikipedia.org/wiki/Hello_world)). Et là, tu viens d'exécuter ta première commande de terminal 🎉
Maintenant nous allons voir les premières commandes de base.  

### **_1.3.3.1. PWD_**
pwd est l'acronyme de Print Working Directory, une commande qui affiche le dossier dans lequel tu es actuellement.
______________________________________________________________
$ pwd
______________________________________________________________
Pour moi, pwd me renvoie :
______________________________________________________________
/Users/felix
______________________________________________________________
C'est comme dans l'explorateur en GUI, quand tu double-cliques sur felix, il te déplace dans le dossier felix qui est dans le dossier Users.

🚀**ALERTE BONNE ASTUCE**    
pwd est généralement la première commande que l'on tappe quand on arrive dans le terminal de quelqu'un : c'est idéal pour s'y retrouver ✌️   

### **_1.3.3.2. LS_**
ls est le diminutif pour list, cette fonction affiche les fichiers et dossiers qu'il y a dans mon dossier actuel.
______________________________________________________________
$ ls   
______________________________________________________________ 
Pour moi, ls me renvoie :  

______________________________________________________________
Applications/   Dropbox/     Music/       Desktop/
Pictures/     Documents/    Library/     Public/
Downloads/    Movies/  
______________________________________________________________
Dans le terminal, nous pouvons donner des options aux fonctions, en faisant $ fonction -option. Par exemple, je peux faire ls -a, ce qui a pour effet d'afficher aussi les fichiers commençant par un . (fichiers de devs en général), ou je peux faire ls -l pour afficher la liste au format long. Et je peux même combiner les deux en faisant ls -al pour afficher aussi les fichiers commençant par un ., tout au format long.

### **_1.3.3.3. MAN_** 
man est le diminutif de manual. Man lance un programme qui permet de lire la manuel d'une fonction précise. Pratique pour savoir toutes ses spécificités. Pour s'en servir il suffit de tapper : man fonction. Par exemple pour afficher le manuel de ls, je dois taper :
______________________________________________________________
$ man ls  
______________________________________________________________
Ce qui m'ouvrira son manuel, qui je peux quitter à tout moment en tapant q.

### **_1.3.4._** Où sommes-nous ?
Une notion **fondamentale** pour le terminal : la notion de géographie. Comme dans l'explorateur en GUI, on se déplace de dossiers en dossiers dans le terminal. Si jamais tu veux ouvrir un fichier en tappant open file.txt (sur macOS) ou xdg-open file.txt (sur Linux) et que tu ne te trouves pas dans le bon dossier, le terminal te renverra une erreur. Un peu comme si tu essayais de double-cliquer sur file.txt dans le mauvais dossier : impossible car il n'y est pas.   

Tu vas devoir te déplacer donc de dossiers en dossiers pour ouvrir et intéragir avec les bons fichiers.  

### **_1.3.5. CD_**  
cd est l'acronyme de Change Directory, qui te permet de naviguer entre dossiers. L'équivalent d'un double-clic sur un dossier en quelque sorte 😁  
______________________________________________________________
$ cd nomdudossier
______________________________________________________________
Tu te déplaceras dans le dossier nommé nomdudossier (s'il existe dans le dossier dans lequel tu te trouves).  
Tu peux aussi te déplacer vers le dossier parent en faisant $ cd ..  

🚀**ALERTE BONNE ASTUCE** 
Utiliser la touche TAB permet de faire de l'autocompletion, très pratique pour cette méthode. Aussi, faire cd + [ESPACE] + TAB + TAB affiche les dossiers disponibles.

### **_1.3.6. Autres fonctions_**  
### **_1.3.6.1. Créer un fichier_**  
En tapant :
______________________________________________________________
$ touch nomdufichier  
______________________________________________________________

Cela aura pour effet de créer un fichier qui s'appelle nomdufichier  

### **_1.3.6.2.Copier_**
Pour copier un fichier ou un dossier d'un endroit à un autre, il suffit de rentrer :  
______________________________________________________________
$ cp fichier_à_copier lieu_de_destination  
______________________________________________________________
### **_1.3.6.3. Déplacer_**    
Pour déplacer (couper) un fichier ou un dossier d'un endroit à un autre, il suffit de rentrer :  
______________________________________________________________
mv [fichier_à_déplacer] [lieu_de_destination]  
______________________________________________________________

**Protip** : mv est très pratique pour renommer un fichier. Imaginons que tu as créé un fichier "hello.rv" au lieu de "hello.rb". Oups, malheur. Heureusement, faire $ mv hello.rv hello.rb résoud ceci en quelques coups de clavier !

### **_1.3.6.4. Remove_**  
Supprimer un fichier :  
______________________________________________________________
$ rm nomdufichier  
______________________________________________________________
Il est possible d'effacer un dossier ainsi que son contenu en ajoutant la récursion en option :  
______________________________________________________________
$ rm -r nomdudossier  
______________________________________________________________

📚**INSTANT CULTURE GÉ**  
rm est à l'origine d'une blague vieille comme le monde. En effet, ajouter l'option -f permet de forcer la suppression d'un fichier, même s'il est important pour l'ordinateur, et finir par / ou * dit à votre ordinateur de prendre absolument tous les fichiers. Ainsi, si tu tapes $ rm -rf / ou $ rm -rf * dans ton terminal, tu dis à ce dernier de tout prendre et de tout effacer, en forçant. Et figure toi que rm est très rapide, et donc effacera l'intégralité de ton ordinateur en quelques secondes à peine. **À ne jamais jamais jamais faire** donc.

### **_1.3.6.5. Vim_**  
Vim est un des éditeurs de texte les plus respectés au monde. Comme il passe uniquement par le terminal, il se marie extrêmement bien avec cet outil. Et comme vim utilise exclusivement le clavier, ses raccourcis permettent d'aller extrêmement vite, pour qui ose grimper la très dure courbe d'apprentissage (quelques semaines à plein temps). De ce fait, je te montrerai vim pour ta culture générale, mais te demanderai de passer par un autre éditeur de texte 😉      
______________________________________________________________
$ vim nomdufichier  
______________________________________________________________

Permet d'ouvrir vim sur le fichier nomdufichier et de l'éditer. Pour quitter vim, il faut rentrer :q!.  

### **_1.3.7. Autres astuces_**    
CTRL + C annule la fonction en cours. Pratique quand on a une boucle infinie.

La casse est très importante, idem pour les espaces.

Il y a des raccourcis pratiques, par exemple CTRL + U efface la ligne en cours.

Les touches du haut et du bas permettent de naviguer dans l'historique des commandes. Très pratique pour par exemple re-éxécuter une commande que tu viens de faire.  

## **1.4. Les points importants**
Voici les points à retenir de la ressource :

- Pour lancer le terminal sur Linux : CTRL + ALT + T ; pour le lancer sur macOS : CMD + SPACE, puis écrire Terminal (ou iTerm), Enter.
- <span style="color: #fb4141">man</span> est le manuel est permet de lancer la manuel des fonctions
- pwd affiche le dossier dans lequel tu es actuellement.
- ls est une commande qui affiche les fichiers et dossiers qu'il y a dans mon dossier actuel
- la notion de géographie est fondamentale : le terminal n'arrivera pas à ouvrir les fichiers s'il ne se trouve pas dans le bon dossier
- cd permet de changer de dossier
- touch permet de créer un fichier
- cp permet de copier un fichier
- mv permet de déplacer un fichier ou un dossier
- rm permet de supprimer un fichier
## **1.5. Aller plus loin**
Voici un excellent [cours express](https://www.vikingcodeschool.com/web-development-basics/a-command-line-crash-course) pour avoir quelques base sur le terminal. Il est un peu similaire au mien, mais aborde d'autres sujets intéressants tels que le PATH.  

Viking Code School ont aussi fait un [cours sur le pimp de terminal](https://www.vikingcodeschool.com/web-development-basics/a-command-line-crash-course) pour avoir plein de couleurs de BGs sur le tien.  

Michael Hartl a fait une célèbre introduction au terminal nommée [Learn Enough Command Line to Be Dangerous.](https://www.learnenough.com/command-line-tutorial) Cette ressource permet d'aller assez loin en détails dans le terminal.  

Pour ceux qui veulent découvrir Vim, voici [une marche à suivre](https://medium.com/actualize-network/how-to-learn-vim-a-four-week-plan-cd8b376a9b85) pour être champion de Vim rapidement.  
