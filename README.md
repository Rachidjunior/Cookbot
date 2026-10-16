# 🤖 CookBot

> **Pipeline d'apprentissage par imitation pour un bras manipulateur X-Arm 7 : de la collecte de démonstrations en simulation au transfert sim-to-real.**

Ce dépôt centralise le code de **CookBot**, un projet académique de Robot Learning (IMT Atlantique). Ce projet consiste à mettre en place un setup en simulation pour permettre l'apprentissage par imitation d'un bras robotique X-Arm 7 en collectant des données de démonstrations par téléopération pour former un dataset au format LeRobot. L'objetif final du projet est de réaliser un transfert sim-to-real sur un bras robotique X-Arm 7 déjà présent dans les laboratoires de l'école.

## Objectifs du projet

Le pipeline de développement s'articule autour de trois grands axes :

1. **Simulation & Téléopération :** Mise en place d'un environnement simulé (ex:Isaac Sim) permettant de contrôler un bras X-Arm 7 (7 DDL) afin de réaliser des tâches culinaires (mélanger, verser) et d'enregistrer des trajectoires expertes.
2. **Collecte et formatage des données :** Enregistrement des actions (joints, positions) et des observations (caméras, proprioception) pour générer des datasets standardisés compatibles avec la librairie [LeRobot](https://github.com/huggingface/lerobot).
3. **Apprentissage VLA & Transfert (Sim-to-Real) :** Entraînement de modèles de fondation robotique de type **Vision-Language-Action (VLA)** sur les données collectées. L'objectif est d'apprendre au robot à prédire des actions motrices à partir d'observations visuelles et d'instructions en langage naturel en simulation, avant de transférer ces capacités sur le robot physique.

## Structure du dépôt (en cours de construction)

\`\`\`text
CookBot/
├── simulation/      # Scripts pour lancer l'environnement virtuel et configurer le X-Arm 7
├── teleoperation/   # Outils de contrôle à distance pour générer les démonstrations
├── lerobot_utils/   # Scripts de conversion et de formatage des données au format LeRobot
├── training/        # Scripts d'entraînement des modèles d'imitation
└── README.md
\`\`\`

*(Note : L'architecture évoluera à mesure que les différents modules seront implémentés).*

## Installation & Prérequis

### Prérequis systèmes
* **OS :** Linux (Ubuntu recommandé)
* **Python :** `3.10` ou supérieur
* **Gestionnaire d'environnement :** `conda` ou `venv` recommandé

### Installation de l'environnement de développement

1. **Cloner le dépôt :**
   \`\`\`bash
   git clone https://github.com/Rachidjunior/Cookbot.git
   cd CookBot
   \`\`\`

2. **Créer et activer un environnement virtuel :**
   \`\`\`bash
   python -m venv venv
   source venv/bin/activate
   \`\`\`

3. **Installer les dépendances (À venir) :**
   *Un fichier `requirements.txt` ou `pyproject.toml` sera ajouté prochainement pour installer l'environnement de simulation et la stack LeRobot.*

## Contribution

Si vous êtes collaborateur sur ce projet :
1. Créez une nouvelle branche pour votre fonctionnalité : `git checkout -b feature/nom-de-la-fonctionnalite`
2. Testez votre code localement.
3. Poussez vos modifications : `git push origin feature/nom-de-la-fonctionnalite`
4. Ouvrez une **Pull Request** sur GitHub pour relecture avant fusion dans la branche principale (`main`).

---
*Projet mené dans le cadre des études d'ingénieur à l'IMT Atlantique.*
