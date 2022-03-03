# HelloTomcat

## Requirements
1. Java 17
2. Maven
3. Apache Tomcat

## Building the webapp
You can build the webapp with the command

    mvn clean package

## Deploying the webapp to Tomcat
You can set the CATALINA_HOME environment variable to the location of Tomcat. The contents of $CATALINA_HOME should look like this:

    % ls $CATALINA_HOME
    BUILDING.txt	CONTRIBUTING.md	bin		conf		lib		logs		temp		webapps		work

Navigate to the root directory of HelloTomcat, where pom.xml is located. Now run the command:

    cp target/HelloTomcat.war $CATALINA_HOME/webapps

## Starting Tomcat
You can start Tomcat by navigating to the location of Tomcat, $CATALINA_HOME, and running the command:

    bin/startup.sh

This should expand the HelloTomcat.war file which is saved in the webapps folder.

## Stopping Tomcat
You can stop Tomcat by navigating to $CATALINA_HOME and running the command:

    bin/shutdown.sh

## Running and using the webapp
After starting Tomcat, point your browser to http://localhost:8080/HelloTomcat and you'll see the index page. 

You can also point your browser to http://localhost:8080/HelloTomcat/hello and you'll see the response by the servlet.
