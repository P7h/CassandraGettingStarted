# Getting started with Cassandra

----------

## Introduction
I just started with [`Apache Cassandra`](https://cassandra.apache.org) and was playing around looking at various sample code present in Planet Cassandra.
I followed [Getting Started with Apache Cassandra and Java (Part I)](http://planetcassandra.org/getting-started-with-apache-cassandra-and-java/) and [Getting Started with Apache Cassandra and Java (Part II)](http://www.planetcassandra.org/getting-started-with-apache-cassandra-and-java-part-2/) blogposts on [Planet Cassandra](http://www.planetcassandra.org), but I could not get the code to work due to the various compilation issues and code issues.

The packages in Cassandra have been refactored in the most recent versions. But Getting Started blogposts were not updated for the same. This repo has the corrected code for the above `Getting Started with Apache Cassandra` blogposts. This code fixes all those compilation errors and also helps to execute the code with ease using a simple Gradle script.

> Ideally this repo could just have been a simple test case oriented. Probably that makes more sense.

## DB Configuration
Please run the following commands on CQL before running the Java code.

    DROP KEYSPACE demo;
    CREATE KEYSPACE demo WITH REPLICATION = { 'class' : 'SimpleStrategy', 'replication_factor' : 3 };
    use demo;
    CREATE TABLE users (lastname text PRIMARY KEY, age int, city text, email text, firstname text);

## Usage
To build and run the code, you must use Java 1.8.<br>

Command to execute [GettingStarted.java](src/main/java/org/p7h/cassandra/gettingstarted/GettingStarted.java) is:

    gradle --no-color -PmainClassName=org.p7h.cassandra.gettingstarted.GettingStarted execute

Command to execute [GettingStartedTwo.java](src/main/java/org/p7h/cassandra/gettingstarted/GettingStartedTwo.java) is:

    gradle --no-color -PmainClassName=org.p7h.cassandra.gettingstarted.GettingStartedTwo execute

## Problems
This is very simple repo and there should not be any errors or issues with this code as such. But, if you find any issues, please report them either raising an [issue](https://github.com/P7h/CassandraGettingStarted/issues) here on GitHub or alert me on Twitter [@P7h](http://twitter.com/P7h). Or even better, please send a [pull request](https://github.com/P7h/CassandraGettingStarted/pulls).<br>
Appreciate your help. Thanks!

## License
Copyright &copy; 2015 Prashanth Babu.<br>
Licensed under the [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0).
