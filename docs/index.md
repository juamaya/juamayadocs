# Welcome to MkDocs

![MkDocs](img/mkdocs.jpg)

For full documentation visit [mkdocs.org](https://www.mkdocs.org).




## Installation

>To install MkDocs, run the following command from the command line:


```sh
pip install mkdocs


```
 
 

## Creating a new project

>  To create a new project, run the following command from the command line:


```sh
mkdocs new my-project
cd my-project

``` 

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.


## Publicando su sitio



##  <mark>1. Usando MkDocs </mark>

>Si prefiere implementar la documentación de su proyecto manualmente, puede simplemente invocar el siguiente comando desde el directorio que contiene el archivo:  mkdocs.yml

```sh
mkdocs build
```

```sh
mkdocs gh-deploy --force
```
###  CREAR REPOSITORIO LOCAL

> En la consola situada en la carpeta del proyecto escribimos el comando:

```sh

  git init

  git add .

  git status

  git commit -m "mi primer commit"


```

###  CREAR REPOSITORIO REMOTO

> En la consola situada en la carpeta del proyecto escribimos el comando:

```sh

  git branch -M main

  git remote add origin https://github.com/juamaya/juamayadocs.git

  git push -u origin main

```
###  CONFIGURAR EN TU REPOSITORIO EN GitHub Settings/ Pages

 

---

####  Build and deployment

> source:
> <mark>Deploy from a branch</mark>

![sandero_2024](images/sandero.jpg)

## <mark> 2. Usando GitHub Actions </mark>

>Usando GitHub Actions puedes automatizar la implementación de la documentación de tu proyecto. En la raíz de su repositorio, cree un nuevo flujo de trabajo de GitHub Actions, por ejemplo .github/workflows/deploy.yml, y copie y pegue el siguiente contenido:

```yml

name: deploy 
on:
  push:
    branches:
      - master 
      - main
permissions:
  contents: write
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Configure Git Credentials
        run: |
          git config user.name github-actions[bot]
          git config user.email 41898282+github-actions[bot]@users.noreply.github.com
      - uses: actions/setup-python@v5
        with:
          python-version: 3.x
      - run: echo "cache_id=$(date --utc '+%V')" >> $GITHUB_ENV 
      - uses: actions/cache@v4
        with:
          key: mkdocs-material-${{ env.cache_id }}
          path: .cache
          restore-keys: |
            mkdocs-material-
      - run: pip install mkdocs-material 
      - run: mkdocs gh-deploy --force


```

 
###  CONFIGURAR EN TU REPOSITORIO EN GitHub Settings/ Pages

---

####  Build and deployment

> source:
> <mark>GitHub Actions</mark>



---


###  SUBIR CAMBIOS AL REPOSITORIO.

En la consola situada en la carpeta del proyecto escribimos el comando:

```

  git add .

  git commit -m "cambios realizados."

  git push


```


# <mark> JUAMAYA 🍺 2024</mark>
