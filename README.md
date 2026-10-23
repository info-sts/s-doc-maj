# S-DOC — mises à jour Android

Ce dépôt contient uniquement les fichiers publics de mise à jour de l’application S-DOC : aucun code source ni secret ne doit y être ajouté.

## Fichiers attendus par l’application

- `S-DOC.apk` : dernière version test, signée avec la même clé Android que les versions précédentes ;
- `update.json` : manifeste lu par l’application au démarrage.

L’application accepte exclusivement l’URL exacte de `S-DOC.apk` indiquée dans sa configuration. Le fichier `update.json` doit conserver les propriétés suivantes :

```json
{
  "version": "2.0.8",
  "versionCode": 20008,
  "apkUrl": "https://raw.githubusercontent.com/info-sts/s-doc-maj/main/S-DOC.apk",
  "notes": "Description courte"
}
```

Pour publier une nouvelle version, remplacer les deux fichiers dans le même commit, augmenter `versionCode`, puis pousser sur `main`. Les téléphones proposent la mise à jour lorsque le code de version publié est supérieur à celui installé.