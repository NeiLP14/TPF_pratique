# Application Flask - MariaDB

## Description

Application web Python avec Flask permettant de vérifier la connexion à une base de données MariaDB.

La page d'accueil affiche :
- Connected : si la connexion fonctionne.
- Disconnected : si la connexion échoue.

## Installation

Cloner le dépôt :

```bash
git clone https://github.com/NeiLP14/TPF_pratique.git
cd TPF_pratique
```

Créer un environnement virtuel :

```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
```

Installer les dépendances :

```bash
pip install -r requirements.txt
```

## Configuration

Configurer les variables d'environnement dans PowerShell :

```powershell
$env:DB_HOST="localhost"
$env:DB_USER="root"
$env:DB_PASSWORD="mot_de_passe"
$env:DB_NAME="test"
```

## Lancer l'application

```bash
python app.py
```

Ouvrir le navigateur :

http://localhost:5000

## Lancer avec Docker

Construire l'image :

```bash
docker build -t flask-mariadb-app .
```

Lancer le conteneur :

```powershell
docker run -d --name flask-app -p 5000:5000 flask-mariadb-app
```