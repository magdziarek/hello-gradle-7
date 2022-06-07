1. Execute `./gradlew :dependencies --configuration compileClasspath`
2. In `app/build.gradle(.kts)`: Add an `implementation` dependency to `com.google.inject:guice:4.2.3` 
3. Execute `:dependencies --configuration compileClasspath` again. Can you see the Guava conflict?
4. Change the Guava version in your build to `26.0-jre`. Which version is selected now?
5. Change the Guice dependency to `runtimeOnly`. Compare the `compileClasspath` and the `runtimeClasspath`. Check the selected Guava versions!
6. Enforce the selection of Guava `26.0-jre` (hint: use a strict version -> that's the !! added after version, i.e. 26.0-jre!!). Is `26.0-jre` selected in both `compileClasspath` and the `runtimeClasspath`?