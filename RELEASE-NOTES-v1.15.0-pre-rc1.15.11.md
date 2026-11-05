# MediaClean 1.15.0 - PRE-RC1.15.11

**Préversion Windows 64 bits - interface en français**

MediaClean aide à identifier, renommer et classer les films et séries grâce à TMDB et TVmaze. Cette version améliore surtout le traitement des vidéos dont la qualité ou les informations de classement sont incomplètes.

## Nouveautés et corrections

- **Détection de la qualité vidéo :** meilleure reconnaissance des indications `4KLight`, `BD1080p`, `HD1080P`, `HD720p` et `BD720p` présentes dans les noms. Une indication issue du nom n'est pas présentée comme une mesure technique vérifiée.
- **Contrôle ciblé avant Apply :** lorsque le classement exige la qualité vidéo et que celle-ci manque, MediaClean peut tenter de lire la résolution réelle du fichier concerné, sans analyser systématiquement toute la vidéothèque.
- **Identification TMDB plus prudente :** vérification supplémentaire des correspondances automatiques incohérentes, notamment lorsqu'un numéro significatif disparaît du titre (exemple : `Chien 51` ne doit pas devenir automatiquement `Chien-chien`).
- **Genres et années :** meilleure récupération des années présentes dans les noms de fichiers et des genres déjà identifiés par TMDB, en préservant les choix manuels.
- **Pas de qualité inventée :** les mentions génériques `WEBRip`, `HDRip` ou `DVDRip` ne suffisent pas à déduire une résolution précise.

## Fonctionnalités conservées

- **Traitement partiel :** les fichiers sûrs peuvent être traités tandis que les conflits et éléments à vérifier restent intacts.
- **Plusieurs versions d'un même film :** possibilité de conserver séparément différentes qualités ou éditions, sans écraser d'exemplaire.
- **Sécurité :** protections des destinations, journal de traitement, mémoire des identifications, sous-titres compagnons et fonction **Undo** conservés.

## Validation

- Compilation **Windows x64 / .NET 10** réussie : **0 erreur, 0 avertissement**.
- **437 auto-tests réussis, 0 échec** lors de la validation GitHub Actions.
- Archive Windows autonome disponible ci-dessous avec son fichier `.sha256`.

Les tests automatisés ne remplacent pas la vérification manuelle sur une bibliothèque réelle. Faites d'abord un essai avec des **copies** de vidéos et conservez vos sauvegardes.

## Installation et sécurité

Téléchargez `MediaClean-PRE-RC1.15.11-win-x64.zip`, **extrayez entièrement** l'archive et lancez `MediaClean.exe`. La publication Windows est autonome : aucune installation séparée du runtime .NET n'est nécessaire.

Le programme n'est pas signé numériquement ; Windows peut donc afficher un avertissement d'éditeur inconnu. Vérifiez la provenance, l'empreinte SHA-256 et, si souhaité, analysez le fichier avec votre antivirus. **Ne désactivez pas SmartScreen ni l'antivirus.**

La version **PRE-RC1.15.10** reste disponible séparément.

---

## English

**MediaClean 1.15.0 - PRE-RC1.15.11** is a Windows x64 test pre-release. The UI is currently in French.

**What's new:** improved recognition of quality tags such as `4KLight` and `BD1080p`; targeted reading of actual video resolution when required for sorting; stricter automatic TMDB title consistency checks; improved recovery of existing movie years and genres. Generic release labels such as `WEBRip` are not assumed to establish a specific resolution.

**Preserved:** safe partial processing, multiple movie versions, identification memory, companion-file handling, collision safeguards, processing logs and Undo.

**Validation:** Windows / .NET 10 build succeeded, **437 automated tests passed, 0 failed**. Manual testing with backup copies remains recommended.

**Install:** download the Windows x64 ZIP below, fully extract it, and run `MediaClean.exe`. The app is self-contained. It is not code-signed: verify the published SHA-256 hash and do not disable Windows security protections.
