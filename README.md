# Moto Rush — Endless Motocross

Course offroad **infinie** en arcade, dessinée et jouable dans un seul fichier — canvas 2D, aucun serveur, aucune installation.

F.S.M Game House

## Jouer

Ouvre `index.html` dans un navigateur récent — sur iPhone, iPad ou ordinateur.

### Mettre le jeu en ligne avec GitHub Pages

1. Les fichiers sont déjà à la racine de ce dépôt.
2. **Settings → Pages** → Source : *Deploy from a branch* → branche `main` → dossier `/ (root)`.
3. Après une minute : `https://wwwh8hv4w5-lang.github.io/moto-rush/`

## Concept

La piste défile sans fin : saute les obstacles, collecte les pièces, maîtrise tes réceptions. Le monde change de région toutes les 520 m, avec palettes, reliefs et décors propres :

- **FORÊT** (*Forest Run*)
- **CANYON** (*Canyon Run*)
- **ALPINE** (*Alpine Run*)

Obstacles : rampe, rocher, tronc, pneus, souche, caisse. Rampe = vrai saut ; le reste se franchit ou se frôle (bonus de frôlement).

### Figures et score

- **Flip** en l'air (incliner la moto) : 250 pts par tour complet
- **Style propre** : 100 pts · **Réception parfaite** : 75 pts
- **Frôlement** : 25 pts
- **Pièces** : 50 pts de base, avec bonus de **combo** (jusqu'à ×8)
- **Nitro** : +125 pts et vitesse accélérée pendant 4,2 s
- **Bouclier** : absorbe un impact (+100 pts)
- Points de distance en continu ; score **doublé** pendant l'événement *FIÈVRE DU SCORE*

## Événements (11 types)

Tirés au sort toutes les ~13 à 18 s, jamais deux fois de suite, annoncés par une bannière avec minuteur :

SPRINT ZONE · PLUIE DE PIÈCES · RAFALE DE POUSSIÈRE · ZONE DE RAMPES · DÉFI STYLE · VENT TRAVERSIER · GRAVITÉ RÉDUITE · PISTE BOUEUSE · ORAGE SUR LA PISTE · FIÈVRE DU SCORE · AIMANT À PIÈCES

## Objectifs (6 types)

Un objectif à la fois, récompensé de 180 à 320 pts, puis le suivant arrive :

COLLECTEUR (pièces) · PILOTE ACROBATIQUE (figures) · ENDURANCE (distance) · PLEIN D'ÉNERGIE (nitro) · À L'ABRI (bouclier) · PISTE MAÎTRISÉE (obstacles)

## Commandes

| Action | Tactile | Clavier |
|--------|---------|---------|
| Sauter | Bouton **SAUT ↑** (ou toucher la piste) | `Espace` / `↑` / `W` |
| Incliner en arrière | Bouton **↶ ARRIÈRE** | `A` / `←` |
| Incliner en avant | Bouton **↷ AVANT** | `D` / `→` |
| Pause / reprendre | Bouton **Ⅱ PAUSE** | `Échap` / `P` |
| Recommencer | Bouton **↻** | `Entrée` (écran de fin) |

Crash si la réception est trop inclinée ou si un obstacle est touché sans bouclier. Le **record** est conservé dans le navigateur (`localStorage`).

## Sons

Moteur sonore synthétisé en **WebAudio** (moteur qui suit la vitesse, effets saut / pièce / réception / crash), désactivé par défaut, activation par le bouton **SON**.

## Technique

- Un seul fichier `index.html`, **zéro dépendance**, canvas 2D
- Résolution plafonnée à ×2 DPR (chaleur et batterie sur iPhone / iPad), physique en sous-pas (écrans 60 / 90 / 120 Hz)
- Pause automatique quand l'onglet est masqué ; gestes navigateur neutralisés sur les commandes
- Difficulté progressive : vitesse et densité d'obstacles montent avec la distance ; génération aléatoire semée

## Fichiers

| Fichier | Rôle |
|---------|------|
| `index.html` | Jeu complet (rendu, physique, événements, missions, audio) |
| `README.md` | Ce document |

## Crédits

- **Jeu** : F.S.M Game House
- **Titre** : Moto Rush — Endless Motocross
