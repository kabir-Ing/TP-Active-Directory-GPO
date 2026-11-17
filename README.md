# TP – Création et configuration d'une unité d'organisation avec application des GPO

## Présentation

le TP porte sur la création et la configuration d'unités d'organisation (UO) dans
Active Directory, la gestion de comptes utilisateurs, la configuration des autorisations
d'un dossier partagé et l'application de stratégies de groupe (GPO) dans l'environnement
de laboratoire LabTech.

## Objectifs du TP

- Créer une UO « Utilisateurs » et y ajouter les comptes demandés.
- Organiser les comptes dans les UO prévues par le TP.
- Configurer les autorisations de partage et de sécurité du dossier `fondecran`.
- Créer et lier des stratégies de groupe.
- Configurer le fond d'écran des utilisateurs .
- Vérifier le résultat en ouvrant des sessions avec les comptes utilisateurs.

## Environnement et outils 

- Windows Server
- Active Directory Users and Computers
- Group Policy Management
- GPO (Group Policy Objects)
- Postes clients Windows 10
- Environnement de laboratoire LabTech

## Travail réalisé

### 1. Unités d'organisation et comptes

Le TP présente une organisation Active Directory avec les unités « Utilisateurs » et
« Administrateurs », puis la création de plusieurs comptes utilisateurs.

### 2. Dossier partagé et autorisations

Le dossier `C:\fondecran` est utilisé pour stocker les images de fond d'écran.
Le rapport montre la configuration des autorisations de partage ainsi que les
autorisations de sécurité du dossier.

### 3. Stratégies de groupe

Le rapport illustre la configuration de stratégies de groupe, notamment :
- le paramètre **Desktop Wallpaper** ;
- le paramètre **Disable Active Desktop**.

Les captures montrent le rattachement des stratégies aux unités d'organisation et
des essais de connexion sur les postes clients.


## Documentation

Le rapport PDF original est disponible ici :
[`documentation/rapport-TP6-original.pdf`](documentation/rapport-TP6-original.pdf)

## Compétences travaillées

- Administration de Windows Server
- Gestion d'Active Directory et des unités d'organisation
- Création et organisation de comptes utilisateurs
- Configuration des permissions de partage et de sécurité
- Gestion et application des stratégies de groupe (GPO)
- Vérification des paramètres sur des postes clients


**Apprendre • Construire • Sécuriser • Progresser**



> Projet pédagogique réalisé en environnement de laboratoire.
