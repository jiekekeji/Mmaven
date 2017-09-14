Maven--集成Tomcat7插件
===

Maven Tomcat插件现在主要有两个版本，tomcat-maven-plugin和tomcat7-maven-plugin。

一、插件tomcat7-maven-plugin步骤:
---

1、在pom.xml中添加如下配置：
```
<build>
	<finalName>demo002</finalName>
	<pluginManagement>
		<plugins>
			<plugin>
				<groupId>org.apache.tomcat.maven</groupId>
				<artifactId>tomcat7-maven-plugin</artifactId>
				<version>2.2</version>
				<configuration>
					<!-- 应用名称 -->
					<path>/msp</path>
					<!-- 端口号 -->
					<port>8099</port>
					<!-- URL按UTF-8进行编码，这样就解决了中文参数乱码。 -->
					<uriEncoding>UTF-8</uriEncoding>
				</configuration>
			</plugin>
		</plugins>
	</pluginManagement>
</build>
```

2、启动Tomcat7插件步骤：右键项目-Run As-Run Configurations-右键Maven build-New-按下图方式操作:

![image](https://github.com/jiekekeji/Mmaven/blob/master/demo002/preview/demo002-1.png)

![image](https://github.com/jiekekeji/Mmaven/blob/master/demo002/preview/demo002-2.png)

**注意Goals填写的是 tomat7:run,不是tomcat:run ,因为这里使用的是tomcat7-maven-plugin。**