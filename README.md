# dynamicws
Dynamic web services, Making development of REST is fun and easy for production for Enterprise system
## Runtime change the request/response of webservice with new code

##Building from source
The `dynamicws` is dynamic jar projects uses a [Gradle](http://gradle.org)-based build system. In the instructions
below, [`./gradlew`](http://vimeo.com/34436402) is invoked from the root of the source tree and serves as
a cross-platform, self-contained bootstrap mechanism for the build. The only
prerequisites are [Git](https://help.github.com/articles/set-up-git) and JDK 1.8.

### check out sources
`git clone git@github.com:nileshdarade/dynamicws.git`

`cd dynamicws`

### compile and test, build all jars
`gradle library`

### run jar

`cd build/libs`

`java -jar dynamicws.jar&`

### Go to home directory

`cd ../../../`

### compile and test, build all jars
`gradle jar`

copy jar from `build/libs` to directory `dynamicws/build/libs` directory

Now you can execute

###Following two api's 
1.[http://localhost:4567/library](http://localhost:4567/library)

2.[http://localhost:4567/library?jarName=book1.1.jar&className=com.nilesh.dynamicws.BookImpl_1_1](http://localhost:4567/library?jarName=book1.1.jar&className=com.nilesh.dynamicws.BookImpl_1_1)

For new code create new jar and add follow same proccess, I create book1.1.jar, book1.2.jar and book1.3.jar fore reference

3.[http://localhost:4567/library?jarName=book1.2.jar&className=com.nilesh.dynamicws.BookImpl_1_2](http://localhost:4567/library?jarName=book1.2.jar&className=com.nilesh.dynamicws.BookImpl_1_2)
4.[http://localhost:4567/library?jarName=book1.3.jar&className=com.nilesh.dynamicws.BookImpl_1_3](http://localhost:4567/library?jarName=book1.3.jar&className=com.nilesh.dynamicws.BookImpl_1_3)

 Process to create new jar cd to book1.1 project
 change the name of the module in settings.gradle file
 change the class name BookImpl_1_1 to BookImpl_1_2 and so on...
 update the method for different response.
 build the jar and copy and paste parallel to dynamicws.jar and your new REST api is ready!


##License
The `dynamicws` build plugin is released under The MIT License (MIT)
[MIT License](https://github.com/nileshdarade/dynamicws/blob/master/LICENSE). Distributions
Compliance with this license is
assured by including the https://github.com/nileshdarade/dynamicws/blob/master/LICENSE file in the dynamicws archive, which
this plugin does automatically.
