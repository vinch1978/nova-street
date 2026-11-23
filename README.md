# NOVA STREET — Prototype e-commerce streetwear

**NOVA STREET** est un prototype interactif de boutique de mode urbaine, conçu dans le cadre du **Workshop 4 — UI/UX, GDU Campus**.

Le projet présente un parcours d'achat fictif, depuis la découverte d'une collection jusqu'à la confirmation simulée d'une commande. L'objectif est de proposer une expérience claire, cohérente et adaptée aux écrans mobiles, tablettes et ordinateurs.

### 🌐 Découvrir le prototype

**[Voir NOVA STREET en ligne](https://nova-street1.netlify.app/)**

> **Projet pédagogique :** aucune commande ni aucun paiement réel ne sont effectués. Utilisez uniquement des informations fictives dans le formulaire.

## Fonctionnalités

- **Accueil :** présentation de l'univers NOVA STREET et accès à la collection.
- **Catalogue :** consultation de huit produits, avec recherche et filtres.
- **Fiches produit :** visuels, déclinaisons, tailles, quantités, informations et gestion des indisponibilités.
- **Panier :** ajout et suppression d'articles, modification des quantités et recalcul des montants.
- **Livraison :** frais de 6,99 € pour un panier inférieur à 80 €, puis livraison offerte à partir de 80 €.
- **Validation simulée :** formulaire contrôlant notamment le format de l'e-mail et du code postal, puis confirmation fictive.
- **Confort de navigation :** retour au panier avec conservation temporaire des informations déjà saisies.
- **Responsive :** interfaces adaptées aux formats mobile, tablette et ordinateur, avec un mini-panier latéral sur desktop.

## Démarche UX/UI

La conception est partie d'une approche **mobile-first**, avec une maquette de référence à **375 px** de largeur.

L'identité visuelle, appelée **« Béton signal »**, associe un fond clair (`#ECEAE4`), des textes anthracite (`#1E1E1E`), un vert canard (`#00695C`) et des accents orange (`#FF5B00`). Elle s'appuie sur les typographies **Oswald** et **Work Sans**.

Les principaux choix UX/UI sont :

- Une hiérarchie visuelle nette et un appel à l'action principal facilement identifiable.
- Des composants cohérents d'un écran à l'autre.
- Des éléments interactifs lisibles et utilisables sur mobile.
- Des retours explicites lors de la sélection d'une taille, de l'ajout au panier ou d'une erreur de formulaire.
- Un parcours de commande simple, sans transaction réelle.

## Utilisation de l'IA et itérations

Le prototype a été créé avec **Claude Design**, à partir d'un cadrage fonctionnel, de parcours utilisateurs et d'une direction artistique définis en amont.

Le travail ne s'est pas limité à une génération initiale : les écrans ont été **analysés, testés et corrigés progressivement**. Parmi les améliorations réalisées :

- Réorganisation de la fiche **HOODIE AXE** pour rendre le nom, le prix et les options plus lisibles.
- Déplacement des indicateurs du carrousel et suppression d'informations répétées.
- Amélioration des messages d'erreur et des réactions aux tailles indisponibles.
- Harmonisation des liens entre catalogue, fiches, panier et validation.
- Adaptation du prototype au desktop en préservant les interactions mobiles.

Cette démarche répond à la **séquence 5 du workshop** : audit assisté par IA, corrections prioritaires, vérification mobile et justification des choix UX/UI.

## Tests réalisés

Le prototype a été testé manuellement, y compris depuis une **fenêtre de navigation privée** :

- Accès au site public.
- Navigation entre les différentes pages.
- Ajout et suppression d'articles.
- Exactitude des totaux et des frais de livraison.
- Simulation de validation de commande.
- Contrôle des champs e-mail et code postal.
- Conservation temporaire des informations lors du retour au panier.
- Navigation au clavier.

Ces vérifications fonctionnelles ne constituent pas un audit d'accessibilité complet.

## Technologies et structure

Le site repose sur un **export statique HTML, CSS et JavaScript** généré avec Claude Design. Il ne nécessite ni serveur applicatif ni base de données pour la démonstration.

```text
nova-street/
├── index.html                         # Point d'entrée du site
├── Accueil - Mobile.dc.html
├── Catalogue - Mobile.dc.html
├── Fiche produit - *.dc.html          # Huit fiches produit
├── Panier - Mobile.dc.html
├── Validation de commande - Mobile.dc.html
└── support.js                         # Runtime associé à l'export
```

Les données du panier et le brouillon du formulaire utilisent le **stockage de session du navigateur** (`sessionStorage`).

## Installation et publication

Pour consulter le projet localement :

1. Cloner le dépôt ou télécharger ses fichiers.
2. Conserver tous les fichiers HTML et `support.js` dans le même dossier.
3. Ouvrir `index.html` avec un serveur web local (par exemple, **Live Server** dans VS Code).

Le dépôt GitHub est connecté à **Netlify** pour publier la branche `main`.

## Limites du prototype

- Aucune authentification, base de données de commandes ou intégration de paiement réel.
- Aucune commande transmise à un commerçant.
- Le brouillon du formulaire peut rester conservé pendant la session après un retour au catalogue : comportement à améliorer.
- Les tests au clavier ne remplacent pas un audit d'accessibilité exhaustif.

---

**Projet réalisé dans le cadre de la formation Product Builder No Code & IA — GDU Campus.**  
**GitHub :** [@vinch1978](https://github.com/vinch1978) · **Démo :** [nova-street1.netlify.app](https://nova-street1.netlify.app/)
