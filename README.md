# mybatis-plus-generator
## 增加注解
生成好的Mapper 需要增加 @Mapper 注解;
```$xslt
#mysql
spring.datasource.url=jdbc:mysql://192.168.10.223:3306/wordpress?useUnicode=true&characterEncoding=utf8
spring.datasource.username=ghost
spring.datasource.password=ghost1234
spring.datasource.driver-class-name=com.mysql.jdbc.Driver
#mybatis-plus
mybatis-plus.mapper-locations=classpath:mapper/*.xml
mybatis-plus.type-aliases-package=com.ycfd.userrole.entity
mybatis-plus.global-config.id-type=0
mybatis-plus.global-config.field-strategy: 1
mybatis-plus.global-config.configuration.map-underscore-to-camel-case=true
mybatis-plus.global-config.configuration.cache-enabled=false
mybatis-plus.global-config.configuration.jdbc-type-for-null='null'
# 配置slq打印日志
mybatis-plus.configuration.log-impl=org.apache.ibatis.logging.stdout.StdOutImpl
```

## 重复执行
当文件已经存在的时候不会自动覆盖的;

## ORACLE
oracle连接jar在中央仓库没用，需要自己下载后手动安装到本地仓库，语法：
```$xslt
mvn install:install-file -DgroupId=com.oracle -DartifactId=ojdbc6 -Dversion=11.1.0.7.0 -Dpackaging=jar -Dfile=ojdbc6.11.1.0.7.0.jar
```