# MediaClean 1.15.0 - PRE-RC1.15.11

> Préversion Windows x64 - préparation de la Release. **Ne pas publier avant compilation et validation des auto-tests Windows.**

## Nouveautés

- Lecture technique ciblée de la résolution manquante avant Apply, uniquement lorsqu'un rangement par qualité la nécessite.
- Meilleure reconnaissance des indications de qualité dans les noms : `4KLight`, `HD1080P`, `BD1080p`, `HD720p`, `BD720p`.
- Les mots `WEBRip`, `HDRip`, `DVDRip` ne sont pas interprétés à eux seuls comme une résolution.
- Contrôle plus prudent des identifications TMDB automatiques incohérentes avec le titre original.
- Récupération des années déjà présentes dans les noms et des genres réellement connus dans TMDB, sans écraser les choix manuels.

## Comportement préservé

- Gestion des variantes de qualité de PRE-RC1.15.10.
- Traitement partiel des fichiers sans conflit.
- Moteurs d'identification TMDB et TVmaze, mémoire d'identification, protections contre les écrasements, journal Apply et Undo inchangés.

## Validation requise

1. Compiler avec .NET 10 sous Windows.
2. Exécuter `test-mediaclean.bat` et vérifier le rapport d'auto-tests.
3. Générer `MediaClean-PRE-RC1.15.11-win-x64.zip` à partir de `publish-win-x64.bat`.
4. Vérifier le SHA-256 et tester l'archive distribuée avant publication.
5. Vérifier Apply et Undo sur une bibliothèque de copies de test.

Cette Release reste **en brouillon** tant que le binaire et les validations ne sont pas disponibles.
