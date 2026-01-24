# Projets de Calcul Quantique (QComp) et Quantum Machine Learning (QML) - CentraleSupélec

Ce dépôt rassemble les travaux pratiques et projets réalisés dans le cadre des modules Quantum Computing (QComp) et Quantum Machine Learning (QML) à CentraleSupélec (Promotion 2025/2026). L'objectif de ces travaux est d'explorer l'implémentation d'algorithmes quantiques complexes, de la synthèse d'oracles arithmétiques à la simulation de systèmes dynamiques pour la prédiction de séries temporelles.

## 1. Algorithmique Quantique (Cours QComp)

Cette section est dédiée à la résolution de systèmes linéaires et à l'optimisation de circuits quantiques.

* Implémentation de HHL (Harrow-Hassidim-Lloyd) : De la version naïve à la version optimisée pour la résolution de systèmes Ax = b.
* Estimation de Phase Quantique (QPE) : Utilisation de la QPE pour l'extraction des valeurs propres.
* Simulation Hamiltonienne (Trotterisation) : Analyse de la décomposition de Suzuki-Trotter (ordres 1 et 2) pour simuler l'évolution temporelle e^(iAt).
* Arithmétique Réversible : Conception de circuits pour l'addition, la multiplication et la synthèse de fonctions par développement de Taylor (oracle d'inversion 1/x).
* Optimisation de Circuits : Algorithmes de réduction du nombre de portes et suppression des contrôles redondants pour les architectures NISQ.

## 2. Quantum Machine Learning (Cours QML)

Travaux portant sur l'utilisation de l'espace de Hilbert comme espace de projection pour l'apprentissage automatique.

### Quantum Kernel Methods
* Quantum Embedding : Étude de différentes feature maps (Phase encoding, ZFM, ZZFM).
* Calcul de Fidélité : Comparaison entre la méthode Adjoint et le Swap Test pour mesurer la similarité entre états.
* Clustering Quantique : Application aux jeux de données Iris et Blobs via le Spectral Clustering.
* Simulation de Bruit : Test de robustesse des noyaux quantiques sur un modèle de bruit réel (FakeBrisbane).

### Quantum Reservoir Computing (QRC)
* Modélisation de Spins : Simulation de la dynamique d'un réservoir de spins interagissant via un Hamiltonien de type Ising à champ transverse.
* Prédiction de Séries Temporelles : Application à l'attracteur chaotique de Lorenz.
* Multiplexage Temporel : Utilisation de nœuds virtuels pour enrichir la dimensionnalité des caractéristiques extraites sans augmenter le nombre de qubits physiques.

## 3. Documentation et Rapport

Le dossier `report/` contient le rapport détaillé rédigé en LaTeX. Ce document présente :
* Les démonstrations mathématiques et analyses théoriques.
* Les captures d'écran des circuits synthétisés.
* L'étude de la convergence de l'erreur en fonction du nombre d'itérations de Trotter.
* Les résultats des benchmarks sur les simulateurs de bruit.

## 4. Installation et Utilisation

### Prérequis
* Python 3.10 ou supérieur.
* Un gestionnaire d'environnement virtuel (venv).

### Configuration de l'environnement
```bash


# Créer et activer l'environnement virtuel
python -m venv .venv
source .venv/bin/activate  # Sur Windows utilisez: .venv\Scripts\activate

# Installer les dépendances
pip install -r requirements.txt