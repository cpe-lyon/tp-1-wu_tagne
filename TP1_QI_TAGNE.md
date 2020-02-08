### COMPTE RENDU  TP1

##  EXERCICE 2

# Manuel 

1. la commande which permet   de localiser une commande.
2. pour chercher un terme on utilise le mot clé  *apropos* suivi du mot que l'on cherche.
3. pour quitter le manuel on utilise la touche *q* du clavier.
4. on a afficheer la premiere page du manuel avec la commande *man 6 inntro* cette  page parle de l'introduction to games.


# Navigation dans l’arborescence des fichiers 
1. on a utlisé la commande :*cd /var/log*.
2. *cd ..*  cette commande permet de remonter dans le dossier parent.
3. *cd* cette commande permet de retourner dans le dossier personnel.
4. *cd -* cette commande permet de retourner  au dossier pécédent.
5. *cd /root * on a pas accès au dossier  root , on le message *permission denied*. 
6. *sudo cd /root*  on nous demande de saisir le mot de passe de  l'utilisateur supérieur du systeme linux.
7. *cd
   *mkdir Dossier1
   *mkdir Dossier2
   *cd Dossier1
   *touch Fichier1
   *cd ../Dossier2
   *mkdir Dossier2.1
   *mkdir Dossier2.2
   *cd Dossier2.2
   *touch Fichier2
   *touch Fichier3

8. 
9. la commande *rmdir* permet de suprimmer un dossier.
10. on nous dit que qu'on ne peut pas le supprimer car le dossier n'est pas vide.
11.  on utilise la commande *rm -r* pour supprimer le dossier en une seul ligne.



# Commandes importantes 
1. la commande *date* permet d'afficher l'heure  et la date.Commande*time commande* permet d'afficher le temps d'execution d'une commande.
2. la commande   *ls* permet d'afficher les fichiers visuels  , *la* elle permet d'afficher les fichier commencant par un point  et ls -a permet d'afficher tout les fichiers meme les liens.
3. le programme  *ls* se  trouve dans */bin*.
4. la commande  *ls -l*   est une entrée manuelle  pour la commande  *ll*.
5. la commande *ls /bin * permet d'afficher les fichiers contenus dans le dossier bin.
6. la commande  *ls ..* liste les fichiers contenus dans le dossier parent.
7. la commande *pwd* permet  de donner le chemin complet du dossier courant.
8. la commande *echo *yo*> plop*  réecris la chaine de caractère "yo" dans le fichier plop.A la fin on obtient un seul "yo".
9. la commande *echo *yo*>> plop*  ajoute  la chaine de caractère "yo" dans le fichier plop.A la fin on obtient deux  "yo".
10. la commande *file * permet d'afficher le type  d'un fichier.
11. * echo  'Hello toto' > toto 
    * ln toto titi
	en modifiant le contenu de toto, le contenu de titi est aussi changer. Après suppression de toto le contenu de titi reste inchangé.
12. on observe que tutu prend le contenu de titi et titi prend celui de tutu. en supprimant le fichier titi on observe que le fichier tutu a été aussi supprimer.

13.  la commande *less /var/log/syslog* permet d'afficher à l'écran le fichier /var/log/syslog.on utilise les touches home,end,pageup,pagedown,up,down,left,right sur le clavier.

14. la commande *head -5 /var/log/syslog* permet d'afficher les 5 premieres lignes du fichier .
    la commande *tail -15 /var/log/syslog* permet d'afficher les 15 dernieres lignes  du fichier.
    la commande *sed -n '10,20p' /var/log/syslog* permet d'	afficher les lignes 10 à 20 du fichier.
15. la commande  *dmesg | less* affiche  la memoire  tampon de message du noyau linux en fonction de less ( pour defilement plus pratique par contre avec cat  on peut pas defiler )

16.  la commande */etc/passwd* elle  contient  les mots de passe de tous les utlisateurs. la commande qui permet d'afficher  la page manuel de ce fichier est  *man 5 passwd*.

17. la commande *ls -1 -r* permet d'afficher  la premiere colonne triée par ordre alphabetique inverse.

18.  la  commande * who -a -q*  nous donne le nombre d’utilisateurs ayant un compte sur cette machine (pas seulement les utilisateurs connectés).

19.  on a 4 pages de manuel  qui comportent le mot-clé conversion dans leur description on les a trouvé grace à la commande *man -f conversion*.

20.  à l'aide  de  la commande *find / -name passwd* on a trouvé des fichiers ci-dessous
	/etc/cron.daily/passwd
	/etc/pam.d/passwd
	/etc/passwd
	/snap/core/8268/etc/cron.daily/passwd
	/snap/core/8268/etc/pam.d/passwd
	/snap/core/8268/etc/passwd
	/snap/core/8268/usr/bin/passwd
	/snap/core/8268/usr/share/bash-completion/completions/passwd
	/snap/core/8268/usr/share/doc/passwd
	/snap/core/8268/var/lib/extrausers/passwd
	/snap/core/7917/etc/cron.daily/passwd
	/snap/core/7917/etc/pam.d/passwd
	/snap/core/7917/etc/passwd
	/snap/core/7917/usr/bin/passwd
	/snap/core/7917/usr/share/bash-completion/completions/passwd
	/snap/core/7917/usr/share/doc/passwd
	/snap/core/7917/var/lib/extrausers/passwd
	/usr/bin/passwd
	/usr/share/lintian/overrides/passwd
	/usr/share/doc/passwd
	/usr/share/bash-completion/completions/passwd


21. la commande *find / -name passwd 1> ~/list_passwd_files.txt 2> /dev/null* permet  de  donner  la liste des fichiers trouvés soit enregistrée dans le fichier ~/list_passwd_files.txt et que les erreurs soient redirigées vers le fichier spécial /dev/null 
22. à fin on cherche où est défini l'alias ll, on peut utiliser la commande *grep 'alias ll' .bashrc*. Et le résultat est *alias ll='ls -alF'*.
23. on utilise la commande *locate history.log* pour le chercher. Cependant, il faut l'installer au début avec  la commande *sud apt install mlocate*.
24. dans notre cas, nous pouvons touver le fichier. Cependant, on ne peut pas localiser le fichier qu'on vient de créer. C'est parce que la commande *locate* cherche un fichier de la base de données créer par programme *crontab*.  Cette  base  de données n'est pas mis à jour toutes les secondes. on ne peut pas le localiser parfois.
	


##  EXERCICE 4

3. Après le test de la commande *source .bashrc*, l'invite de commande a changé en couleurs sans redémarrer le shell:

![changer couleur](/images/changer_couleur.png)	
	

4.  On doit seulement changer la premiere ligne  PS1 à 	**PS1='${debian_chroot:+($debian_chroot)}\[\033[01;31m\]\A\[\033[00m\]\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\$ '**, et après l'invite de commande est bien modifiée.


