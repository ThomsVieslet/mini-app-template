# MiniApp Template 📱

Modèle de départ pour créer des **mini-apps Android de calcul** sans backend :
une page HTML unique affichée dans une WebView, compilée en APK par GitHub Actions, partagée directement — sans Play Store.

## Créer une nouvelle app à partir de ce template

1. Créer un nouveau dépôt vide sur GitHub (ne pas « Use this template » en public si l'app est privée : dupliquer la structure suffit).
2. Copier tous les fichiers de ce template dans le nouveau dépôt.
3. Remplacer `app/src/main/assets/index.html` par votre interface (une seule page, autonome, sans dépendance externe).
4. Adapter `android:label="MiniApp"` dans `app/src/main/AndroidManifest.xml` au nom de l'app.
5. Adapter `applicationId` dans `app/build.gradle.kts` si souhaité.

## Obtenir l'APK (sans rien installer)

1. Onglet **Actions** du dépôt → dernier run **Build APK**.
2. Télécharger l'artefact **MiniApp-APK** : il contient `app-debug.apk`.

## Installer sur un téléphone

1. Envoyer l'APK par mail/WhatsApp/Drive.
2. L'ouvrir sur le téléphone ; autoriser « sources inconnues » (une seule fois).
3. L'app apparaît sur l'écran d'accueil avec son icône.

## Modifier l'app

Éditer `index.html`, enregistrer : GitHub Actions recompile automatiquement (~5 min). Retélécharger l'artefact et remplacer l'APK sur les téléphones (mise à jour, pas de désinstallation).

## Structure

- `app/src/main/assets/index.html` — **toute l'app** (interface + calculs)
- `app/src/main/java/be/miniapp/template/MainActivity.kt` — WebView plein écran
- `app/src/main/AndroidManifest.xml` — nom, icône, aucune permission
- `.github/workflows/build-apk.yml` — build APK automatique (licences SDK acceptées non interactivement)
