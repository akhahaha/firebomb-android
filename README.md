# firebomb-java
_Firebase object mapper_

Firebomb makes it easier to persist relational data in a NoSQL document database such as
[Firebase][1].

For more documentation about Firebomb, see [Firebomb-java][2].

## Getting Started
### Add Firebomb to your project
#### Gradle
    repositories {
        jcenter()
    }

    dependencies {
        compile 'firebomb:core:0.2.0'
        compile 'firebomb:firebase-android:0.2.0'
    }

#### Maven
    <dependency>
      <groupId>firebomb</groupId>
      <artifactId>core</artifactId>
      <version>0.2.0</version>
      <type>pom</type>
    </dependency>

    <dependency>
      <groupId>firebomb</groupId>
      <artifactId>firebase-android</artifactId>
      <version>0.2.0</version>
      <type>pom</type>
    </dependency>

#### Initialize Firebomb
[Initialize Firebase][3] and then initialize Firebomb with a new [FirebaseManager][3].

```java
Firebomb.initialize(new FirebaseServerConnection(FirebaseDatabase.getInstance()));
Firebomb.getInstance().setRootPath("v1"); // Optional root path
```

## License
Firebomb-java is distributed under the [Apache License 2.0][99].

[1]: https://firebase.google.com/
[2]: https://github.com/akhahaha/firebomb-java
[2]: https://firebase.google.com/docs/database/android/start
[3]: firebase-android/src/main/java/firebomb/database/FirebaseManager.java
[99]: LICENSE.txt
