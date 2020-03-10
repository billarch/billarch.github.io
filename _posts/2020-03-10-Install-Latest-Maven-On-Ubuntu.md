我今天在网上看到一个安装maven的方法，觉得挺好的。考虑比较周全。在Ubuntu 18.04上测试通过。

1. Download the latest maven
2. `sudo tar xf /tmp/apache-maven-*.tar.gz -C /opt`
3. `sudo ln -s /opt/apache-maven-3.6.0 /opt/maven`
4.  `sudo nano /etc/profile.d/maven.sh`
5. maven.sh内容：
```
export JAVA_HOME=/usr/lib/jvm/default-java
export M2_HOME=/opt/maven
export MAVEN_HOME=/opt/maven
export PATH=${M2_HOME}/bin:${PATH}
```
6. `sudo chmod +x /etc/profile.d/maven.sh`
7. `source /etc/profile.d/maven.sh`