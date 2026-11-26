# TP PyTorch : modèles génératifs sur MNIST

Ce projet contient un notebook pour charger et explorer MNIST, entraîner un
classificateur, un auto-encodeur et un auto-encodeur variationnel (VAE).

## Environnement (Windows, VS Code)

Python 3.11 est requis. À la racine du projet, dans le terminal PowerShell :

```powershell
uv python install 3.11
uv sync --python 3.11
```

`uv sync` crée l'environnement `.venv` et installe les dépendances déclarées
dans `pyproject.toml`. Pour l'activer manuellement :

```powershell
.\.venv\Scripts\Activate.ps1
```

Ouvrir `modeles_generatifs_mnist.ipynb`, choisir le noyau Python de `.venv`,
puis exécuter les cellules dans l'ordre. Le notebook télécharge MNIST au
premier lancement ; une connexion Internet est alors nécessaire. Il utilise
CUDA si disponible et sinon le processeur (CPU).

Les trois modèles sont configurés par défaut pour trois époques afin de rester
accessibles sur CPU. Augmenter `EPOCHS_CLASSIFIEUR`, `EPOCHS_AUTOENCODEUR` et
`EPOCHS_VAE` pour prolonger l'entraînement.