# Learnings on build tool maven

## Packaging Methods
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
    
    
    <build>
     <pluginManagement>
      <plugins>
       <plugin>
         <artifactId>maven-clean-plugin</artifactId>
         <version>3.1.0</version>
       </plugin>
       
       <plugin>
         <artifactId>maven-resource-plugin</artifactId> <!-- copying project resouces to build output -->
         <version>3.0.2</version>
       </plugin>
       
       <plugin>
         <artifactId>maven-compiler-plugin</artifactId>
         <version>3.8.0</version>
       </plugin>
       
       
       <plugin>  <!-- Helps to generate Jar -->
         <groupId>org.apache.maven.plugins</groupId>
         <artifactId>maven-jar-plugin</artifactId>
         <configuration>
           <archive>
             <manifest>
               <addClasspath>true</addClasspath>
               <classpathPrefix>libs/</classpathPrefix> <!-- manually add all jars to a folder named libs -->
               <mainClass>com.example.app.MainClass</mainClass>
             </manifest>
           </archive>
         </configuration>
       </plugin>
       
      </plugins>
     </pluginManagement>
     
      <plugins>
       <plugin> <!-- Plugin to create jar with all dependencies -->
         <groupId>org.apache.maven.plugins</groupId>
         <artifactId>maven-assembly-plugin</artifactId>
         <configuration>
           <descriptorRefs>
             <descriptorRef>jar-with-dependencies</descriptorRef>
           </descriptorRefs>
           <archive>
             <manifest>
               <mainClass>org.example.App</mainClass>
             </manifest>
           </archive>
         </configuration>
       </plugin>
     </plugins>
    </build
    
  </project>
  
```
## 
