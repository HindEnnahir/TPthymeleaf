# Application Web CRUD Utilisant Spring Boot et Thymeleaf
Cette application permet de gérer des utilisateurs en fournissant des fonctionnalités CRUD (Créer, Lire, Mettre à jour, Supprimer) à l'aide de Spring Boot, Spring Data JPA et Thymeleaf. L'objectif est de simplifier le développement d'applications CRUD en tirant parti des fonctionnalités de Spring pour une gestion efficace de la persistance des données et de la présentation.
## Fonctionnalités
L'application est structurée en plusieurs couches pour une meilleure séparation des responsabilités :
1. Couche de Domaine : Définition des entités utilisateur pour la modélisation de la base de données.
2. Couche de Référentiel : Utilisation de CrudRepository de Spring Data JPA pour interagir avec la base de données en encapsulant la logique CRUD.
3. Couche Contrôleur : Gestion des requêtes HTTP et appel des méthodes de référentiel pour manipuler les entités.
4. Couche Présentation : Modèles HTML utilisant Thymeleaf pour afficher les formulaires d’inscription et de mise à jour, ainsi que la liste des utilisateurs.
## Structure de l'Application
1. Dépendances Maven
Le projet utilise spring-boot-starter-parent pour simplifier la gestion des dépendances et des versions. Cela permet de maintenir un fichier pom.xml minimaliste, tout en profitant de la configuration Spring Boot.
2. Configuration application.properties
Les paramètres de configuration standards sont définis dans le fichier application.properties pour simplifier la gestion de la persistance et des connexions à la base de données.
3. Couche de Domaine
La classe User modélise les entités utilisateur, avec des validations de champs pour garantir l'intégrité des données saisies par les utilisateurs.
4. Couche de Référentiel
En utilisant CrudRepository, Spring Data JPA permet d'implémenter une couche de persistance robuste sans coder manuellement les méthodes DAO. Cette couche d'abstraction rend la gestion des entités utilisateur rapide et efficace.
5. Couche Contrôleur
Le UserController gère les requêtes HTTP pour les opérations CRUD :
* showSignUpForm() : Affiche le formulaire d'inscription.
* addUser() : Valide et enregistre une nouvelle entité utilisateur.
* updateUser() : Met à jour un utilisateur existant.
* deleteUser() : Supprime un utilisateur de la base de données.
6. Couche Présentation
Les vues Thymeleaf, situées dans src/main/resources/templates, permettent d'afficher les formulaires et la liste des utilisateurs avec du contenu dynamique. Les modèles sont construits avec des expressions Thymeleaf telles que @{/adduser} et ${} pour intégrer des actions et des données.
7. Exécution de l'Application
Le point d'entrée de l'application est défini par une méthode main() typique de Spring Boot. Pour démarrer l'application :
* Exécutez le projet à partir de votre IDE.
* Ouvrez un navigateur et accédez à http://localhost:8080 pour voir l'interface utilisateur.
