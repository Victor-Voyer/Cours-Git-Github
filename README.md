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

<br>
<br>

# 🔍 Git — La commande `git diff`

La commande `git diff` permet de **voir les changements** ligne par ligne entre :

- le **code actuel** et la **dernière version validée** (commit),
- la **zone de staging** et la **dernière version validée**,
- ou entre **deux commits**, **deux branches**, etc.
<br>

En résumé la commande **`git diff`** permet de pouvoir compararer deux versions de notre code, entre deux commit.

---

## 💡 Utilisations courantes

### 1. Voir les modifications non ajoutées au staging

```bash
git diff
```

<br>
<br>

## Que fait `git status` ?

Cette commande vous informe sur :

- ✅ **Les fichiers modifiés mais non indexés**  
  *(non ajoutés avec `git add`)*

- ✅ **Les fichiers stagés (indexés) prêts à être commités**

- ✅ **Les fichiers non suivis (untracked)**  
  *(nouveaux fichiers qui ne sont pas encore dans le suivi Git)*

- ✅ **Les fichiers supprimés ou renommés**

- ✅ **La branche active**  
  *(et si elle est en avance ou en retard par rapport à sa branche distante)*

En résumé le **`git status`** nous permet de voir toutes les modifications entre deux **`git commit`**

  <br>

## Commande `git status`

La commande `git status` est utilisée pour afficher l'état actuel de l'index et de l'arborescence de travail dans un dépôt Git.

## Syntaxe de base

```bash
git status
```

<br>
<br>

## Que fait `git log` ?

Cette commande affiche l'historique des commits dans un dépôt Git. Elle vous informe sur :

- 📌 **Les identifiants uniques des commits** 

- 👤 **L’auteur de chaque commit**  
  *(nom et adresse email)*

- 🕒 **La date et l’heure du commit**

- 📝 **Le message de commit**  
  *(description des modifications apportées)*

- 🌿 **La branche et les tags associés** 

- 🔀 **La structure des branches et des fusions**

---

### Exemples d'options utiles

- `git log --oneline` : Affiche chaque commit sur une seule ligne
- `git log --graph` : Affiche un graphe ASCII de l’historique
- `git log --decorate` : Affiche les noms des branches et tags
- `git log --all` : Montre les commits de toutes les branches


<br>
<br>

## Que fait `git checkout` ?

La commande `git checkout` permet de naviguer entre les branches, de restaurer des fichiers ou de revenir à un commit spécifique. Elle peut être utilisée pour :

- 🌿 **Changer de branche**  
  *(ex. : `git checkout nom-de-branche`)*

- ✨ **Créer une nouvelle branche et s’y positionner**  
  *(ex. : `git checkout -b nouvelle-branche`)*

- 🛠️ **Restaurer un fichier modifié depuis l'index ou un commit**  
  *(ex. : `git checkout HEAD -- chemin/fichier.txt`)*

- 🕒 **Se déplacer à un commit spécifique**  
  *(ex. : `git checkout abc1234` pour un commit précis — mode détaché)*

---

### Cas d’usage courants

| Commande                              | Action effectuée                                              |
|---------------------------------------|---------------------------------------------------------------|
| `git checkout dev`                    | Change vers la branche `dev`                                 |
| `git checkout -b feature/login`       | Crée et passe à une nouvelle branche `feature/login`         |
| `git checkout -- index.html`          | Restaure le fichier `index.html` depuis l'index              |
| `git checkout abc1234`                | Passe à un commit spécifique (mode détaché)                  |

---

### Remarques

- Depuis Git 2.23, `git checkout` a été partiellement remplacée par deux commandes plus spécifiques :
  - `git switch` (pour changer de branche)
  - `git restore` (pour restaurer des fichiers)

> 💡 **Bon à savoir :** utiliser `git checkout` peut écraser des modifications locales si elles ne sont pas commités ou sauvegardées.

<br>
<br>

## Que fait `git restore` ?

La commande `git restore` permet d’annuler ou de restaurer des modifications apportées à des fichiers dans l’espace de travail ou dans l’index. Elle est introduite à partir de Git 2.23 pour remplacer certains usages ambigus de `git checkout`.

### Elle peut être utilisée pour :

- 🔄 **Annuler des modifications locales**  
  *(restaurer un fichier à son état dans le dernier commit)*  
  ➤ `git restore fichier.txt`

- 🔙 **Retirer un fichier de l'index**  
  *(le fichier reste modifié mais n’est plus en attente de commit)*  
  ➤ `git restore --staged fichier.txt`

- 💾 **Restaurer un fichier depuis un commit spécifique**  
  ➤ `git restore --source=HEAD~1 fichier.txt`

---

### Cas d’usage courants

| Commande                                  | Action effectuée                                               |
|-------------------------------------------|----------------------------------------------------------------|
| `git restore index.html`                  | Remplace `index.html` par la version du dernier commit         |
| `git restore --staged index.html`         | Retire `index.html` du staging area                            |
| `git restore --source=commit_id fichier`  | Restaure le fichier depuis un commit spécifique                |
| `git restore .`                           | Restaure tous les fichiers modifiés (attention !)              |

---

### Comparaison rapide : `restore` vs `checkout`

| Action                                   | Ancienne méthode (`checkout`)      | Nouvelle méthode (`restore`)          |
|------------------------------------------|-------------------------------------|----------------------------------------|
| Annuler les changements d’un fichier     | `git checkout -- fichier.txt`      | `git restore fichier.txt`              |
| Retirer un fichier du staging            | `git reset HEAD fichier.txt`       | `git restore --staged fichier.txt`     |

