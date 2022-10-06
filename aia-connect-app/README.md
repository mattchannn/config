<div align="center">
<h1>AIA Connect App 📱</h1>
<p>React Native</p>
<p>Powered by React Native CLI</p>
<hr />
</div>

## 💡 Prerequisites

- You should walk this [setup guide](https://aiahk-confluence.aiaazure.biz/display/ACTA/RN+Setup) through before looking any further

## 🎃 What you should learn from this repo

## System Requirements

Follow the instruction [here](https://reactnative.dev/docs/environment-setup) and make sure the version of Node, Android Studio, JDK and other related package are within the requirement

> For TSS team, you may refer to [this](https://www.react-native.cn/docs/environment-setup/)

- You should use `yarn` instead of `npm` to install dependencies

## 🚀 Setup

**Install dependencies**

```shell
yarn install
```

**Start Development Server**

```shell
yarn start
```

**To install android application on your device, you can run**

_Please do not do it under AIA network_

```shell
yarn android-UAT
```

## 🎭 Common Gotcha

Experience any issue when installing dependencies?

1. Delete `yarn.lock` and retry
2. If you recognize the below error message, try to install dependencies with run script `yarn install --ignore-engines`

   > The engine "node" is incompatible with this module
3. If that still does not work, please refer to this [link](https://github.com/yarnpkg/yarn/issues/5259) for voodoo.

### Run app in iOS (Xcode)

In Xcode, arm64 architecture error when building the AIAConnect-UAT app

- Solution for `error build: In <path>, building for iOS Simulator, but linking in object file built for iOS, file <path> for architecture arm64` is to open Xcode in Rosetta mode.

### Run app in Android

Experience any issue when running `yarn android-UAT`?

- If you recognize the below error message, try to include the code in `build.gradle`. [Reference](https://hosochin.com/2021/07/15/post-871/)

  > Error: NoClassDefFoundError: javax/annotation/Generated

  ```java
  implementation 'javax.annotation:javax.annotation-api:1.3.1'    annotationProcessor("javax.annotation:javax.annotation-api:1.3.2")
  ```

- If you recognize the below error message, please make sure you have the right NDK version installed. [Reference](https://stackoverflow.com/questions/60404457/no-version-of-ndk-matched-the-requested-version)

  > No version of NDK matched the requested version _%version%_. Versions available locally: _%version%_

White screen

- If you see white screen, there is a high chance your device / emulator does not connected to the React Native development server. First, make sure you have the Metro server on, then you can open React Native development menu and click "Reload", the error screen will popup if that's the case.

Cannot connect to React Native development server?
- If you cannot connect to React Native development server. That's because some applications in your device occupies `8081` port which is the default port of React Native development  server. The solution is that you should start the React Native development server with other port, for example `8000`. And once you started the application, open React Native development menu, go to "Settings", and find "Debug server host & port for device" setting, enter `ipaddress:port` like the illustration below.
