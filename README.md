Git par la pratique
===================

* Mettez vous deux par deux.
* Créez vous chacun un compte sur GitHub.
* Dupliquez à l'aide de *fork* le projet TP02 dans votre espace public.
* Récupérez sur votre disque dur les sources du projet.

        git clone https://github.com/votrecompte/TP02.git

* Indiquez le dépôt officiel :

        cd TP02
        git remote add official https://github.com/estiam/TP02.git

* Sur votre disque dur, ajoutez à la fin de ce fichier le prénom et le nom **d'un** des membres du binôme. La ligne doit commencer par une étoile. Corrigez la liste pour que la dernière ligne se termine par un point et les autres par des virgules.
* Faites une révision :

        git checkout -b votrecompte1
        git add README.md
        git commit

* Publiez-la dans votre espace public:

        git push origin votrecompte1

* Ajoutez le prénom et le nom de l'autre membre du binôme selon les mêmes règles que tout à l'heure.
* Faites une révision :

        git checkout master
        git checkout -b votrecompte2
        git add README.md
        git commit

* Intégrez automatiquement la première branche à une branche d'intégration :

        git checkout master
        git checkout -b votrecompte1-votrecompte2
        git merge votrecompte1
        
* Essayez d'intégrer la seconde branche à

        git merge votrecompte2

* Réglez le conflit. Modifiez la mise en page de la liste pour qu'elle soit correcte. Puis déclarez que le conflit est réglé :

        git add README.md
        git commit

* Une fois que le conflit est réglé par une révision, publiez l'ensemble des révisions dans votre espace public :

        git push origin votrecompte1-votrecompte2

* Dans GitHub faites une demande d'intégration (*pull request*).

* Supposons maitenant que la branche officielle soit en déshérence et que vous décidiez de prendre la relève. Récupérez la dernière version officielle :
 
        git pull official master

* Récupérez la demande d'intégration d'un de vos collègues :

        git pull https://github.com/nomducollegue/TP02.git nomdesabranche

* Réglez le conflit. Mettez à jour votre branche maître. Publiez.
