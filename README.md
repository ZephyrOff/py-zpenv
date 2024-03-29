# zpenv
# Langue/Language
[English Version](#EN-Informations)
# Informations
Outil multi-plateforme de gestion d'environnement virtuel Python pour la création, l'édition, la suppression ou le travail avec un environnement virtuel.<br>
Tout se passe directement en console.<br>
Il est possible de migrer ces anciens environnements virtuels sur cette solution.
## Prerequis
- Python 3
<br>

# Installation
```console
pip install zpenv
```
<br>

# Utilisation
## Affichage de toutes les commandes disponibles
```console
[user@host ~]$ zpenv -h
```
<br>

## Installation d'un environnement
```console
[user@host ~]$ zpenv --install [NomEnvironnement]
```
>- --name = Donner un nom à notre environnement
>- --tag = Ajouter des tags (séparés avec ,)
>- --comment = Ajouter un commentaire
>- --projectfolder = Spécifier le dossier du projet (emplacement du code)
>- --prompt = Spécifier le message dans le prompt
(D'autres options sont disponibles)
<br>

## Suppression d'un environnement
```console
[user@host ~]$ zpenv --remove [NomEnvironnement]
```
> --nopurge = Ne pas supprimer le dossier de l'environnement
Le dossier du projet ne sera jamais supprimé
<br>

## Migration d'un environnement
Permet de récupérer la gestion d'un environnement créé par venv ou virtualenv par exemple.
```console
[user@host ~]$ zpenv --migrate [CheminVersEnvironnement]
```
Si aucun chemin n'est spécifié, l'app prendra le répertoire courant.
<br><br>

## Lister les environnements disponibles
```console
[user@host ~]$ zpenv --list
- Project1
- Project2
```
<br>

## Afficher les informations d'un environnement
```console
[user@host ~]$ zpenv --info [NomEnvironnement]
Environment name:        Project1
Environment path:        C:\Users\zephyroff\Desktop\ENV
Environment version:     3.10.8
Environment tag:         ProjectConsole,TabBar
Project Folder:          C:\Users\zephyroff\Desktop\ENVCode
```
<br>

## Ouverture d'un environnement
Pour activer l'environnement virtuel et commencer à travailler dessus, il faut l'ouvrir.
```console
[user@host ~]$ zpenv --open [NomDeLEnvironnement]
```
> --shell = Pour entrer directement dans le shell Python
<br>

## Gestion de package
### Installer un package
```console
[user@host ~]$ zpenv --installmodule [package]
```
ou pour installer des packages depuis un fichier requirement
```console
[user@host ~]$ zpenv --requirement [RequirementFile]
```

### Supprimer un package
```console
[user@host ~]$ zpenv --removemodule [package]
```

### Mettre à jour un package
```console
[user@host ~]$ zpenv --upgrademodule [package]
```

### Installation de pip
```console
[user@host ~]$ zpenv --installpip
```
<br><br>

# EN - Informations
Cross-platform Python virtual environment management tool for creating, editing, deleting, or working with a virtual environment.<br>
Everything happens directly in console.<br>
It is possible to migrate these old virtual environments to this solution.
## Prerequisites
-Python 3
<br>

# Installation
```console
pip install zpenv
```
<br>

# Use
## Showing all available commands
```console
[user@host ~]$ zpenv -h
```
<br>

## Installing an environment
```console
[user@host ~]$ zpenv --install [EnvironmentName]
```
>- --name = Give a name to our environment
>- --tag = Add tags (separated with ,)
>- --comment = Add a comment
>- --projectfolder = Specify project folder (code location)
(Other options are available)
<br>

## Deleting an environment
```console
[user@host ~]$ zpenv --remove [EnvironmentName]
```
> --nopurge = Don't delete environment folder
The project folder will never be deleted
<br>

## Migrating an environment
Allows to recover the management of an environment created by venv or virtualenv for example.
```console
[user@host ~]$ zpenv --migrate [PathToEnvironment]
```
If no path is specified, the app will take the current directory.
<br><br>

## List available environments
```console
[user@host ~]$ zpenv --list
-Project1
-Project2
```
<br>

## Display environment information
```console
[user@host ~]$ zpenv --info [EnvironmentName]
Environment name: Project1
Environment path: C:\Users\zephyroff\Desktop\ENV
Environment version: 3.10.8
Environment tag: ProjectConsole,TabBar
Project Folder: C:\Users\zephyroff\Desktop\ENVCode
```
<br>

## Opening an environment
To activate the virtual environment and start working on it, you must open it.
```console
[user@host ~]$ zpenv --open [EnvironmentName]
```
> --shell = To enter the Python shell directly
<br>

## Package management
### Install a package
```console
[user@host ~]$ zpenv --installmodule [package]
```
or to install packages from a requirement file
```console
[user@host ~]$ zpenv --requirement [RequirementFile]
```

### Delete a package
```console
[user@host ~]$ zpenv --removemodule [package]
```

### Update a package
```console
[user@host ~]$ zpenv --upgrademodule [package]
```

### Install pip
```console
[user@host ~]$ zpenv --installpip
```