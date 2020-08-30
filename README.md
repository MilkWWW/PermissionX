# PermissionX
安卓运行权限API简化库

PermissionX是一个用于简化Android运行权限用法的开源库。

添加如下配置将PermissionX引入你的项目中：

```groovy

dependencies {
    ...
    implementation 'com.permission.maodev:permission:1.0.0'
}
```

然后就可以使用如下语法结构来申请运行时权限了：

```kotlin
PermissionX.request(this,
                 Manifest.permission.CALL_PHONE,
                 Manifest.permission.READ_CONTACTS) { allGranted, deniedList ->
                 if(allGranted) {
                    Toast.makeText(this,"All permissions are granted",Toast.LENGTH_SHORT).show()
                 }else{
                    Toast.makeText(this,"You denied $deniedList",Toast.LENGTH_SHORT).show()
                 }
             }
```