## __*GitHub*__

## 1 Présentation 
### 1.1 GitHub
*Plateforme collaborative* pour dev, plus grand espace de stockage de travaux collaborative dans le monde! GitHub en lui-meme m'est plus rien de plus q'un reseau social comme fb. Vous construisez un profil, vous y deposez des projets à partager et vous vous connectez avec d'autre utilisateurs en suivant leurs comptes. Meme si la plupart des utilisateurs y deposent des projets de programmes ou de code, rien ne vous empeche d'y placer des textes ou tout type de fichier à présenter dans vos repertoires de projets.
### 1.2 Git
Git est un *logiciel de controle de version*, ce qui signifie qu'il gere les modifications d'un projet sans écraser n'importe quelle partie du projet.


## 2 Lexique de de Git et GitHub
### 2.1 Vocabulaire
**ligne de commande**: En gros: le programme de l'ordinateur que nous utilisons pour entrer des commandes Git. Dans le monde UNIX, on dit qu’on travaille en “ligne de commande” pour désigner le fait d’interagir avec un système informatique en entrant des lignes d’instructions textuelles dans un terminal, et non à l’aide d’une interface graphique. Les commandes tapées dans le terminal sont interprétées par un Shell. [Doc: Journal du Net ](https://www.journaldunet.fr/web-tech/dictionnaire-du-webmastering/1445276-commande-informatique-definition-precise-et-exmples/)

**Depot**: Un repertoire ou de l'espace de stockage ou vos projets peuvent vivre.Les utilisateurs de GitHub raccourcissent ca en "repo" pour "repository". Il peut etre un espace de stockage sur GitHub ou un autre hebergeur en ligne. A l'interieur d'un depot, vous pouvez conserver des fichiers de codes, des fichiers txtdes images.

**Controle de version**: Fondamentalement, l'objectif pour lequel Git a ete concu. Quand vous avez un fichier Word, vous l'écrasez à chaque fois que vous sauvgardez plusieurs versions. Avec Git, vous n'est plus oblige de faire ca. Git conserve des "instantanes" de chaque point dans l'historique d'un projet, de sorte que vous ne pouvez jamais le perdre ou l'ecraser.

**Commit**: C'est la commande qui donne à git toute puissance. Quand vous committez, vous prenez un instantané, une photo de votre depot à ce stade vous donnant un point de controle que vous pouvez ensuite réévaluer ou tout simplement restaurer votre projet à cette version. Il est nécessaire de rappeler que le nom de vos commits doivent-être parlant afin de savoir à quel stade du projet celui-ci a été fait.

**Branche**: Comment plusieurs personnes travaillant sur un projet en meme temps sans que Git ne s'embrouille? Habituellement, elle se debranchent du projet principal avec leur propres versions complètes, des modifications qu'elles ont chacune produites de leur cote. Apres avoir termine, il est temps de fusionner cette branche pour la ramener vers la branche master, le repertoire principal du projet.

### 2.2 Commandes specifiques Git 
**git init**: Initialise un nouveau depot git jusqu'a ce que vous executiez les commandes Git qui suivent.

**git config**: Raccourci de configuration, ceci est tout particulièrement utile quand vous paramétrez Git pour la premiere fois indentifiant et mot d'utilisateur.

**git help**: Oublie une commande? pour afficher les 21 commande de git.

**git status**: Verifie le statut de votre repo. Voir les fichiers et quelle sont les modifications à commiter et sur quelle branche ou repo vous etes en train de travailler.

**git add**: Ceci n'ajoute pas des fichiers dans votre repo, Au lieu de cela, cela porte de nouveaux fichiers à l'attestation de Git. Apres avoir ajoute des fichiers, ils dont inclus dans les instantanes du depot Git.

**git commit**: La commande la plus importante de Git. Apres avoir effectue toute sorte de modification vous entrez ca afin de prendreun instantanes du depot. le mettre en memoire. On ecrit ca sous la forme de git commit -m 'votre message'. Le -m indique que la section suivante de la commande devrait etre lu comme in message.

**git branche**: Vous travaillez avec plusieurs collaborateurs et vous voulez produire des modification de votre cote? cette commandevous permet de construire une nouvelle branche, ou une chronologie des commits, des modifications et  des ajouts de fichiers qui sont completement les votres. Votre titre va apres la commande. Si vous vouliez creer une nouvelle branche appellee 'chats', vous saisiriez git branche chats.

