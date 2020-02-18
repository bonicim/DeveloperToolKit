#### How to Get a Java Project started quickly in Intellij

* Environment 
  - Java13
  - JUnit5
  - Hamcrest
  - [Gradle project](https://www.jetbrains.com/help/idea/work-with-gradle-projects.html)

* Update to JUnit 5.5.2
  - Go to Project Structure 
  - Under Project Settings > Libraries, add the JUnit5 library by searching for `org.junit.jupiter` Choose the latest version, which is 5.5.2 as of 24 Oct 2019
  - Then go to Test module, and add the new Junit5 to Dependencies 
  - Then update `build.gradle` with JUnit5. For more info, see [Maven Repository for JUnit5](https://mvnrepository.com/artifact/org.junit.jupiter/junit-jupiter/5.5.2). Replace the old `testCompile` section with the following : ```testImplementation group: 'org.junit.jupiter', name: 'junit-jupiter', version: '5.5.2'```
  - Also within `build.gradle` add the following code block:

```
test {
    useJUnitPlatform()
    testLogging {
        events "passed", "skipped", "failed"
    }
}
```
  - Build the project
  - Create a stairstep test using JUnit5 to ensure the project can run a simple test
