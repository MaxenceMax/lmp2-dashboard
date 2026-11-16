# lmp2-dashboard — contexte pour Claude

Tableau de bord SimHub « dash-max-lmp2 » pour Le Mans Ultimate (LMP2). Répondre en français.

## Où il s'affiche

Sur l'iPhone 17 du pilote, en paysage, pendant qu'il conduit. Son écran (≈ 2,17:1) est bien plus
large que le canevas d'origine (1200×720, soit 1,67:1) : toute retouche de mise en page tient compte
de ce format et des zones mortes (Dynamic Island, barre d'accueil).

## Ce que le pilote attend

- **La lisibilité d'abord**, l'esthétique ensuite : l'information doit se trouver d'un coup d'œil.
- **Une hiérarchie nette** : rapport engagé et vitesse très gros et proches l'un de l'autre,
  réglages en petit. Refusés : étiquettes grises, caractères fins, textes tous de la même taille.
- Disposition inspirée du tableau de bord de la McLaren 720S GT3 : rapport orange au centre, vitesse
  dessous, réglages en bandeau en haut, plusieurs pages. Police Oxanium.

## Comment travailler

1. Proposer une maquette avant de toucher aux fichiers : `mock-dashboard.html`, un aperçu HTML animé
   généré depuis une copie de travail des `.djson`.
2. Attendre l'accord du pilote.
3. Appliquer au dossier `dash-max-lmp2/`, puis reconstruire `dash-max-lmp2.simhubdash` : c'est une
   archive zip du dossier `dash-max-lmp2/`.

SimHub est un logiciel Windows. Sur le Mac, rien ne s'y teste : les `.djson` se modifient par script
et se contrôlent sur l'aperçu, puis le pilote importe le `.simhubdash` sur son PC. Dire clairement
ce qui n'a pas été vu dans SimHub.

## Git

- Dépôt public. Gitflow : toute branche part de `develop` et y revient par une PR ; `develop` ouvre
  la PR vers `main`. Titres et descriptions de PR courts, sans mention d'outil de génération.
- E-mail de commit à régler localement sur l'adresse noreply du compte :
  `git config user.email "3344026+MaxenceMax@users.noreply.github.com"`.
- L'archive d'origine du tableau de bord, faite par un tiers, et les anciennes sauvegardes sont
  ignorées : ne pas les publier.

L'ingénieur de course vocal est dans un autre dépôt, `MaxenceMax/e-race`.