**git checkout**: C'est une commande de navigation qui vous permet de vous deplacer vers le repertoire que vous voulez verifier. Vouspouvez utiliser cette commande sous la forme de git checkout master pour regarder la branche master, ou git checkout chats pour regarder une autre branche.

**git merge**: Lorsque vous avez fini de travailler sur une branche, vous pouvez fusionner vos modifications vers la branche master,qui est visible pour tous les collaborateur. git merge chats prendrait toutes les modifications que vous avez apportées à la branche chats et les ajoutera à la branche master.

**git push**: Si vous travaillez sur votre ordinateur en local et voud voulez que vos  commits soient visibles aussi en ligne surGithub, vous  pushez les modifications vers  GitHub avec cette commande.

**git  pull**: Si vous travaillez en local et que vous voulez la version la plus a jour de votre repo pour travailler dessus, vous pullez les modifications provenant de GitHub avec cette commande.

**git clone**: Permet de dupliquer, cloer un repo existant sur GitHub pour l'avoir en local. La commande git clone doit etre suivit de url de repo correspondant qui copie depuis GitHub direct.


## 3 Fonctionnement GIT

### 3.1 branch master
Cette branche est la branche principale du projet, c'est sur cette branche que les différentes parties vont être merge. Avant de merge sur celle-ci **vérifiez que votre code fonctionne** et **commentez** on ne le dira jamais trop mais dans le travail collaboratif il faut communiquer. Si il y a un conflit c'est que l'assimilation du code de la branch master et l'autre (ou les autres) ne s'est pas effectuée correctement. En cas de conflit il faut vérifier que le code rajouté à bien été pris en compte et que d'autres n'ont pas étées supprimées.

### 3.2 branch dev / test ...
Une branch commune est souvent ajoutée pour les mutualisations de code afin de protége la branch master. On préfèrera pull les modifications des autres branchs.
   
### 3.3 branch nomDeBranch
Sur cette branch vous metterez à jour vos avancées dans la programmation. _Git add ._ et son commit sont différents de la sauvegarde sur l'ordinateur, pas besoin de commit à chaque sauvegarde en local. **Il ne faut pas confondre ou assimiler le commit et le push!** On doit commit pour push mais chaque commit n'implique pas un push.

### 3.4 Commit 
Avant de Commit tu dois entrer _git add ._ , cette commande récupèrera les changements depuis le dernier commit et seront utilisés pour le commit qui suit. _git commit -m "tonblabla"_ sert à sauvegarder tes changements pour ton **versionning**, ainsi en plus d'avoir une sauvegarde dans ton explorateur de fichier (ne gardant que la dernière version), tu auras également une trace de tes changements et te permettera de faire machine arrière si quelque chose se passe mal.

### 3.5 Push
Push sur ta branch quand tu as ajouté une fonctionnalité qui marche, afin qu'on puisse récupérer le travaille fait et voir si c'est compatible. Ce n'est que sur la fin du projet ou que quelqu'un à finit de travailler sur le projet qu'il fera un merge / push sur la branch dev / test. Avant de **push sur une autre branch que la vôtre**, vérifiez que vous ètes à jour sur la destination du push à l'aide de _git log_ et si besoin pullez, attention aux conflits.

### 3.6 Pull
Avant de taper _git pull origin nomDeBanch_, il faut **obligatoirement** que l'autre branch ai push pour pouvoir récupérer les changements. Il est **recommandé** de push sur notre branch avant de pull le contenu d'une autre pour réduire les risques de **conflits**, mais il est **encore plus fortement conseillé** de faire au moins un commit pour avoir une sauvegarde en cas de conflit. 

### 3.7 Conflits
Les conflits sont à Git ce que les bugs sont aux développeurs, fréquents... Pour les éviter au maximum il faut éviter de modifier le même fichier sur deux branch différente. Essayez de pull toutes les modifications apportées à ce même fichier de toute les branchs où il aurait été modifier **avant** de commencer à le modifier de votre côté. [Doc: Atlassian]( https://www.atlassian.com/fr/git/tutorials/using-branches/merge-conflicts)


## Documentation
[Blog: Synbioz](https://www.synbioz.com/blog/tech/git-adopter-un-modele-de-versionnement-efficace)  
[Forum: Openclassrooms ](https://openclassrooms.com/forum/sujet/git-pull-sans-commit-49970#message-7109921)

>En espérant que ce ReadMe vous ai été utile.



