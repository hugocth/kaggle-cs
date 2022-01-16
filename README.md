# CentraleSupélec ML2022 - Kaggle Project

Hello les gens, je vous écris un README rapide comme ça tout le monde bossera sur le même environnement, ça facilitera le debug.

## Téléchargement de tous les fichiers utiles

Avant tout, faites un git clone de ce repo dans un fichier sur votre ordi. Etant donné que GitHub ne permet pas d'upload des fichiers de plus de 100Mo, il faudra rajouter les fichiers `train.geojson` et `test.geojson` à la main dans ce dossier, à partir de ce lien :

`https://www.kaggle.com/c/centralesypelec-ml2022-course/data`

## Setup de l'environnement commun 

Lancez un terminal anaconda (le plus intuitif est de lancer VSCode avec Anaconda et d'ouvrir un terminal shell ou bash).
Pour créer l'environnement, exécuter :

`conda create -n ML_geopandas python=3.7`

Puis, pour activer l'environnement :

`conda activate ML_geopandas`

Pour installer le module le plus chiant, on utilisera conda :

`conda install geopandas -c conda-forge`

Puis (croyez moi c'est vraiment important j'ai galéré pour trouver mdr) :

`pip uninstall rtree`

Cependant, sur windows, il y a de fortes chances que, lors de l'installation, il y ait cette erreur : 

`error: Microsoft Visual C++ 14.0 or greater is required. Get it with "Microsoft C++ Build Tools": https://visualstudio.microsoft.com/visual-cpp-build-tools/`

Dans ce cas, il faut suivre le lien et télécharger l'IDE Visual Studio, puis, lors de l'installation, télécharger Visual C++ (attention ça prend à peu près 7Go d'espace).

Pour installer les autres modules nécessaires, exécuter :

`python -m pip install --user -r requirements.txt`

## Utiliser l'environnement comme kernel sur un jupyter notebook

Pour rajouter l'environnement à la liste des kernels :

`(ML_geopandas)$ ipython kernel install --name ML_geopandas --user`

Pour lancer le notebook :

`(ML_geopandas)$ jupyter notebook KaggleProject.ipynb`

## Test pour savoir si tout fonctionne bien

Exécuter les 2 premières cellules (en gros toute la section "Test code"). Si à la fin le print "Everything is fine !" se passe bien, alors tout est bon !

## Une autre option : utiliser Google Colab

Il y a un bon moyen d'éviter les problèmes d'installation : c'est de lancer tout le projet dans un google colab. J'ai créé un repo github dont l'URL est :

`https://github.com/hugocth/kaggle-cs`

Vous n'avez qu'à suivre les instructions de ce tuto de Stanford pour lancer le projet dans le colab :

`https://cs230.stanford.edu/section/2/colab.pdf`

Il faudra alors mettre les fichiers `test.geojson` et `train.geojson` dans votre Google Drive et suivre ce tuto pour les importer dans l'espace de travail Colab :

`https://colab.research.google.com/notebooks/io.ipynb`
