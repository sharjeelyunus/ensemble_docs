# Deploy to Android Play Store

* Make sure you completed the [Preparing your App](/deploy/1-prepare-app.md) step, then navigate to the folder created (e.g. my_first_app).
* Open the file `pubspec.yaml` and look for `version` e.g. version: 1.0.0+1. The last number is the build number which has to be unique on every upload. Simply increment it for each production build.
* Run `flutter create --platforms=android .` (note the period at the end).
* Run `flutter build appbundle --no-tree-shake-icons`. This will create the bundle file under `build/app/outputs/bundle/release/app-release.aab`.
* Log into your [Play Store console](https://play.google.com/console) and go to your App. Select your release and upload the `.aab` file.

## Updating your Play Store app.
* Once your app has been approved and live on the Play Store, follow these instructions for subsequent updates:
  * Run `flutter pub upgrade` to upgrade Ensemble dependencies. This may include framework's bug fixes as well as new widget additions.
  * If you are using Ensemble-hosted definitions, you already have the latest page definitions.
* Increment the version (the one after the + sign) in `pubspec.yaml`.
* Run `flutter build appbundle --no-tree-shake-icons`. This will create the bundle file under `build/app/outputs/bundle/release/app-release.aab`.
* Log into your [Play Store console](https://play.google.com/console) and go to your App. Select your release and upload the `.aab` file.
