# API Dependency Issue

This project was creating using `flutter create` on the stable channel.

The only modification was to add `api "com.symbol:emdk:7.6.10"` to the dependencies of `android/app/build.gradle`

## Building stable APK

`flutter channel stable`

`flutter channel upgrade`

`flutter clean`

`flutter pub get`

`flutter build apk --target-platform android-arm64 --split-per-abi --no-shrink`

## Building beta APK

`flutter channel beta`

`flutter channel upgrade`

`flutter clean`

`flutter pub get`

`flutter build apk --target-platform android-arm64 --split-per-abi --no-shrink`

## Comparing

Use Analyze APK in Android studio to inspect the differences in classes.dex.

In the stable APK, com.symbol.emdk is included but is missing from the beta APK.
