# Mise en contexte et rappel de concepts de base

Les exercices suivants ont pour but de vous familiariser avec l’outil QGIS et ses fonctionnalités de base. Les données utilisées sont celles qui vous serviront pour votre projet par la suite.

## 1.1 Rappel sur les données (“couches”) utilisées dans les SIG

Toutes les données géographiques ont un point commun : elles ont une localisation dans l‘espace. On peut donc les représenter et les visualiser sur une carte. Pour représenter – de façon numérique – des données géographiques, il y a deux modes fondamentaux : le mode vecteur et le mode raster.

Dans un environnement SIG, les couches (données vecteur ou raster) composant une carte ont deux composantes : une composante spatiale (sa forme et son étendue géographique) et une composante attributaire (les informations qui lui sont associées).

Dans sa forme la plus simple, un raster, c’est une image. C’est même exactement ce qu’on imagine en pensant à une image numérique : un ensemble de pixels. Dans une donnée raster, chaque pixel contient une information (p.ex. code couleur), que l’on appelle “band” (en Anglais). Un même raster peut contenir plusieurs “bands” (donc plusieures couches d’information dans chaque pixel).

Les vecteurs ne sont pas composés de pixels. Les vecteurs sont des « dessins mathématiques », c’est-à-dire des géométries décrites par des paramètres cartésiens spécifiés en 2 ou 3 dimensions. Ainsi, vous pouvez “zoomer” infiniment sur une couche vecteur sans que celle-ci ne se “pixelise”. On parle également de dessins vectoriels ou d’images vectorielles. Un des formats de fichiers vecteur le plus couramment utilisé est le ESRI Shapefile, qui se compose en fait d’au moins trois fichiers (ayant tous le même nom, mais une extension différente) :

Un fichier terminant par l’extension «.shp» contenant la géométrie
Un fichier terminant par l’extension «.dbf» contenant les attributs de chaque élément géométrique
Un fichier terminant par l’extension «.shx» contenant l’index reliant chaque géométrie à ses attributs
(Optionnel) un fichier terminant par l’extension « .prj » contenant le système de projection de la couche vectorielle

L’ESRI shapefile n’est pas le seul format de données vectoriel. Le “geopackage” est un autre format couramment utilisé et certainement plus pratique car il réunit tous les éléments susmentionnés en un seul fichier (se terminant par l’extension “.gpkg”).

## 1.2 GeoPandas Project

Dans un projet GeoPandas, nous faisons référence à l'ensemble des données spatiales et des tâches d'analyse organisées au sein d'un environnement Python. GeoPandas nous permet de travailler avec différents types de données géospatiales, notamment des données vectorielles telles que des fichiers shapefile, GeoJSON ou gpkg. Ces ensembles de données sont importés dans GeoPandas, où nous pouvons les manipuler, les analyser et les visualiser à l'aide de code Python.

Il est pratique de directement sauvegarder le projet dans votre dossier de travail (dossier contenant toutes les données vecteur et raster) et de le sauvegarder régulièrement tout au long des exercices.
