# how-to-build-react-native-library
.


1. Create react native project.

```console
npx create-expo-app@latest
npx expo install expo-dev-client
```

2. Create react native builder bob.

```console
npx create-react-native-library@latest my-module
```

3. Packaging module

```console
npm pack
```

4.

```console
npx expo run:ios
npx expo run:android
```
