# TP 1 - Installation d’Ubuntu Server et priseen main du shell
## Exercice 2. Prise en main de l’interpréteur de commandes

### Manuel
1. A l’aide du manuel, identifiez le rôle de la commande which
> La commande which retourne le chemin pour accéder aux fichiers qui seraient executés si les arguments étaient tapés en ligne de commande.

2. Quand on consulte une page du manuel, comment peut-on rechercher un terme (par exemple, chercherle termeoptiondans la page de manuel dewhich?
>Pour rechercher un terme lors d'une recherche sur le manuel on peut, une fois sur la page du manuel en entrant "/" suivi du terme voulu pour mettre en surbrillance les termes recherchés. ex :/filenames"


3. Comment quitte-t-on le manuel?
>On quitte le manuel en appuyant sur q.

4. Chaque sectiondu manuel a une première page, qui présente le contenu de la section. Aﬀicher lapremière page de la section 6; de quoi parle cette section?
>Cete section parle de jeux et programmes qu'il y a dans le système, on y accède via la commande "man 6 intro"

### Navigation dans l’arborescence des fichiers

1. allez dans le dossier /var/log
>Pour accéder au dossier /var/log, on utilise la commande cd. En tapant "cd.vaR.log", on accède au dossier voulu en chemin absolu.

2. remontez dans le dossier parent (/var) en utilisant un chemin relatif
>Pour remonter au dossier parent en utilisant un chemin relatif il suffit d'exécuter la commande "cd..." qui permet de retourner au dossier parent.

3. retournez dans le dossier personnel
>Pour retourner au dossier personnel, on exécute "cd".

4. revenez au dossier précédent (/var)sans utiliser de chemin
>Pour retourner au dossier var depuis le dossier personnel sans utiliser de chemon, on peut utiliser "cd -" qui permet de retourner au dossier precedent.

5. essayez d’accéder au dossier /root; que se passe-t-il?
>Pour accéder au dossier root, on utilise "cd /" pour accéder directement à la racine.

6. essayez la commande sudo cd /root; que se passe-t-il? Expliquez
>En tapant "cd/root", on obtient une erreur nous disant que root n'existe pas , ce qui est normal car en tapant /root on recherche le dossier root dans la racine qui n'existe pas.

7. à partir de votre dossier personnel, créez l’arborescence suivante :
>Pour créer cette arborescence, on utilisel a commande "mkdir" pour créer des dossiers et "cat" pour créer des fichiers. ex :mkdir Dossier1". "cat fichier1.txt".
¨Pour créer cette arborescence depuis notre dossier personnel on entre : 
>  - mkdir Dossier 1
>  - mkdir Dossier 2
>  - cd Dossier 1
>  - car <Fichier 1.txt
>  - cd...
>  - mkdir Dossier2
>  - cd Dossier2
>  - mkdir Dossier2.1
>  - mkdir Dossier2.2
>  - cd Dossier2.2
>  - car > Fichier2.txt
>  - car > Fichier3.txt

8. revenez dans votre dossier personnel; à l’aide de la commande rm, essayez de supprimer Fichier1, puisDossier1; que se passe-t-il?
> Depuis le dossier personnel, si on essaye d'utiliser la commande rm pour supprimer Fichier1, ça ne fonctionne pas car il faut tout d'abord être dans le Dossier1 afin de pouvoir effectuer la commande. Si on essaye ensuite de supprimer Dossier1 grâce à cette même commande, ça ne fonctionne pas non plus car Dossier1 n'est pas un fichier. Il faudrait utiliser la commande "rmdir Dossier1" pour supprimer Dossier1.

9.  quelle commande permet de supprimer un dossier?
> La commande permettant de supprimer un dossier est "rmdir"

10. que se passe-t-il quand on applique cette commande à Dossier2?
>Si on execute "rmdir Dossier2", ça ne fonctionne pas car Dossier2 est n'est pas vide. 

11. comment supprimer en une seule commande Dossier2 et son contenu?
> Pour supprimer en une seule commande Dossier2 et son contenu on utilise la commande "rm -r" pour supprimer un dossier même s'il n'est pas vide. On entre alors "rm -r Dossier2".

## Commandes importantes

1. Quelle commande permet d’aﬀicher l’heure? A quoi sert la commande time?
> La commande permettant d'afficher l'heure est date. La commande Time donne des informations sur les ressources utilisées par les programmes.  

2. Dans votre dossier personnel, tapez successivement les commandes ls puis la; que peut-on en déduiresur les fichiers commençant par un point?
>ls affiche le contenu du dossier et la affiche également les fichiers cachés.

3. Où se situe le programmels?
>En utilisant la commande "whereis", on peut trouver la localisation d'un programme sur le disque. En executant "whereis ls", on voit alors que ls est situé dans /usr/bin/ls, et son manuel dans /usr/share/man/man1/ls.1.gz.


4. Essayez la commandell. Existe-t-il une entrée de manuel pour cette commande? Utilisez les com-mandesaliasoualiaspour en savoir plus sur la nature de cette commande.
> Grace a la commande "alias ll", on apprend que la commande ll est un alias de la commande ls -alF, elle affiche donc le contenu du dossier, en affichant les fichiers cachés (-a), les details des fichiers/dossiers (-s) ainsi que des indicateurs pour les fichirs/dossiers (-F).

5. Quelle commande permet d’aﬀicher les fichiers contenus dans le dossier/bin?
> Pour afficher le contenu de /bin, on utilise "ls /bin".

6. Que fait la commandels ..?
> La commande "ls .." affiche le contenu du dossier parent.

7. Quelle commande donne le chemin complet du dossier courant?
>La commande qui donne le chemin complet du dossier courant est 'pwd'

8. Que fait la commandeecho 'yo' > plopexécutée 2 fois?
>  En executant "echo yo > plop", on redirige l'affichage de plop qui devait s'afficher dans la console vers le fichier plop qui est créé. En l'executant 2 fois, cela ne change rien car le chevron écrase le fichier s'il existe deja. il y a donc uniquement un seul "yo" dans plop

9. Que fait la commande echo 'yo' >> plop exécutée 2 fois?
> Le double chevron redirige la sortie de echo a la fin du fichier sans l'écraser, donc en l'executant 2 fois on a 2 "yo" dans plop.


10. A quoi sert la commande file? Essayez la sur des fichiers de types différents.
>La commande file renvoie le type de dossier. En le faisant sur dossier, on remarque que c'est de type "directory". Sur le fichier plop, on voit que c'est un fichier texte. ('file dossier1' et 'file plop')

11. Créez un fichiertotoqui contient la chaîneHello Toto !; créer ensuite un lientitivers ce fichieravec la commandeln toto titi. Modifiez à présent le contenu detotoet aﬀichez le contenu detiti:qu’observe-t-on? Supprimez le fichiertoto; quelle conséquence cela a-t-il surtiti?
>Pour créer toto, avec la chaine 'Hello toto !', on utilisa la commande 'echo Hello toto!> plop'. En exécutant la commande 'ln toto titi', on crée un lien titi vers le fichier toto. Ensuite, on voit qu'en modifiant toto, cela modifie également le contenu de titi ('echo ReHello >> toto'). De plus, en supprimant toto, cela ne supprime pas titi et le contenu reste le même.   

12. Créez à présent un liensymboliquetutusurtitiavec la commandeln -s titi tutu. Modifiez lecontenu detiti; quelle conséquence pourtutu? Et inversement? Supprimez le fichiertiti; quelleconséquence cela a-t-il surtutu?
>En créent un lien symbolique tutu sur titi (ln -s titi tutu), on remarque que tutu et titi sont liés : si on modifie titi ou tutu l'autre fichier est modifié en cons"quence et si on supprime titi, tutu est inutilisable. 

13. Aﬀichez à l’écran le fichier/var/log/syslog. Quels raccourcis clavier permettent d’interrompre et reprendre le défilement à l’écran?
>Pendant l'affichage de syslog, on peut utiliser les raccourcis claviers CTRL + S et CTRL + Q pour reprendre le défilement du texte. 

14. Aﬀichez les 5 premières lignes du fichier/var/log/syslog, puis les 15 dernières, puis seulement leslignes 10 à 20.
> Pour afficher les 5 premières lignes du fichier, o, utilise la commande '5 syslog'. Pour afficher les 15 dernières lignes : 'tail -15 syslog'. On affiche les 20 premières lignes grâce à 'head -20 syslog'  Avec la commande | on affiche les 10 dernières lignes des 20 premières lignes precedemment affichées. La commande entière est pour afficher les lignes de 10 à 20, on a donc la commande suivante 'head -20 syslog | tail -10'.

15. Que fait la commande dmesg | less?
> La commande dmesg permet d'afficher la mémoire tampon de message du noyau. La commande less permet de visualiser un fichier en disposant de plusieurs fonctionnalités comme pouvoir naviger dans celui ci ou rechercher des chaînes. En executant "dmesg | less", on peut naviger dans l'affichage de la mémoire tampon de message du noyau. 

16. Aﬀichez à l’écran le fichier/etc/passwd; que contient-il? Quelle commande permet d’aﬀicher la pagede manuel de ce fichier?
>passwd est le nom du gichier associé à la commande passwd, qui permet de changer de mot de passe. Pour afficher son manuel on utilise "whereis passwd".

17. Aﬀichez seulement la première colonne triée par ordre alphabétique inverse
>On utilise "cut -c1" pour afficher uniquement la 1ere colonne et "sort -r" pour trier par ordre alphabetique inverse. On execute alors "cut -c1 /etc/passwd | sort -r" pour afficher la première colinne triée par ordre alphabétique inverse. 

18. Quelle commande nous donne le nombre d’utilisateurs ayant un compte sur cette machine (pas seule-ment les utilisateurs connectés)?
> La commande donnant le nombre d'utilisateurs ayant un compte est "wc -l /etc/passwd "

19. Combien de pages de manuel comportent le mot-clé conversion dans leur description?
> On utilise la commande "man -k conversion" et on trouve que 4 pages de manuel contionnent ce mot clé

20. A l’aide de la commande find, recherchez tous les fichiers se nommant passwd présents sur la machine
> On utilise la commande find /-name "passwd" pour rechercher tous les fichiers se nommant 

21. Modifiez la commande précédente pour que la liste des fichiers trouvés soit enregistrée dans le fichier~/list_passwd_files.txt et que les erreurs soient redirigées vers le fichier spécial/dev/null
> On execute "find / -name passwd > ~/list_passwd_files.txt" pour enregistrer les fichiers trouvés vers le fichier list_passwd_files et "find / -name passwd 2>> /dev/null" pour rediriger les erreurs vers /dev/null.

22. Dans votre dossier personnel, utilisez la commande grep pour chercher où est défini l’alias ll vu précédemment
> On execute "grep -ll", on obtient que ll est défini dans grep [OPTION] ... PATTERNS[FILE]

23. Utilisez la commande locate pour trouver le fichier history.log.
>Tout d'abord on installe la commande locate avec la commande "apt install mlocate", puis on recherche le fichier voulu avec "locate history.log" : on trouve que le chemin vers ce fichier est /var/log/apt/history.log

24. Créer un fichier dans votre dossier personnel puis utilisez locate pour le trouver. Apparaît-il? Pourquoi?
>En créant un fichier dans notre espace personnel et en le recherchant avec la commande locate, il n'apparait pas dans les résulats de la recherche.


## Exercice 4. Personnalisation du shell

1. Commencez par créer une copie de ce fichier, que vous appellerez.bashrc_bak

2. Editez le fichier.bashrcavecnanoet décommentez la ligneforce_color_prompt=yespour activerla couleur. Enregistrez le fichier et quitteznano.

3. Le fichier.bashrcest lu au démarrage du shell; pour le recharger, il faudrait donc se déconnecter puis se reconnecter; mais il existe un autre moyen : la commande source .bashrc. Testez-la, l’invite de commande devrait immédiatement passer en couleurs.
> En executant les commandes, l'invite de commande passe effectivement en couleur.  

4. Les couleurs par défauts (surtout celle du dossier courant) ne sont pas très visibles. Dans.bashrc,cherchez les lignes commençant par PS1=; elles indiquent la mise en forme de l’invite de commande(selon que l’on est en couleurs ou non).Sur cette ligne, on peut distinguer un certain nombre de raccourcis :
> On modifie la ligne de mise en forme de l'invite de commande PS1 = ... pour afficher la mise en forme voulue, on la remplace par : 
> PS1 = ' ${debian_chroot:+($debian_chroot)}\[\033[31m\][\A]\[\033[00m\]]-\[\033[32m\]\u@\h\[\033[00m\]:\[\033[34m]\w\[\033[00m\]\$ '






















