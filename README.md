# Annuaire des sapeurs-pompiers de Vienne

Annuaire téléphonique interne du centre, consultable depuis un téléphone.
Un seul fichier, aucune dépendance, aucun serveur : `index.html`.

## Accès

Les coordonnées ne figurent pas en clair dans le code. Elles sont chiffrées
(AES-256-GCM, clé dérivée par PBKDF2-SHA256, 300 000 itérations) et ne
s'affichent qu'après saisie du code du centre. Le code n'est écrit nulle part
dans ce dépôt : il se transmet de vive voix au centre.

Le code n'est demandé qu'une fois par appareil.

## Mise en ligne (GitHub Pages)

1. Créer un dépôt et y déposer `index.html` à la racine.
2. Settings → Pages → Source : `Deploy from a branch`, branche `main`, dossier `/ (root)`.
3. Attendre une minute, puis ouvrir l'adresse indiquée par GitHub.

Sur iPhone, ouvrir l'adresse dans Safari puis Partager → « Sur l'écran d'accueil ».
Sur Android, Chrome → menu → « Ajouter à l'écran d'accueil ».

## Fonctions

- Recherche par nom, prénom ou fragment de numéro, insensible aux accents
- Filtres SPP / SPV / statut I et liste de favoris propre à chaque téléphone
- Appel direct et SMS en un geste, index alphabétique latéral
- Affichage clair ou sombre selon le réglage du téléphone

## Mise à jour de la liste

Les données sont chiffrées dans `index.html` : elles ne se modifient pas à la
main. Pour intégrer une nouvelle version de la liste du centre, il faut
régénérer le fichier à partir des données à jour et du code d'accès.

Source actuelle : liste papier du centre, mise à jour le 09/09/2026.
Transcription à vérifier avant tout usage opérationnel.