> ✅ **Recommandé** : Utiliser `git restore` pour une meilleure clarté et éviter les erreurs liées à `git checkout`.

---

### Astuce

Vous pouvez combiner `--source` avec `--staged` pour restaurer un fichier dans l’index sans toucher au fichier de travail :

```bash
git restore --source=HEAD --staged fichier.txt
```

<br>
<br>

## Que fait `git reset` ?

La commande `git reset` permet de réinitialiser la position de la branche actuelle, de retirer des fichiers du staging area (index), ou d’annuler des commits. Elle peut modifier l’index **et** l’arborescence de travail, selon les options utilisées.

---

### Elle peut être utilisée pour :

- 🔙 **Annuler un commit sans supprimer les modifications dans les fichiers**  
  ➤ `git reset --soft HEAD~1`

- ♻️ **Annuler un commit et retirer les fichiers du staging**  
  ➤ `git reset --mixed HEAD~1` (par défaut)

- ❌ **Annuler un commit et écraser les modifications dans les fichiers**  
  ➤ `git reset --hard HEAD~1`

- 🛠️ **Retirer un ou plusieurs fichiers du staging**  
  ➤ `git reset HEAD fichier.txt`

---

### Types de `reset`

| Option       | Effet sur les commits | Effet sur l’index (staging) | Effet sur l’arborescence de travail |
|--------------|------------------------|------------------------------|--------------------------------------|
| `--soft`     | 🔁 Réécrit HEAD         | ✅ Garde les fichiers dans l’index     | ✅ Garde les modifications locales    |
| `--mixed`    | 🔁 Réécrit HEAD         | ❌ Retire les fichiers du staging      | ✅ Garde les modifications locales    |
| `--hard`     | 🔁 Réécrit HEAD         | ❌ Vide le staging                    | ❌ Réinitialise les fichiers locaux   |

---

### Cas d’usage courants

| Commande                              | Action effectuée                                           |
|---------------------------------------|------------------------------------------------------------|
| `git reset HEAD fichier.txt`          | Retire un fichier du staging, sans toucher aux modifs      |
| `git reset --soft HEAD~1`            | Annule le dernier commit, conserve staging et modifs       |
| `git reset --mixed HEAD~1`           | Annule le dernier commit, vide staging, garde modifs       |
| `git reset --hard HEAD~1`            | Annule commit, staging et modifications locales (⚠️)        |

---

### ⚠️ Attention

- `git reset --hard` est **destructif** : les modifications locales sont **perdues**.
- Pour annuler un `reset`, vous pouvez parfois utiliser `git reflog` pour retrouver l'ancien HEAD.

---

### Alternative : `git restore`

Pour retirer un fichier du staging sans toucher aux autres :

```bash
git restore --staged fichier.txt
``` 
<br>
<br>

# 🧠 Les Conflits de Merge

## 📌 Qu'est-ce qu'un Conflit de Merge ?

Un **conflit de merge** se produit lorsque Git ne peut pas fusionner automatiquement deux branches car des modifications incompatibles ont été apportées à la même partie du code dans les deux branches.

### Exemple :
- Branche `main` : ligne 10 → `color: red;`
- Branche `feature` : ligne 10 → `color: blue;`

Git ne peut pas deviner quelle couleur choisir.

---

## 🔧 Quand les Conflits Se Produisent-ils ?

1. Lors d’un `git merge` entre deux branches avec des modifications sur les **mêmes lignes** d’un fichier.
2. Lors d’un `git rebase` si les commits réécrits chevauchent des modifications existantes.
3. Lors d’un `git pull` si la branche locale a divergé de la branche distante.

---

## 🧭 Comment Savoir s’il y a un Conflit ?

Après un `git merge`, Git affiche un message d’erreur :

```bash
Auto-merging fichier.txt
CONFLICT (content): Merge conflict in fichier.txt
Automatic merge failed; fix conflicts and then commit the result.
```

<br>
<br>

## 🛠️ Résoudre un Conflit Étape par Étape

### 1. Ouvrir le fichier en conflit

Git ajoute des **marqueurs de conflit** pour indiquer les parties modifiées :

```text
<<<<<<< HEAD
Contenu depuis la branche actuelle
=======
Contenu depuis la branche fusionnée
>>>>>>> feature
```
### 2. Choisir quoi garder

✅ Garder une des deux versions.  
✅ Combiner les deux manuellement.  
✅ Réécrire entièrement selon les besoins.

🧽 **N’oubliez pas de supprimer les marqueurs** (`<<<<<<<`, `=======`, `>>>>>>>`) !

### 3. Ajouter le fichier résolu

```bash
git add fichier.txt
```
### 4. Terminer le merge

```bash
git commit
```
## 🧰 Outils Utiles pour Résoudre les Conflits

- **Visual Studio Code** : propose des boutons pour accepter une version, l’autre, ou les deux.
- **KDiff3**, **Meld**, **Beyond Compare**, etc. : outils de fusion visuelle.
- `git mergetool` : lance un outil graphique configuré pour résoudre les conflits.

## 🚫 Annuler un Merge en Conflit

Si vous voulez annuler un merge (non terminé) :

```bash
git merge --abort

git rebase --abort
```

<br>

## ✅ Bonnes Pratiques

- 💾 Faire des commits fréquents.
- 🔄 Tirer (`git pull`) régulièrement pour éviter trop de divergences.
- 🌿 Utiliser des branches courtes et isolées.
- 👀 Relire les modifications conflictuelles avant de les valider.