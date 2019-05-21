# maven-snapshots
介绍如何通过 android studio 配置公司 snapshots 远程仓库地址

## 工程根配置 

- 工程根目录`build.gradle`配置    
```gradle
 allprojects {
     repositories {
         jcenter()
         mavenCentral()
         maven {
             url "https://raw.githubusercontent.com/aorise-org/maven-snapshots/master"
         }
     }
 }
```

## Android 公共库

### 介绍
- 统一的联网请求接口
- 统一的图片请求接口
- 统一的数据库操作接口
- 统一BaseActiviy、BaseFragment等UI处理
- 统一列表下拉刷新、上拉加载更多的处理
- 统一的登录组件


- 项目根目录`build.gradle`配置（替换最新版本号）    
```gradle
dependencies {
    compile 'cn.aorise:android-common:1.3.3-SNAPSHOT'
}
```

## Android 视频库

### 介绍
- 基于 webrtc 的视频通讯库
- 统一的视频请求页面
- 统一的视频接听页面

详细介绍请看接口文档


- 项目根目录`build.gradle`配置（替换最新版本号）    
```gradle
dependencies {
    compile 'cn.aorise:android-webrtc:1.2.9-SNAPSHOT'
}
```
