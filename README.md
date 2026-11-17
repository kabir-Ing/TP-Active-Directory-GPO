# TP — Active Directory : création d'une unité d'organisation et application de GPO

![Windows Server](https://img.shields.io/badge/Windows-Server-0078D4?logo=windows&logoColor=white)
![Active Directory](https://img.shields.io/badge/Active%20Directory-Domaine-0078D4)
![GPO](https://img.shields.io/badge/Group%20Policy-Administration-0078D4)

## Présentation

Ce projet pédagogique porte sur l'administration d'Active Directory dans un environnement Windows Server fourni par LabTech.

Il couvre :

- la création d'unités d'organisation (UO) ;
- la création et l'organisation de comptes utilisateurs ;
- la configuration d'un dossier partagé et de ses autorisations ;
- la création et le rattachement de stratégies de groupe (GPO) ;
- la vérification des paramètres sur des postes clients Windows 10.

## Objectifs

- Créer une UO **Utilisateurs** et organiser les comptes concernés.
- Créer une UO **Administrateurs** pour structurer les comptes administratifs.
- Configurer les autorisations de partage et de sécurité du dossier `C:\fondecran`.
- Configurer le fond d'écran commun des utilisateurs.
- Désactiver Active Desktop afin d'assurer l'application du fond d'écran configuré.
- Lier les stratégies aux UO appropriées et vérifier leur application lors des connexions utilisateur.

## Environnement technique

| Élément | Technologie utilisée |
|---|---|
| Serveur | Windows Server |
| Annuaire | Active Directory |
| Gestion des utilisateurs | Active Directory Users and Computers |
| Gestion des stratégies | Group Policy Management |
| Postes clients | Windows 10 |
| Laboratoire | LabTech |

## Travaux réalisés

### 1. Création des unités d'organisation

La structure Active Directory comprend notamment les UO suivantes :

```text
Domaine
├── Utilisateurs
└── Administrateurs
```

Les comptes utilisateurs sont créés dans l'UO **Utilisateurs** afin de permettre l'application centralisée des stratégies du domaine.

### 2. Gestion des comptes utilisateurs

Les comptes demandés dans le TP sont créés dans Active Directory, puis placés dans les UO prévues.

Les paramètres suivants sont vérifiés :

- nom d'utilisateur ;
- appartenance au domaine ;
- emplacement dans l'UO ;
- mot de passe initial ;
- possibilité de connexion sur un poste client.

### 3. Configuration du dossier partagé

Le dossier suivant est utilisé pour stocker les images du fond d'écran :

```text
C:\fondecran
```

Deux niveaux d'autorisation sont configurés :

- les autorisations de partage ;
- les autorisations de sécurité NTFS.

Les permissions sont limitées aux besoins des utilisateurs afin d'autoriser la lecture des images tout en empêchant les modifications non souhaitées.

### 4. Création et liaison des GPO

Les paramètres suivants sont configurés dans Group Policy Management :

| Paramètre | Usage |
|---|---|
| Desktop Wallpaper | Définit le chemin de l'image de fond d'écran utilisée par les utilisateurs |
| Disable Active Desktop | Désactive Active Desktop pour permettre l'application du fond d'écran choisi |

Les GPO sont liées aux UO concernées afin que les paramètres s'appliquent uniquement aux comptes utilisateurs concernés.

### 5. Vérification sur les postes clients

La mise en œuvre est vérifiée depuis les postes Windows 10 :

1. connexion avec un compte utilisateur du domaine ;
2. ouverture d'une invite de commandes ;
3. actualisation des stratégies avec `gpupdate /force` ;
4. ouverture de la session de groupe avec `gpresult /r` ;
5. vérification de l'application des GPO ;
6. contrôle visuel du fond d'écran sur le poste client.

## Résultats attendus

- Les comptes utilisateurs sont correctement placés dans l'UO prévue.
- Les utilisateurs peuvent accéder au dossier partagé en lecture.
- Les modifications non autorisées du dossier partagé sont empêchées.
- Les GPO liées à l'UO des utilisateurs sont appliquées lors de l'ouverture de session.
- Le fond d'écran configuré s'affiche sur les postes concernés.
- Active Desktop est désactivé pour les utilisateurs concernés.

## Compétences travaillées

- Administration de Windows Server
- Gestion d'Active Directory et des unités d'organisation
- Création et organisation de comptes utilisateurs
- Configuration des autorisations de partage
- Configuration des autorisations de sécurité NTFS
- Création, liaison et dépannage de GPO
- Vérification des stratégies sur les postes clients

## Documentation

Le rapport PDF original est disponible dans le dépôt :

- [`documentation/rapport-TP6-original.pdf`](documentation/rapport-TP6-original.pdf)

## Auteur

Projet réalisé dans le cadre d'un TP d'administration Active Directory en environnement de laboratoire.

**Apprendre • Construire • Sécuriser • Progresser**

> Projet pédagogique réalisé en environnement de laboratoire LabTech.
