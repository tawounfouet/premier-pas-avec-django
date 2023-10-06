


## Création et activation d'un environnement virtuel
```bash
virtualenv myprojectenv
source myprojectenv/bin/activate
```




## Installation de django et création d'un projet
```bash
# Installation de la version officielle de django
python -m pip install Django

# Vérification de la version de django installée
python -m django --version


# Sauvegarde des dépendances dans un fichier requirements.txt
pip freeze > requirements.txt

# Creatiion d'un projet
django-admin startproject mysite
```


## Lancement du serveur de développement
```bash
cd src 
python manage.py runserver


# Modification du port d'écoute
python manage.py runserver 8080
```

## Initialisation du depot git
```bash
git init
git add .
git commit -m "Initial commit"
```

## Création du fichier .gitignore
```bash
# Création du fichier .gitignore
touch .gitignore

# Ajout des fichiers à ignorer
echo "myprojectenv/" >> .gitignore
echo "db.sqlite3" >> .gitignore
echo "*.pyc" >> .gitignore
echo "__pycache__/" >> .gitignore
echo "local_settings.py" >> .gitignore
echo ".DS_Store" >> .gitignore
echo ".idea/" >> .gitignore
echo ".vscode/" >> .gitignore
echo ".venv/" >> .gitignore
echo "env/" >> .gitignore
echo "venv/" >> .gitignore
```


## Création de l’application Polls
```bash
python manage.py startapp polls
```


## Configuration de la base de données
```bash
# création des tables dans la base de données
python manage.py migrate

# Exécuter les makemigrations pour indiquez à Django que vous avez effectué des changements aux modèles
python manage.py makemigrations polls

# Vérification de la conformité du projet
 python manage.py check

# exécutez à nouveau la commande migrate pour créer les tables des modèles dans votre base de données
python manage.py migrate
``` 

## Introduction au site d’administration de Django
```bash
# Création d'un superutilisateur
python manage.py createsuperuser
username: admin
email: admin@example.com
password: password123 ou admin

# Lancement du serveur de développement
python manage.py runserver

#À présent, ouvrez un navigateur Web et allez à l’URL « /admin/ » de votre domaine local – par exemple, http://127.0.0.1:8000/admin/
```