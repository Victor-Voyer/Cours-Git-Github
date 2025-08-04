# 🌐 Qu’est-ce que Git ?

Git est un **système de contrôle de version distribué**, créé par Linus Torvalds (le créateur de Linux).  
Il permet de :
- suivre l’historique des modifications d’un projet,
- travailler à plusieurs sans écraser le travail des autres,
- revenir à une version antérieure si besoin.

### 🔑 Concepts clés :
- **Dépôt (repository)** : le dossier contenant tous les fichiers du projet ainsi que l’historique des modifications.
- **Commit** : un "instantané" des modifications enregistrées. C’est comme une sauvegarde avec un message explicatif.
- **Branche (branch)** : une version parallèle du projet pour travailler sur une fonctionnalité sans toucher à la version principale (souvent appelée `main` ou `master`).
- **Merge** : fusionner une branche avec une autre (souvent pour intégrer un travail terminé dans la branche principale).
- **Staging area** : une zone intermédiaire où l’on prépare les fichiers à valider avant le commit.

### 🧪 Commandes de base :
```bash
git init                # Créer un dépôt Git
git status              # Voir les modifications
git add fichier.txt     # Ajouter un fichier à la zone de staging
git commit -m "Message" # Enregistrer les changements
git log                 # Voir l’historique des commits
git branch              # Lister les branches
git branch nom-branche  # Créer une nouvelle branche
git checkout branche    # Passer sur une autre branche
git merge branche       # Fusionner une branche avec l’actuelle
```
<br>
<br>

# 🌐 Qu’est-ce que GitHub ?

GitHub est une **plateforme en ligne d’hébergement de dépôts Git**. Elle permet de :

- Stocker du code en ligne  
- Collaborer à plusieurs  
- Gérer les versions d’un projet  
- Suivre les bugs et suggestions (via *issues*)  
- Proposer des modifications (via *pull requests*)  

---

## ⚙️ Fonctionnalités principales

- **Dépôts publics ou privés** : le code peut être ouvert à tous ou réservé à certaines personnes.  
- **Fork** : faire une copie d’un dépôt pour le modifier sans affecter l’original.  
- **Pull Request (PR)** : proposer une modification (fusion d’une branche dans une autre).  
- **Actions** : automatisations (tests, déploiements, etc.).  
- **Collaborateurs** : gestion des accès et des permissions.

---

## 🖥️ Interface Web

GitHub propose une interface web pour :

- Visualiser les commits, branches, PR, fichiers, etc.  
- Gérer les droits d’accès  
- Commenter et discuter les modifications  

<br>
<br>

# 🔗 Pourquoi connecter Git à GitHub ?

Git est un **outil local**. GitHub permet de **partager ce travail local en ligne**.  
La connexion entre les deux permet de :

- Sauvegarder le projet sur Internet  
- Travailler en équipe à distance  
- Collaborer via *pull requests* et *forks*  

---

## ⚙️ Étapes pour connecter Git à GitHub

### 1. Créer un dépôt GitHub vide  
Rends-toi sur [https://github.com](https://github.com) et crée un nouveau dépôt sans README (optionnel).

### 2. Connecter ton dépôt Git local à GitHub  
Dans ton terminal, exécute :

```bash
git remote add origin https://github.com/ton-utilisateur/nom-du-depot.git
```

<br>
<br>

# 📝 Questionnaire

## 🔹 Questions sur Git

**1. Quelle commande permet d’enregistrer les changements dans l’historique Git ?**  
<br>
a) `git push`  
b) `git commit`  
c) `git save`  
d) `git update`  

---

**2. Quelle commande crée un nouveau dépôt Git dans un dossier ?** 
<br>
a) `git start`  
b) `git clone`  
c) `git init`  
d) `git new`  

---

**3. Que fait la commande `git status` ?**  
<br>
a) Affiche les branches du projet  
b) Donne les logs des commits  
c) Montre les fichiers modifiés, en attente ou non suivis  
d) Supprime les fichiers ignorés  

---

## 🔹 Question sur la différence entre Git et GitHub

**4. Quelle est la principale différence entre Git et GitHub ?**  
<br>
a) GitHub est un éditeur de texte, Git est un outil en ligne  
b) GitHub permet de créer des branches, Git non  
c) Git est un système de versionnement en local, GitHub est une plateforme de collaboration en ligne  
d) Git et GitHub sont exactement la même chose  

---

**5. Vrai ou Faux :**  
> Il est possible d’utiliser Git sans GitHub.

<br>
<br>

# 🛠️ Git — Du démarrage au premier commit

Voici les étapes clés pour démarrer un projet avec Git, de l'initialisation jusqu'à l'enregistrement du premier commit.

---

## 1. 📁 Créer un dossier pour ton projet

Avant d’utiliser Git, crée un dossier pour ton projet :

`mkdir mon-projet`  
`cd mon-projet`

---

## 2. 🧩 Initialiser un dépôt Git

Pour indiquer à Git que ce dossier est un dépôt, utilise la commande :

`git init`

> Cette commande crée un sous-dossier `.git/` qui contient tous les fichiers de configuration et l'historique du projet.

---

## 3. 📝 Créer ou ajouter des fichiers

Tu peux maintenant ajouter des fichiers à ton projet, par exemple :

`touch index.html`

---

## 4. 🔍 Vérifier l'état du dépôt

Avant d’ajouter ou de valider des fichiers, tu peux consulter l’état de ton dépôt :

`git status`

Cela affichera les fichiers non suivis ou modifiés.

---

## 5. ➕ Ajouter les fichiers à la zone de staging

Avant de faire un commit, les fichiers doivent être ajoutés à la zone de préparation (staging area) :

`git add index.html`

Tu peux aussi tout ajouter :

`git add .`

---

## 6. ✅ Enregistrer les changements avec un commit

Une fois les fichiers ajoutés, tu peux enregistrer un **instantané** des changements :

`git commit -m "First commit : ADD index.html"`

---

## 7. 📜 (Optionnel) Vérifier l’historique des commits

Pour voir l’historique de ton dépôt :

`git log`

---

## 🚀 Résumé des commandes utilisées

- `mkdir mon-projet`  
- `cd mon-projet`  
- `git init`  
- `touch index.html`  
- `git status`  
- `git add index.html`  
- `git commit -m "Premier commit"`  
- `git log`


