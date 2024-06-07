
# Projet de Détection d'Objets avec YOLOv5

Ce projet implémente une solution de détection d'objets en temps réel en utilisant le modèle YOLOv5 et la bibliothèque OpenCV. Il permet de détecter et de sauvegarder des images de certains objets spécifiques (ordinateurs portables et souris) capturés par une webcam.

## Structure du Projet

- `detection.py`: Le script principal contenant les classes et les méthodes pour la détection d'objets et le traitement de flux vidéo.
- `yolov5s.pt`: Le modèle pré-entraîné YOLOv5 utilisé pour la détection.

## Prérequis

- Python 3.x
- OpenCV
- PyTorch
- Ultralytics YOLOv5

## Installation

1. Clonez ce dépôt :
    ```bash
    git clone https://github.com/votre-utilisateur/votre-projet.git
    cd votre-projet
    ```

2. Installez les dépendances nécessaires :
    ```bash
    pip install -r requirements.txt
    ```

3. Téléchargez le modèle YOLOv5s pré-entraîné et placez-le dans le répertoire du projet :
    ```bash
    wget https://github.com/ultralytics/yolov5/releases/download/v5.0/yolov5s.pt -O yolov5s.pt
    ```

## Utilisation

Pour lancer la détection d'objets en temps réel à partir de votre webcam, exécutez le script `detection.py` :
```bash
python detection.py
```

### Fonctionnalités

- **Détection d'objets** : Utilisation du modèle YOLOv5 pour détecter des objets dans le flux vidéo.
- **Filtrage des objets** : Détection et sauvegarde uniquement des ordinateurs portables et des souris.
- **Sauvegarde des images** : Les images des objets détectés sont sauvegardées dans des répertoires spécifiques selon le type d'objet.

## Code Expliqué

### Classe `ObjectDetection`

- **Initialisation** : Charge le modèle YOLOv5 et initialise les paramètres nécessaires.
- **Méthode `detect_objects`** : Détecte les objets dans une image donnée et retourne les objets cibles avec leurs coordonnées de délimitation.
- **Méthode `save_detection`** : Sauvegarde les images des objets détectés dans des répertoires spécifiques.

### Classe `CameraStream`

- **Initialisation** : Initialise la caméra et l'objet de détection.
- **Méthode `process_stream`** : Lit les images de la caméra en temps réel, applique la détection d'objets et affiche les résultats avec les annotations.

### Utilisation Principale

Le script démarre un flux vidéo à partir de la webcam par défaut, traite chaque image pour détecter les objets spécifiés, et affiche les résultats avec des annotations. Les objets détectés (ordinateurs portables et souris) sont sauvegardés dans des répertoires spécifiques.

## Contribution

Les contributions sont les bienvenues ! N'hésitez pas à soumettre des problèmes ou des pull requests pour améliorer ce projet.

## Licence

Ce projet est sous licence MIT. Veuillez consulter le fichier `LICENSE` pour plus de détails.
