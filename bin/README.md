# Springboot_contact

Application de gestion de contacts simple implémentée à l'aide de Spring Boot et de Spring Data JPA.

Cette application a été conçue pour apprendre Spring Boot, Hibernate avec Spring Data JPA et Hibernate Validator. Elle ne se concentre pas beaucoup sur la partie interface utilisateur.

Elle utilise uniquement trois tables :

User - pour gérer la connexion
Contact - pour stocker les informations de contact de l'utilisateur telles que le nom, l'adresse e-mail (comme les contacts dans un téléphone) et il a une relation many-to-one unidirectionnelle avec User.
ContactPhone - pour stocker les numéros de téléphone (oui ! elle peut stocker plusieurs numéros de téléphone pour chaque contact) pour chaque contact et il a une relation many-to-one unidirectionnelle avec Contact.
Dans le cadre de Spring MVC, cette application met en œuvre :

La création de mappages de requêtes à l'aide d'annotations et l'utilisation d'annotations de contrôleur et de référentiel.
La liaison de données du formulaire à l'arrière-plan.
L'injection automatique des objets requis.
La redirection d'un contrôleur à un autre à l'aide de flashattributes.
Dans le cadre de Hibernate Validator, cette application met en œuvre :

La vérification de la nullité et de la longueur à l'aide d'annotations.
La vérification des champs croisés à l'aide d'annotations définies par l'utilisateur au niveau de la classe.
L'utilisation des annotations Valid et BindingResult dans les classes de contrôleur.
Dans le cadre de Spring Data JPA :

L'utilisation du référentiel CRUD.
L'utilisation de la méthode findBy et delete en utilisant différents modèles de noms.
Dans le cadre de Hibernate ORM :

L'utilisation des annotations Entity et ID.
L'utilisation des annotations de mappage, utilisant uniquement une relation many-to-one unidirectionnelle.
L'utilisation des annotations Query et Param lors de l'utilisation de JPQL.
L'utilisation des annotations Transactional lors de la suppression de méthodes selon le modèle deleteby.
Quelles fonctionnalités peuvent être implémentées à l'avenir ?

AOP pour la journalisation et la vérification de session de sécurité avant l'accès aux méthodes de contrôleur critiques.
Hibernate - Fetch Type.
Session Spring utilisant Redis DB pour la gestion de session en cluster.
Mises à jour :

Pour faciliter le développement, une branche h2_database a été créée qui utilise une base de données h2 en mémoire.

h2-database & aop-brach a les mises à jour suivantes :

Aspectj est utilisé pour la mise en œuvre de préoccupations transversales telles que la journalisation et la vérification de session.
Dans le cadre d'Aspectj, nous pouvons apprendre l'utilisation d'annotations telles que Aspect, Point Cut expression, Around & Before advice types.



