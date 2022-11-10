# Junit 5 (Junit-jupiter)

You will need the [**junit-jupiter-api**](https://mvnrepository.com/artifact/org.junit.jupiter/junit-jupiter-api) and
[**junit-jupiter**](https://mvnrepository.com/artifact/org.junit.jupiter/junit-jupiter). 
PS: Without the *junit-jupiter*, the Test classes won't run if you run ```mvn test```.

```xml 
      <!-- Test dependencies -->
        <dependency>
            <groupId>org.junit.jupiter</groupId>
            <artifactId>junit-jupiter-api</artifactId>
            <version>${junit.jupiter.api.version}</version>
            <scope>test</scope>
        </dependency>

        <dependency>
            <groupId>org.junit.jupiter</groupId>
            <artifactId>junit-jupiter</artifactId>
            <version>${junit.jupiter.version}</version>
            <scope>test</scope>
        </dependency>
        <!-- End of test dependencies -->
```

In the plugins area, you will need to have the 
[**maven-surefire-plugin**](https://mvnrepository.com/artifact/org.apache.maven.plugins/maven-surefire-plugin) and the
[**maven-failsafe-plugin**](https://mvnrepository.com/artifact/org.apache.maven.plugins/maven-failsafe-plugin).

```xml 
            <plugin>
                <artifactId>maven-surefire-plugin</artifactId>
                <version>${mvn.surefire.plugin.version}</version>
            </plugin>
            <plugin>
                <artifactId>maven-failsafe-plugin</artifactId>
                <version>${mvn.failsafe.plugin.version}</version>
            </plugin>
```

In the user defined properties area, add this.
```xml
        <!-- Test Attributes -->
        <junit.jupiter.version>5.9.1</junit.jupiter.version>
        <junit.jupiter.api.version>5.9.1</junit.jupiter.api.version>
        <mvn.surefire.plugin.version>2.22.2</mvn.surefire.plugin.version>
        <mvn.failsafe.plugin.version>2.22.2</mvn.failsafe.plugin.version>
        <!-- End of test attributes -->
```
PS: Don't forget to check the links below for the most up-to-date versions).

### Plugins Maven Repository Links:
* [**junit-jupiter-api**](https://mvnrepository.com/artifact/org.junit.jupiter/junit-jupiter-api)
* [**junit-jupiter**](https://mvnrepository.com/artifact/org.junit.jupiter/junit-jupiter)
* [**maven-surefire-plugin**](https://mvnrepository.com/artifact/org.apache.maven.plugins/maven-surefire-plugin)
* [**maven-failsafe-plugin**](https://mvnrepository.com/artifact/org.apache.maven.plugins/maven-failsafe-plugin)
