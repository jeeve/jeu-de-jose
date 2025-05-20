# Jeu de José

Ce projet implémente une simulation du casse-tête classique de la traversée de rivière, souvent connu sous le nom de "Missionnaires et Cannibales". Dans cette version, nous avons des "humains" et des "orques".

Le problème est configuré comme suit :
- Il y a 3 humains et 3 orques sur la rive droite d'une rivière.
- Le but est de déplacer les 3 humains sur la rive gauche.
- Un bateau est disponible, mais il ne peut transporter qu'un maximum de 2 individus à la fois.
- La règle cruciale : Sur aucune des rives, ni dans le bateau pendant le transit (implicitement, car le contenu du bateau forme un groupe temporaire sur une rive ou au milieu de la rivière), les humains ne peuvent être en infériorité numérique par rapport aux orques. Si des humains sont présents, ils doivent être en nombre égal ou supérieur à celui des orques. Si aucun humain n'est présent sur une rive, le nombre d'orques n'a pas d'importance (par exemple, si tous les humains sont sur l'autre rive).

## Contenu du Dépôt

- **`Jeu_de_José.ipynb`** : Un notebook Jupyter qui contient le code Python pour la simulation.
    - Il définit une classe `JeuDeJose` qui modélise la logique du casse-tête, y compris l'état des rives, le mouvement du bateau et la validation des règles.
    - Le notebook exécute ensuite la simulation plusieurs fois pour trouver une solution optimale (celle avec le moins de déplacements) et affiche la séquence de ces déplacements.

## Comment Exécuter

La simulation est contenue dans le notebook Jupyter `Jeu_de_José.ipynb`. Pour l'exécuter :

1.  **Environnement** : Vous aurez besoin d'un environnement capable d'exécuter des notebooks Jupyter.
    *   **Google Colab** : Le notebook inclut un lien pour l'ouvrir directement dans Google Colab, qui est un environnement gratuit basé sur un navigateur. C'est le moyen le plus simple de l'exécuter.
        ```
        <a href="https://colab.research.google.com/github/jeeve/Jeu-de-Jose/blob/main/Jeu_de_Jos%C3%A9.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Ouvrir dans Colab"/></a>
        ```
    *   **Environnement Jupyter Local** : Si Python est installé, vous pouvez configurer un environnement Jupyter local.
        *   Installez JupyterLab ou Jupyter Notebook :
            ```bash
            pip install jupyterlab
            # ou
            pip install notebook
            ```
        *   Accédez au répertoire du dépôt et exécutez :
            ```bash
            jupyter lab
            # ou
            jupyter notebook
            ```
        *   Ouvrez le fichier `Jeu_de_José.ipynb` depuis l'interface Jupyter.

2.  **Exécution de la Simulation** : Une fois le notebook ouvert, vous pouvez exécuter les cellules séquentiellement. La dernière cellule exécute la simulation et affichera les étapes de la meilleure solution trouvée.
