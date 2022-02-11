```
cd pre-compiled-scripts
./gradlew build publishToMavenLocal
cd -
cd main-project
./gradlew build
```
Build is successful

Edit `main-project/settings.gradle` and uncomment `includeBuild` directive.

```
$ ./gradlew build

FAILURE: Build failed with an exception.

* Where:
Build file 'sub-project\sub-project-api\build.gradle' line: 2

* What went wrong:
Plugin [id: 'com.mycompany.example.java'] was not found in any of the following sources:

- Gradle Core Plugins (plugin is not in 'org.gradle' namespace)
- Included Builds (None of the included builds contain this plugin)
- Plugin Repositories (plugin dependency must include a version number for this source)

* Try:
> Run with --stacktrace option to get the stack trace.
> Run with --info or --debug option to get more log output.
> Run with --scan to get full insights.

* Get more help at https://help.gradle.org

BUILD FAILED in 1s

```



