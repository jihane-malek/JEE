
#Patients MVC

#Structure du projet patients-mvc
1. src/main/java/jihane/malek/patientsmvc
Ce répertoire contient tout le code source Java, organisé en plusieurs sous-packages pour assurer une structure claire et maintenable.

#entities :

#Patient.java :
Classe représentant l'entité Patient, mappée à une table de la base de données.
Contient les attributs d'un patient (par exemple : id, nom, dateNaissance, etc.).
Utilise les annotations JPA comme @Entity et @Id pour définir la table et les colonnes.
Utilité : Fournit une structure d'objet pour manipuler les données des patients dans l'application.
repositories :

#PatientRepository.java :
Interface qui hérite de JpaRepository ou CrudRepository.
Fournit des méthodes prêtes à l'emploi pour effectuer des opérations CRUD (Create, Read, Update, Delete) sur les entités Patient.
Exemple : findAll(), save(), et deleteById() permettent de simplifier la gestion des données.
Utilité : Abstraction pour interagir avec la base de données sans écrire de requêtes SQL manuellement.
web :

#PatientController.java :

Classe contrôleur qui gère les requêtes HTTP et connecte la logique métier à la vue.
Utilise des annotations Spring comme @Controller ou @RequestMapping.
Exemple : Méthodes pour afficher la liste des patients, ajouter un nouveau patient, ou supprimer un patient.
Utilité : Fournit les endpoints nécessaires à l'application et orchestre les interactions entre le modèle et la vue.
PatientsMvcApplication.java :

Classe principale du projet contenant la méthode main.
Utilise l'annotation @SpringBootApplication pour indiquer qu'il s'agit d'une application Spring Boot.
Lance le serveur intégré (par exemple : Tomcat) et configure automatiquement le projet.
#2. src/main/resources
Ce répertoire contient toutes les ressources nécessaires à l'application, telles que les fichiers de configuration, les templates, ou les fichiers statiques.

#templates :
Contient les fichiers HTML qui définissent l'interface utilisateur de l'application.
Ces fichiers sont utilisés avec Thymeleaf (ou tout autre moteur de template pris en charge par Spring).
Exemple : Un fichier HTML pour afficher la liste des patients ou un formulaire pour ajouter un patient.
L'utilité de Java dans ce projet
Java est utilisé dans ce projet en raison de sa robustesse et de sa compatibilité avec Spring. Ses caractéristiques principales incluent :

Orienté objet : Facilite la modélisation des entités comme Patient.
Écosystème riche : Intégration avec des frameworks comme Spring MVC et JPA pour développer rapidement des applications web.
Sécurité : Java propose des outils puissants pour construire des applications sûres, particulièrement dans les environnements d'entreprise.
L'utilité de Spring dans ce projet
Spring MVC est un sous-module de Spring Boot qui permet de développer facilement des applications web basées sur l'architecture MVC (Modèle-Vue-Contrôleur).

#Architecture MVC :

Modèle : Décrit les données de l'application (dans ce cas, la classe Patient).
Vue : Interface utilisateur (dans le dossier templates).
Contrôleur : Relie le modèle et la vue (dans PatientController).
#Principaux avantages :

Configuration simplifiée : Avec Spring Boot, les configurations complexes sont automatisées.
Gestion des dépendances : Maven simplifie l'intégration des bibliothèques nécessaires.
Support des bases de données : Spring Data JPA facilite l'intégration avec les bases de données relationnelles.
