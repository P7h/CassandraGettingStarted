# Getting started with Cassandra

----------

## Introduction
This is corrected code of [Getting Started with Apache Cassandra and Java (Part I)](http://planetcassandra.org/getting-started-with-apache-cassandra-and-java/) and [Getting Started with Apache Cassandra and Java (Part II)](http://www.planetcassandra.org/getting-started-with-apache-cassandra-and-java-part-2/).

The packages in Cassandra have been refactored in the most recent versions. But Getting Started blogposts were not updated for the same.
This code fixes all those compilation errors and also helps to execute the code with ease using a simple Gradle script.

## Usage
To build and run the code, you must use Java 1.8.<br>

Command to execute [GettingStarted.java](src/test/java/org/p7h/cassandra/gettingstarted/GettingStarted.java) is:

    gradle --no-color

Comment out line[#3](build.gradle#L3) in `build.gradle` and uncomment line[#4](build.gradle#L4) for `mainClassName` to execute the other class [GettingStartedTwo.java](src/test/java/org/p7h/cassandra/gettingstarted/GettingStartedTwo.java) in this repo. This class can be executed as before:

    gradle --no-color

## Problems
If you come across any issues, please report them either raising an [issue](https://github.com/P7h/CassandraGettingStarted/issues) here on GitHub or alert me on Twitter [@P7h](http://twitter.com/P7h). Or even better, please send a [pull request](https://github.com/P7h/CassandraGettingStarted/pulls).<br>
Appreciate your help. Thanks!


## License
Copyright &copy; 2015 Prashanth Babu.<br>
Licensed under the [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0).