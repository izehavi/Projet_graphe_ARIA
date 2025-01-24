# Analyse du Sur-apprentissage des Réseaux de Neurones avec la GFT

Ce projet explore l'utilisation de la **Transformée de Fourier sur Graphe (Graph Fourier Transform, GFT)** pour analyser le sur-apprentissage (**overfitting**) dans les réseaux de neurones. En combinant des notions de traitement du signal sur graphe et l'analyse des activations neuronales, nous avons mis en œuvre une méthode permettant de détecter et de caractériser le sur-apprentissage à travers une approche spectrale.

## Contenu du projet

### **1. Rapport**
Le rapport détaillé, intitulé **`rapport_GFT_overfiting.pdf`**, explique les concepts mathématiques et les méthodes utilisées pour cette étude, notamment :
- Une introduction théorique à la GFT.
- L'application de la GFT pour analyser les activations des réseaux de neurones.
- Une étude pratique utilisant un autoencodeur pour illustrer les différences entre un modèle ayant sur-appris et un modèle généralisant.

### **2. Code**
Le fichier **`FCNN_GFT.ipynb`** est un notebook Jupyter contenant :
- L'implémentation des outils de construction de graphes à partir des poids des réseaux de neurones.
- Les calculs des activations des neurones et de leur GFT.
- Une analyse visuelle des spectres GFT des activations neuronales pour comparer un modèle ayant sur-appris et un modèle généralisant.

## Résultats principaux

- **Observation des spectres GFT** : 
  - Les modèles ayant sur-appris présentent une forte proportion de composantes haute fréquence dans leur spectre GFT, reflétant des activations complexes et spécifiques aux données d'entraînement.
  - Les modèles généralisants sont dominés par des composantes basse fréquence, indiquant des activations régulières et globales.
  
- **Perspectives** :
  - Cette méthode pourrait être étendue à d'autres architectures de réseaux de neurones, comme les réseaux convolutifs.
  - Une application intéressante serait le développement d'un outil dynamique détectant le sur-apprentissage en temps réel pendant l'entraînement.

## Structure des fichiers

- **`rapport_GFT_overfiting.pdf`** : Rapport complet détaillant les résultats et la méthodologie.
- **`FCNN_GFT.ipynb`** : Notebook Jupyter contenant le code Python pour reproduire les expériences.

## Instructions pour l'utilisation du code

### **Prérequis**
Assurez-vous d'avoir les bibliothèques suivantes installées dans votre environnement Python :
- `numpy`
- `matplotlib`
- `networkx`
- `torch`
- `scipy`

Vous pouvez installer les dépendances avec la commande suivante :
```bash
pip install numpy matplotlib networkx torch scipy
