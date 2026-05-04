# GLPI ITSM Lab — GLPI 10.0.24 sur Debian 13 (Apache2 + MySQL)

Projet de lab ITSM visant à **installer, configurer et administrer GLPI 10.0.24** sur **Debian 13** avec **Apache2** et **MySQL**, afin de gérer :
- les **tickets** (incidents / demandes),
- les **actifs** (inventaire du parc),
- les **utilisateurs, rôles et permissions**,
- les **rapports/statistiques**.

---

## Objectifs

- Déployer une plateforme **GLPI** fonctionnelle (Web + base de données).
- Mettre en place un environnement ITSM : **catégories, modèles, règles, workflows**.
- Créer et organiser un inventaire des **actifs**.
- Appliquer des **bonnes pratiques de sécurité** (droits, comptes dédiés, organisation des rôles).

---

## Stack / Technologies

- **Debian 13**
- **Apache2**
- **MySQL**
- **PHP** (extensions requises par GLPI)
- **phpMyAdmin** (optionnel)
- **GLPI 10.0.24**
- Réseau de lab : **NAT / Host‑Only**

---

## Architecture

- Serveur Debian 13 (VM / lab)
- GLPI déployé dans : `/var/www/html/glpi`
- Base MySQL dédiée (ex: `glpidb`) + utilisateur dédié (ex: `glpiuser`)
- Accès : `http://127.0.0.1/glpi`

---

## Installation (résumé)

1. Installation de la stack : **Apache2 + MySQL + PHP** (+ extensions GLPI)  
2. Création d’une base MySQL dédiée et d’un utilisateur MySQL dédié  
3. Déploiement de **GLPI 10.0.24** dans `/var/www/html/glpi`  
4. Ajustement des permissions et configuration Apache (VirtualHost / rewrite si besoin)  
5. Installation via l’interface web GLPI (connexion DB, configuration initiale)

---

## Configuration ITSM (réalisée)

- **Tickets**
  - Catégories
  - Modèles (templates)
  - Règles (ex : attribution automatique, routage)
- **Actifs**
  - Création des types d’actifs (PC, laptop, imprimante, équipements réseau, etc.)
  - Organisation : emplacements, statuts, affectations
- **Utilisateurs / Rôles**
  - Profils (Admin, Technicien, Helpdesk, Utilisateur)
  - Permissions adaptées (principe du moindre privilège)

---

## Sécurité / Bonnes pratiques appliquées

- Permissions sécurisées sur le répertoire **/glpi**
- Base MySQL dédiée + **compte MySQL séparé** (pas de root)
- **Changement du mot de passe admin** après installation
- Structuration claire des rôles IT

---

## Tests & Vérifications

- Création de tickets (incident/demande)
- Attribution et traitement (manuelle et/ou via règles)
- Ajout d’actifs et vérification de l’inventaire
- Rapports et statistiques
- Contrôle des accès selon les profils

---

## Ce que j’ai appris

- Fonctionnement d’une solution **ITSM** (process, workflows, rôles)
- Gestion de parc informatique (**inventaire, affectation, cycle de vie**)
- Administration Linux + services web (**Apache/MySQL**) autour d’une application
- Mise en pratique des bonnes pratiques de sécurité

---

## Auteur

- **GitHub :** @youssef-pi  
- **Date :** 2026-05-04
