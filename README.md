#申明
从crossoverjie学习过来的项目 
作者地址: https://github.com/crossoverJie/SSM-DUBBO-HTTP

# 开发

http://crossoverjie.top/2017/05/02/SSM13/

# 预览
![dubbo-http封面.jpg](https://ooo.0o0.ooo/2017/04/30/5905dae5d9b8c.jpg)

# 简介
将dubbo服务对外暴露出`http`服务。

可供其他任何语言进行调用。


# 安装

```
git clone https://github.com/crossoverJie/SSM-DUBBO-HTTP.git
```

```
cd SSM-DUBBO-HTTP
```

```
mvn clean
```

```
mvn install
```


# 使用

```xml
<dependency>
    <groupId>com.chengjs</groupId>
    <artifactId>CJS-SSM-HTTP-PROVIDER</artifactId>
    <version>1.0.0</version>
</dependency>
```

## spring配置

```xml
    <!--dubbo服务暴露为http服务-->
    <bean class="HttpProviderConf">
        <property name="usePackage">
            <list>
            	   <!--需要暴露服务的接口包名，可多个-->
                <value>com.chengjs.api</value>
            </list>
        </property>
    </bean>
    <!--扫描暴露包-->
    <context:component-scan base-package="com.chengjs.dubbo.http"/>
```
