# gradle-types

Builds groovy source with different groovy versions and publishes each build as a separate jar:

 - gradle-types-1.0.pom
 - gradle-types-1.0.jar // default. groovy 2.4
 - gradle-types-1.0-groovy2_0.jar
 - gradle-types-1.0-groovy2_3.jar

The default is built with groovy 2.4 and is available as:
```gradle
  repositories {
    maven { url "https://jitpack.io" }
  }
```
```gradle
  compile 'com.github.jitpack-io:gradle-types:1.0'
```

Older versions:
 - groovy2_0
 - groovy2_3

are available using classifiers and packaging type @jar:
```gradle
  compile 'com.github.jitpack-io:gradle-types:1.0:groovy2_0@jar'
  compile 'org.codehaus.groovy:groovy-all:2.0.5'
```

Specifiying packaging type won't resolve transitive dependencies so those have to be added separately.

