# mkyong_tutorials
Thanks to https://www.mkyong.com/ 

Uso interessante del plugin Maven di Eclipse
```xml
<plugin>
			<groupId>org.apache.maven.plugins</groupId>
			<artifactId>maven-eclipse-plugin</artifactId>
			<version>2.9</version>
			<configuration>
			        <!-- Always download and attach dependencies source code -->
				<downloadSources>true</downloadSources>
				<downloadJavadocs>false</downloadJavadocs>
				<!-- Avoid type mvn eclipse:eclipse -Dwtpversion=2.0 -->
				<!-- NB: The option -Dwtpversion=2.0 tells Maven to convert the project 
				into an Eclipse web project (WAR), not the default Java project (JAR) --> 
				<wtpversion>2.0</wtpversion>
			</configuration>
</plugin>
```
E del plugin Tomcat di Eclipse:

pom.xml
```xml
<!-- For Maven Tomcat Plugin -->
<plugin>
	<groupId>org.apache.tomcat.maven</groupId>
	<artifactId>tomcat7-maven-plugin</artifactId>
	<version>2.2</version>
	<configuration>
		<path>/CounterWebApp</path>
	</configuration>
</plugin>
```
Type this command :

mvn tomcat:run

It will start Tomcat and deploy your project default to port 8080.
