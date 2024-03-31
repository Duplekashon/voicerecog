# A Hackers AI Voice Assistant

## Running on native machine
### dependencies
* python3
* portaudio (for recording with pyaudio to work)
* [ctcdecode](https://github.com/parlance/ctcdecode) 

If you're on mac you can install `portaudio` using `homebrew`

### using virtualenv (recommend)
1. `virtualenv voiceassistant.venv`
2. `source voiceassistant.venv/bin/activate`

### pip packages
`pip install -r requirements.txt` 

## Running with Docker
### setup
If you are running with just the cpu
`docker build -f cpu.Dockerfile -t voiceassistant .`

If you are running on a cuda enabled machine 
`docker build -f Dockerfile -t voiceassistant .`

# Projet Voice Assistant

Ce projet contient du code et des ressources pour implémenter un assistant vocal.

## Structure des Répertoires

### fun\arnold_audio
- Contient des fichiers audio ou des ressources liées à la voix d'Arnold.

### VoiceAssistant\nlu
- **images**: Dossier contenant des images liées au réseau de neurones ou au jeu de données.
- **neuralnet**: Contient des fichiers et des scripts pour l'implémentation du réseau de neurones.
- **nlu_dataset**: Jeu de données utilisé pour l'entraînement ou les tests des modèles NLU.
- **scripts**: 
    - `__init__.py`: Fichier d'initialisation pour les packages Python.
    - `bash.sh`: Script bash pour diverses tâches, par exemple, la configuration de l'environnement, l'exécution de tâches, etc.
    - `engine.py`: Script principal gérant les fonctionnalités principales du NLU.
    - `meta_data.bin`: Fichier binaire contenant des métadonnées.
    - `readme.md`: Documentation fournissant des détails sur la partie NLU du projet.
    - `requirements.txt`: Liste des dépendances requises pour exécuter la partie NLU.

### speechrecognition
- **demo**:
   - Contient des fichiers de démonstration et des modèles illustrant le fonctionnement de la reconnaissance vocale.
   - `demo.html`: Modèle HTML pour l'interface de démonstration.
   - `demo.py`: Script Python pour les fonctionnalités de démonstration.

- **templates**:
  - Modèles HTML utilisés dans différentes parties du module de reconnaissance vocale.

- **neuralnet**:
  - Fichiers liés à l'implémentation du réseau de neurones dans le module de reconnaissance vocale, notamment :
      * dataset.py: Gère le chargement et la prétraitement des données du jeu de données,
      * model.py: Définit l'architecture du modèle de réseau de neurones,
      * optimize_graph.py: Script pour optimiser le graphe de calcul,
      * scorer.py: Évalue les performances du modèle,
      * train.dv: Script d'entraînement ou de validation des données.

## Pour Commencer

Suivez ces étapes pour configurer et exécuter le projet :

1. Clonez ce dépôt localement,
2. Accédez au répertoire VoiceAssistant\nlu,
3. Installez les dépendances avec la commande pip install requirements.txt,
4. Exécutez bash.sh pour effectuer les tâches de configuration initiale 
5. Lancez engine.py pour démarrer le moteur NLU,

Pour tester la reconnaissance vocale, accédez au répertoire speechrecognition\demo et exécutez demo.py après avoir configuré l'environnement comme indiqué dans le readme.md à l'intérieur du dossier nlu.


