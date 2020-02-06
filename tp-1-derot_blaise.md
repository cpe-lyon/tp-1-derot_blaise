# TP 1 - Installation d’Ubuntu Server et priseen main du shell
## Exercice 2. Prise en main de l’interpréteur de commandes

### Manuel
1. A l’aide du manuel, identifiez le rôle de la commande which
> La commande which retourne le chemin pour accéder aux fichiers qui seraient executés si les arguments étaient tapés en ligne de commande.

2. Quand on consulte une page du manuel, comment peut-on rechercher un terme (par exemple, chercherle termeoptiondans la page de manuel dewhich?
>Pour rechercher un terme lors d'une recherche sur le manuel on peut, une fois sur la page du manuel en entrant "/" suivi du terme voulu pour mettre en surbrillance les termes recherchés. ex :/filenames"


3.Comment quitte-t-on le manuel?
>On quitte le manuel en appuyant sur q.

4.Chaque sectiondu manuel a une première page, qui présente le contenu de la section. Aﬀicher lapremière page de la section 6; de quoi parle cette section?
>

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
>  En executant "echo > plop", on redirige l'affichage de plop qui devait s'afficher dans la console vers le fichier plop qui est créé. En l'executant 2 fois, cela ne change rien car le chevron écrase le fichier s'il existe deja. il y a donc uniquement un seul "yo" dans plop

8. Que fait la commandeecho 'yo' > plopexécutée 2 fois?
> Le double chevron redirige la sortie de echo a la fin du fichier sans l'écraser, donc en l'executant 2 fois on a 2 "yo" dans plop.

9. Que fait la commandeecho 'yo' >> plopexécutée 2 fois?
>

10. A quoi sert la commandefile? Essayez la sur des fichiers de types différents.
>

11. Créez un fichiertotoqui contient la chaîneHello Toto !; créer ensuite un lientitivers ce fichieravec la commandeln toto titi. Modifiez à présent le contenu detotoet aﬀichez le contenu detiti:qu’observe-t-on? Supprimez le fichiertoto; quelle conséquence cela a-t-il surtiti?
>

12. Créez à présent un liensymboliquetutusurtitiavec la commandeln -s titi tutu. Modifiez lecontenu detiti; quelle conséquence pourtutu? Et inversement? Supprimez le fichiertiti; quelleconséquence cela a-t-il surtutu?
>

13. Aﬀichez à l’écran le fichier/var/log/syslog. Quels raccourcis clavier permettent d’interrompre etreprendre le défilement à l’écran?
>

14. Aﬀichez les 5 premières lignes du fichier/var/log/syslog, puis les 15 dernières, puis seulement leslignes 10 à 20.
>

15. Que fait la commandedmesg | less?
>

16. Aﬀichez à l’écran le fichier/etc/passwd; que contient-il? Quelle commande permet d’aﬀicher la pagede manuel de ce fichier?
>

17. Aﬀichez seulement la première colonne triée par ordre alphabétique inverse
>

18. Quelle commande nous donne le nombre d’utilisateurs ayant un compte sur cette machine (pas seule-ment les utilisateurs connectés)?
>

19.Combien de pages de manuel comportent le mot-cléconversiondans leur description?
>

20.A l’aide de la commandefind, recherchez tous les fichiers se nommantpasswdprésents sur la machine
>

21.Modifiez la commande précédente pour que la liste des fichiers trouvés soit enregistrée dans le fichier~/list_passwd_files.txtet que les erreurs soient redirigées vers le fichier spécial/dev/null
>

22.Dans votre dossier personnel, utilisez la commandegreppour chercher où est défini l’aliasllvuprécédemment
>

23.Utilisez la commandelocatepour trouver le fichierhistory.log.
>

24.Créer un fichier dans votre dossier personnel puis utilisez locate pour le trouver. Apparaît-il? Pourquoi?
>























