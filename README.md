READ_me_ProjetProxiBanque_Sébastien_Ludovic :

Le livrable est constitué de 3 écrans fonctionnels et 5 écrans d’erreur. La correspondance avec la spécification est la suivante:
	Ecran N°1 : Authentification Conseiller
    => TestAuthenticationManagerAJAX 
	Ecran N°2 : Liste des Clients
    => ClientListDisplayAJAX
	Ecran N°3 : Edition d’un client
    => ClientListDisplayAJAX
	Ecran N°4 : Liste compte d’un client
    => MoneyTransferAJAX
	Ecran N°5 : Virement Compte à Compte
    => MoneyTransferAJAX
	Ecran N°6 : Erreur 
    => Erreur Authentification
    => ErreurAccountsNotFound
    => ErreurIdenticalAccounts
    => ErreurInsufficientBalance
    => ErreurNegativeAmount
Le site peut être testé avec les jeux de données des fichiers JSON suivant
-	account_list
-	bank_clients
-	bank_exec_creds

Afin de naviguer sur le site Proxibanque et effectuer les diverses fonctionnalités proposées par le site, vous devez suivre un certain nombre d’opérations:
Dans le dossier Apache de votre poste (C:\Program Files\Apache Software Foundation\Apache2.4\htdocs), veuillez copier les fichiers contenus dans le dossier « Projet Web Static Sebastien Ludovic\Fichiers à copier dans Apache » (situé sur le réseau interne dans \\PARME26\Formation ou sur GitHub sur le repository https://github.com/sign00/proxibanque5.git )
-	Ouvrir une page internet (Mozilla ou Chrome de préférence)
-	Taper dans la barre de recherche : « localhost »
*	Une liste des fichiers contenus dans le dossier Apache s’affiche.
-	Cliquer sur « TestAuthenticationManagerAJAX » pour afficher la page de connexion Conseiller du site Proxibanque
o	Pour vous connecter vous devez renseigner un conseiller connu, par exemple :
*	Login : moiGrandConseiller, password : 123Soleil
*	Login : moiGrandVizir, password : laMarelle123
En cas d’erreur au moment de la saisie du login ou mot de passe, un écran d’erreur s’affiche et propose de réessayer.
En cas de succès, la liste des clients s’affiche à l’écran, vous pouvez :
-	Editer toutes les informations d’un client (sauf son ID)
-	Effectuer un virement entre comptes en cliquant sur le bouton prévu à cet effet

Un bouton de retour à la liste clients est disponible dans la page de virements.

Edition des informations d’un client :
Pour modifier les informations d’un client, vous devez le sélectionner au préalable grâce au bouton radio sur la même ligne, ce qui ouvre un nouvel écran, dans lequel vous pouvez :
-	Saisir les modifications souhaitées dans les champs des formulaires
-	Appuyer sur le bouton « Valider » pour effectuer les modifications
L’ID du client ne peut pas être modifié. Les champs laissés en blanc ne seront pas modifiés.

Effectuer un virement :
Vous devez renseigner les champs pour effectuer un virement, la liste des comptes est affichée en dessous des formulaires :
-	Numéro du compte à Débiter
-	Numéro du compte à Créditer
-	Montant de la transaction
-	Cliquer sur « Valider » pour effectuer un virement
Attention cliquer à nouveau sur « Valider » déclenche un nouveau virement.

Plusieurs cas d’erreur sont possibles et redirigent à un écran d’erreur, par exemple :
-	Le montant est négatif
-	Le montant est supérieur au solde du compte débiteur
-	Les numéros des comptes à créditer et débiter sont identiques
-	Le numéro d’un ou des deux comptes est(sont) inconnu(s)
Il est bien sur possible de revenir en arrière.
Pour réinitialiser les opérations de virements, cliquer sur le bouton de rafraichissement de la page (ou F5).
