# Build openfire plugin example by gradle @ Android Studio & IntelliJ IDEA 

[![N|Solid](https://blog.desdelinux.net/wp-content/uploads/2013/02/XMPP_logo.png)](https://en.wikipedia.org/wiki/XMPP)

[![N|Solid](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRklICFoRqqDLY5qFuJYVpcIxxxAeGzBxAAgK0Sd8ltIgAMUKTs)](https://www.igniterealtime.org/projects/openfire/)

This project is fork form  [openfire-plugin-example]  
Openfire is a real time collaboration (RTC) server.

# Android Studio !

  - Need Import [Ant plugin]  

# How to import ?

you can follow the Ref and then step by step :
* [将4.2.4版本的openfire源码导入到IDEA中]  !

# How to Building ?

Building the [Openfire plugin](http://download.igniterealtime.org/openfire/docs/latest/documentation/plugin-dev-guide.html) with Gradle.

Project Structure:

```
openfire-plugin-example/
|-- openfire/
|-- src/
    |-- main/
        |-- java/**/*.java
        |-- resources/
        |-- database/
        |-- i18n/
        |-- web/
        |-- plugin.xml
        |-- readme.html
        |-- changelog.html
        |-- logo_small.gif
        |-- logo_large.gif
```

Checkout this project:

```sh
$ git clone https://github.com/shrhdk/openfire-plugin-example
```

Download and extract [Openfire](https://www.igniterealtime.org/downloads).

```
openfire-plugin-example/
|-- openfire/  <- extracted
    |-- README.html
    |-- ...
```

Build and deploy this project:

```sh
$ ./gradlew deployPlugin
```

As a result `example.jar` will be built:

```
openfire-plugin-example/
|-- build/
    |-- distributions/
        |-- example.jar  <- built
```

And `example.jar` will be copied to `plugins` directory:

```
openfire-plugin-example/
|-- openfire/
    |-- plugins/
        |-- example.jar  <- copied
```

Launch Openfire:

```sh
$ openfire/bin/openfire run
Openfire 4.0.3 [Nov 12, 2016 4:44:25 PM]
Admin console listening at:
  http://localhost:9090
  https://localhost:9091
ExampleComponent initialzie, JID: example.localhost
<iq type="get" id="456-1" from="component.localhost" to="example.localhost">
  <query xmlns="http://jabber.org/protocol/disco#info"/>
</iq>
```


(** Set up the openfire from admin console (http://localhost:9090) at the firsttime. **)

# Ref

[Java Build Tools: Ant vs Maven vs Gradle](https://technologyconversations.com/2014/06/18/build-tools/).

[Using Ant from Gradle](https://docs.gradle.org/current/userguide/ant.html?_ga=2.49925295.808292931.1537139109-1327524230.1534698594#sec:import_ant_build).

[Converter for pom.xml into build.gradle](https://discuss.gradle.org/t/converter-for-pom-xml-into-build-gradle/557).

[Quickly create Jar artifact for application](https://blog.jetbrains.com/idea/2010/08/quickly-create-jar-artifact/).

[How do I build an OpenFire plugin using Gradle in Intellij?](https://stackoverflow.com/questions/27671434/how-do-i-build-an-openfire-plugin-using-gradle-in-intellij).



   [Ant plugin]: <https://github.com/CMingTseng/AndroidStudio_To_JetBrains>
   [将4.2.4版本的openfire源码导入到IDEA中]: <https://www.jianshu.com/p/ceccc32af028>
   [openfire-plugin-example]: <https://github.com/shrhdk/openfire-plugin-example>
