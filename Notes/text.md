## Comprendre l'objectif du pojet
Le but est de créer un site où :
- un client peut réserver un voyage,
- choisir son siège,
- confirmer la réservation,
- voir son historique, <br>
et où :
- un administrateur peut gérer les voyages,
- voir les réservations,
- administrer les utilisateurs.

En pratique ce serait :
- un <b>Frontend</b> -> interface utilisateur,
- un <b>Backend API</b> -> logique du serveur,
- une <b>Base de données MySQL</b> -> stockage de données.

---
# Commande
- npm init -y : 
	- Initialisation du projet Node.js
	- Création de package .json :
		- le nom du projet
		- la version
		- les dépendances
		- les scripts
		- les informations du projet
- npm install express mysql2 cors dotenv
	- express : framework de backend principal (Création de serveur, des routes API, des reqûetes HTTP, des réponses JSON)
	- mysql2 : permet à Node.js de communiquer avec MySQL
	- cors :  pour l'autorisation de la communication entre frontend et backend
	- dotenv : stockage des informations sensibles dans un fichier <b>.ienv</b> (Protection des mots de passe, clés API, tokens, configurations sensibles)
	- nodemon : relancement automatique du serveur lors d'un modification d'un fichier