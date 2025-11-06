# Kafka 4, fantastique ?

## Générer les slides en local

1. Télécharger la dernière version de `reveal.js` https://github.com/hakimel/reveal.js/releases, le dézipper à la racine et nommer le répertoire `reveal.js`.


2. Lancer les commandes suivantes :
```
docker container run --rm -ti -u $(id -u):$(id -g) -v $(pwd):/documents asciidoctor/docker-asciidoctor:1.96 asciidoctor-revealjs index.adoc
```

3. Ouvrir le fichier index.html généré.

## Résumé

Vous l'attendiez, impatiemment, depuis quatre ans et ... ça y est ! **Kafka 4 est là !** À chaque release majeure, son lot de nouveautés, et on se retrouve pour explorer les évolutions clés, leurs motivations et leurs impacts.
 
Nous aborderons, entre autres :

- **La suppression de ZooKeeper** : le passage à KRaft pour simplifier la gestion et améliorer la scalabilité
- **Le nouveau protocole de rééquilibrage** : une optimisation des groupes de consommateurs pour plus de stabilité et de performance
- **Les files d'attente (Early Access)** : une consommation coopérative pour des cas d'usage point-à-point, étendant la polyvalence de Kafka

Nous détaillerons également les changements nécessaires pour vos applications (producteurs, consommateurs) et clusters : migration de Log4j vers Log4j2, transition de ZooKeeper à KRaft, mise à jour vers Java 11 (clients/Streams) et Java 17 (brokers/Connect/tools).

Vous repartirez avec une compréhension claire des nouveautés de Kafka 4 et des étapes concrètes pour réussir votre migration, que vous soyez développeur, architecte ou administrateur.

## Plan Original

* Introduction (5 minutes)
  * Pourquoi Kafka 4 est une release majeure (plus de 25 KIPs, ~200 tickets JIRA).
  * Objectifs du talk : Décrypter les nouveautés, expliquer leurs impacts, et fournir une feuille de route pour migrer.
* Les évolutions clés : Fonctionnalités, impacts et migrations
  * Suppression de ZooKeeper (6 minutes) : à quoi sert ZooKeeper ? Pourquoi le remplacer ? Exemple d'architecture avant / après. Comment migrer ?
  * Nouveau protocole de rééquilibrage des groupes de consommateurs (6 minutes) : comment ça fonctionnait avant ? Pourquoi cette amélioration ? Comment en profiter ?
  * Files d'attente pour Kafka (Early Access) (6 minutes) : Quels cas d'usage ? Démo de la fonctionnalité.
  * Réinitialisation d'offset basée sur une durée (5 minutes) : Explication du tiers storage et du stockage infini. Démo de la fonctionnalité.
  * Nouveaux Tools Kafka (4 minutes) : Présentation des Tools existants car peu connus. Présentation des nouveaux Tools.
  * Focus Exigences Java (2 minutes) : Clients Kafka et Kafka Streams : Nécessitent Java 11. Brokers, Connect, Tools : Nécessitent Java 17.
  * Migration de Log4j à Log4j2 (3 minutes) : Utilisation de l'outil log4j-transform-cli pour convertir les configurations Log4j existantes
* Récapitulatif et Takeaways (5 minutes)
* Questions / Réponses (3 minutes)


## Pourquoi ce talk ?

Apache Kafka 4 est une release majeure, avec plus de 25 KIPs (Kafka Improvement Proposals) et près de 200 tickets JIRA. Face à cette complexité, ce talk offre une synthèse claire des fonctionnalités clés, de leurs impacts sur les applications (producteurs, consommateurs, Spring Kafka) et des migrations nécessaires (KRaft, Log4j2, Java 11/17). 

Les participants repartiront avec :

- Une compréhension précise des nouveautés et de leurs bénéfices pratiques.
- Une feuille de route concrète pour migrer leurs clusters et applications.
- Des informations pour optimiser leurs architectures, que ce soit pour le développement, l'administration ou la conception.

Ce talk s'adresse aux développeurs, architectes et administrateurs, leur offrant des connaissances pour tirer pleinement parti de Kafka 4.

