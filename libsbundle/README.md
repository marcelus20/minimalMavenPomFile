# Bundling your libs jars. 

### You will need the [**maven-shade-plugin**](https://mvnrepository.com/artifact/org.apache.maven.plugins/maven-shade-plugin)
```xml
<plugins>
    <plugin>
        <!-- Maven plugin to bundle all your jar libs together-->
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-shade-plugin</artifactId>
        <version>3.2.4</version>
        <configuration>
            <!-- put your configurations here -->
        </configuration>
        <executions>
            <execution>
                <phase>package</phase>
                <goals>
                    <goal>shade</goal>
                </goals>
            </execution>
        </executions>
    </plugin>
<plugins>
```

### If you want to build a jar file to run a Main class with a main method and you app uses external libs, you will need to also use the [**maven-jar-plugin**](https://mvnrepository.com/artifact/org.apache.maven.plugins/maven-jar-plugin)
```xml
<plugins>
    <plugin>
        <!--        Maven plugin to bundle all your jar libs together-->
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-shade-plugin</artifactId>
        <version>3.2.4</version>
        <configuration>
            <!-- put your configurations here -->
        </configuration>
        <executions>
            <execution>
                <phase>package</phase>
                <goals>
                    <goal>shade</goal>
                </goals>
            </execution>
        </executions>
    </plugin>

    <plugin>
        <!-- Build an executable JAR -->
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-jar-plugin</artifactId>
        <version>3.3.0</version>
        <configuration>
            <archive>
                <manifest>
                    <addClasspath>true</addClasspath>
                    <classpathPrefix>lib</classpathPrefix>
                    <mainClass>com.mycompany.app.App</mainClass>
                </manifest>
            </archive>
        </configuration>
    </plugin>
</plugins>
```

###
Plugins Maven Repository Links:
* [**maven-shade-plugin**](https://mvnrepository.com/artifact/org.apache.maven.plugins/maven-shade-plugin)
* [**maven-jar-plugin**](https://mvnrepository.com/artifact/org.apache.maven.plugins/maven-jar-plugin)

