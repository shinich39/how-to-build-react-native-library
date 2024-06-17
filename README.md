# how-to-build-react-native-library

Use native modules.

##

1. Create react native project.

```console
npx create-expo-app@latest
npx expo install expo-dev-client
```

2. Create react native builder bob.

```console
npx create-react-native-library@latest my-module
```

3. Add native modules.

  - android
  ```kotlin
  // build.gradle

  ...
  // Add java modules
  implementation "net.lingala.zip4j:zip4j:2.+"
  implementation "com.github.junrar:junrar:7.+"
  implementation files("libs/libp7zip-1.7.1.aar")
  ```

  - ios
  ```podspec
  # MODULE_NAME.podspec
  s.source_files = "ios/**/*.{h,m,mm,swift}"
  
  # Add ios modules
  s.dependency "SSZipArchive"
  ```

4. Packaging module

```console
npm pack
```

5. Install module

```console
npx pod-install
npx expo run:ios
npx expo run:android
```

