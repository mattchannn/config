<div align="center">
<h1>AIA Connect App 📱</h1>
<p>React Native</p>
<hr />
</div>

## 💡 Prerequisites

This project is powered by React Native CLI.

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

**Once the server is up and running, you can then run**

```shell
yarn android-UAT
```

## 🎭 Common Gotcha

Experience any issue when installing dependencies?

1. Delete `yarn.lock` and retry
2. If you recognize the below error message, try to install dependencies with run script `yarn install --ignore-engines`

   > The engine "node" is incompatible with this module

Experience any issue when running the App (Android)?

- If you recognize the below error message, try to include the code in `build.gradle`. [Reference](https://hosochin.com/2021/07/15/post-871/)

  > Error: NoClassDefFoundError: javax/annotation/Generated

  ```java
  implementation 'javax.annotation:javax.annotation-api:1.3.1'    annotationProcessor("javax.annotation:javax.annotation-api:1.3.2")
  ```

- If you recognize the below error message, please make sure you have the right NDK version installed. [Reference](https://stackoverflow.com/questions/60404457/no-version-of-ndk-matched-the-requested-version)
  
  > No version of NDK matched the requested version _%version%_. Versions available locally: _%version%_
