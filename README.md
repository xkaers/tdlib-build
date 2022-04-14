# tdlib-build
使用Github Actions编译TDLib库. 支持Java/C#及使用TDLib库json接口的全部开发语言, 当前仅支持windows及linux系统下的TDLib库编译.

### Release说明

release中只提供Windows和linux系统下的TDLib库, 其中

1. 带有java的表示该压缩包是提供给使用jni调用TDLib库的Java开发者使用的
2. 带有csharp的是提供给使用C++/CLI调用TDLib库(windows下开发,不含uwp)的开发者使用的
3. 带有through-json-interface的是提供给使用json接口调用TDLib库的开发者使用的

只有Java和C#是需要下载上面符合**`1,2`**说明的库, 其他语言根据系统直接下载带有through-json-interface的库即可.  .net core开发者请使用带有through-json-interface的库



### 常见问题

Ubuntu下运行示例程序如果报`java.lang.UnsatisfiedLinkError: /home/**/tdlib/bin/libtdjni.so: libc++.so.1: cannot open shared object file: No such file or directory` 请先安装libc++-dev

`sudo apt-get install libc++-dev`



### 参考资料

https://github.com/tdlib/td

https://tdlib.github.io/td/build.html

https://www.arloor.com/posts/tdlib-java-telegram-client/



*workflows目前是手动触发启动的,如果你用的时候发现release不是最新的请提PR给我*



