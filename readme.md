## spring boot 打包相关示例

#### profile-package 多环境打包 
结合使用: `maven profile` + `spring boot profile`
* `maven profile` 打包时替换profile内容
* `spring boot profile` 运行时采用指定 application-xx.yml 配置文件
* 符合 spring boot plugin 标准打包，可以制作成系统服务

不太方便的地方：是一个 fat jar，文件较大时上传服务较慢。

#### thin-jar-package 打 thin 包(只包括自己编写的class),将依赖的jar 输出至 lib 目录
- [X] jar 已外置 ./lib 目录, `java -Dloader.path=lib/ -jar thin-jar-demo.jar`
- [X] 配置外置, ./config 目录，spring boot 会优先 包内的配置
- [ ] 可配置化的将输出称为 zip (app.jar/config/lib/) ，即lib可选
- [ ] 启动脚本 start.sh 

