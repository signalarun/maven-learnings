# maven-learnings
Learnings on build tool maven

# Packaging Methods
```
  <project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/maven-v4_0_0.xsd">
    <modelVersion>4.0.0</modelVersion>
    <groupId>com.example.app</groupId>
    <artifactId>MyApp</artifactId>
    <version>1.0-SNAPSHOT</version>
    
    <name>MyApp</name> <!-- Name of the app -->
    <description>This is a sample to project to demo POM</description>
    <url>www.app.example.com</url>
    
    <properties>
        <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
        <maven.compiler.source>11</maven.compiler.source>
        <maven.compiler.target>11</maven.compiler.target>    <!-- Java compiler -->
    </properties>
    
    <packaging>jar</packaging> <!-- This indicates the packaging -->
  </project>
  
```
## 
