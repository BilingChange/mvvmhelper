###项目初始化模板
:chicken::chicken::chicken: 这是一个快速开发的框架，使用Kotlin语言开发，MVVM+Jetpack架构，封装了公共头部、界面状态管理、ViewModel、LiveData、DataBinding、头部刷新、加载更多、沉浸式、全局通知、丰富好用的拓展函数、RxHttp网络请求等等一系列工具**
## 1.如何集成

- **1.1 在root's build.gradle中加入Jitpack仓库**

```gradle
buildscript {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}
allprojects {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}
```

- **1.2 在app's build.gradle中添加依赖**

```gradle
apply plugin: 'kotlin-kapt'

...

dependencies {
  ...
  implementation 'com.github.hegaojian:MvvmHelper:1.0.6'
  kapt "com.ljx.rxhttp:rxhttp-compiler:2.5.5"
}
```

- **1.3 在app's build.gradle中，android 模块下开启DataBinding(如果你不想用DataBinding,请忽略这一步)**

``` gradle
AndroidStudio 4.0 以下版本------>
android {
    ...
    dataBinding {
        enabled = true 
    }
}

AndroidStudio 4.0及以上版本 ------>
android {
    ...
   buildFeatures {
        dataBinding = true
    }
}
 
```

