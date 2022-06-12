./gradlew --no-build-cache --dependency-verification lenient assemblePlayProdRelease

keytool -genkey -v -keystore my-release-key.keystore -alias mykey -keyalg RSA -keysize 2048 -validity 10000

~/Library/Android/sdk/build-tools/32.0.0/apksigner sign -ks my-release-key.keystore app/build/outputs/apk/playProd/release/file.apk
