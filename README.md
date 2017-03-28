Overview
========

This sample uses the light weight SparkJava framework to implement a simple
hello world REST service that can return a message defined in an environment
variable.

See [Hello.java](src/main/java/example/Hello.java).

Building
========

Run `mvn clean package` to compile the code, generate a fat jar, and package it
in an archive (zip) file along with the ACCS manifest.json file.

Local Testing
=============

1. run `java -jar target/javaspark-hello-0.0.1-SNAPSHOT-jar-with-dependencies.jar`
2. GET "/" from the application to obtain the default greeting
3. Define the environment variable GREETING and restart the application.  It will
now return the value of GREETING when you GET "/".

Running on ACCS
===============

1. Create an ACCS application deploying the archive file `target/javaspark-hello-0.0.1-SNAPSHOT-dist.zip`.
2. Once the application is created and started open the application URL in a browser
or do a GET on it to obtain the default greeting.
3. Define the environment variable GREETING on the Deployments tab, apply the change
to restart the application and it will now return the value of GREETING.
