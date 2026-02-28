# Décrypter le Transformer : Création d'un mini-GPT

## Objectif du projet
L'objectif principal de ce Bureau d'Études (BE) est de se familiariser en profondeur avec l'architecture Transformer. Plus concrètement, il s'agit de s'approprier le code vu en cours pour entraîner notre propre modèle de génération de texte de type GPT.

Dans ce cadre, notre travail s'est divisé en deux axes : 
1. L'étude de l'impact des hyperparamètres sur l'apprentissage et les performances du modèle.
2. L'exploration de deux stratégies d'amélioration pour la génération de texte : l'implémentation d'un algorithme de *Beam Search* et le passage à un tokenizer plus complexe.

Afin de mesurer objectivement nos résultats au fil des expériences, nous nous sommes appuyés sur les métriques proposées dans le sujet : la perplexité, la diversité lexicale et le taux d'hallucination.

## Structure du dépôt

Notre travail est réparti sur trois notebooks distincts pour plus de clarté :

* **`Etude_hyperparametre.ipynb`** : Ce notebook vise à étudier l'influence des différents hyperparamètres (taille du contexte, nombre de têtes d'attention, nombre de blocs) sur la qualité du texte généré, la loss et le temps de calcul.
* **`BEAM_SEARCH.ipynb`** : Exploration d'une méthode de génération alternative. Nous y implémentons un Beam Search, une méthode déterministe permettant d'évaluer plusieurs pistes en parallèle pour trouver la séquence globale la plus probable.
* **`BPE.ipynb`** : Changement de stratégie de tokenisation. 