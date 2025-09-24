# TD1 — Optimisation algébrique

## Objectifs du TD
Ce TD a pour but de te familiariser avec l'algèbre relationnelle et son lien avec SQL.  
À l'issue de ce TD, tu devras être capable de :  
- Représenter un schéma relationnel sous forme Entité/Association (diagramme E/A).  
- Traduire des requêtes SQL en expressions algébriques (linéaires et arborescentes).  
- Identifier et corriger des expressions algébriques incorrectes.  
- Optimiser des expressions pour réduire le volume de données manipulé.  
- Proposer une version SQL efficace correspondant à l'expression optimisée.

---

## Schéma relationnel utilisé
Tous les attributs sont de type chaîne de caractères, sauf mention contraire (entier).

- **ETUDIANT**(**Et_Id**, Et_Nom, Et_Pren, Et_DateNais, Et_LieuNais)  
- **ENSEIGNANT**(**En_Id**, En_Nom, En_Pren, En_DateNais, En_LieuNais)  
- **UE**(**UE_Id**, UE_Libelle, UE_CM, UE_TD, UE_NbGrp, _En_Id_)  
- **ENS_TD**(_UE_Id_, _En_Id_, **ETD_Grp**)  
- **INSCRIPTION**(_Et_Id_, _UE_Id_, I_Grp, I_NoteF)  

> Remarques :  
> - UE = Unité d’Enseignement  
> - Clés primaires en gras, clés étrangères soulignées  
> - Attributs entiers : UE_CM, UE_TD, UE_NbGrp, ETD_Grp, I_Grp

---

## Symboles d’algèbre relationnelle utilisés
- **π** : projection (sélection de colonnes)  
- **σ** : sélection (filtrage de lignes)  
- **⋈** : jointure  
- **×** : produit cartésien  
- **∪** : union  
- **−** : différence  
- **ρ** : renommage  
- **∩** : intersection  
- **÷** : division (pour les “pour tous”)

---


