
### 打不同环境的包

具体原理就是根据传入的参数修改`sourceset`的设定

**01-folder**展现的是把不同环境文件按folder归类存放，打包时将src/main/resources下的文件打包,标明环境的folder目录不变，排除掉其他环境的folder,如果需要去除环境目录直接将内容打到src/main/resources下可以将目标环境目录添加到srcDirs中


执行下面的命令打相关环境的包
```bash
gradle -q -Penv=pro
```

可以修改`gradle.properties`中的`env`默认值