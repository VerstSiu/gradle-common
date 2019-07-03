
# Jar Module Export

## Usage

1. Apply grale file to your `{module}/build.gradle`:

    ```gradle
    apply from: 'https://raw.githubusercontent.com/VerstSiu/gradle-common/master/java/jar-module-export.gradle'
    ```

2. Execute `:{module}:release` or `:{module}:releaseExport` tasks on terminal.

## Examples

* File structure:

    ```
    <root>
    /--- lib
    |    +--- build.gradle
    ```

* Results of `./gradlew :lib:release`:

    ```
    // NOTE: Old generated jar files will be removed from here
    lib/build/libs/{baseName}-{version}.jar
    lib/build/libs/{baseName}-{version}-sources.jar
    ```

* Results of `./gradlew :lib:releaseExport`:

    ```
    // NOTE: Old generated jar files will be removed from here
    export/{baseName}-{version}.jar
    export/{baseName}-{version}-sources.jar
    ```
