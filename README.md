# docker-maven-java-app-archetype
Maven archetype for a dockerized Java standalone application with Maven build.

[![Build Status](https://jenkins.fuin.org/job/docker-maven-java-app-archetype/badge/icon)](https://jenkins.fuin.org/job/docker-maven-java-app-archetype/)
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/org.fuin.archetypes/docker-maven-java-app-archetype/badge.svg)](https://maven-badges.herokuapp.com/maven-central/org.fuin.archetypes/docker-maven-java-app-archetype/)
[![LGPLv3 License](http://img.shields.io/badge/license-LGPLv3-blue.svg)](https://www.gnu.org/licenses/lgpl.html)

This archetype was built using the [docker-maven-java-app](https://github.com/fuinorg/docker-maven-java-app) sample appliaction.

## Create project

**Mandatory Parameters**
```
mvn archetype:generate \
     -DarchetypeGroupId=org.fuin.archetypes \
     -DarchetypeArtifactId=docker-maven-java-app-archetype \
     -DarchetypeVersion=0.1.0-SNAPSHOT
```

**All Parameters**
```
mvn archetype:generate \
     -DarchetypeGroupId=org.fuin.archetypes \
     -DarchetypeArtifactId=docker-maven-java-app-archetype \
     -DarchetypeVersion=0.1.0-SNAPSHOT \
     -DgroupId="com.mycompany" \
     -DartifactId="my2ndapp" \
     -Dversion="0.1.0-SNAPSHOT" \
     -DpackageName="com.mycompany.my2ndapp" \
     -DpackagePath="com/mycompany/my2ndapp" \
     -DappName="my2ndapp" \
     -Dcompany="mycompany99"
```

**Explanation**
<table border="1" style="font-size:0.9em; text-align:left; vertical-align:top; padding-top:5px; padding-bottom:4px;">
<tr><th>Parameter</th><th>Default Value</th><th>Description</th></tr>
<tr><td>groupId</td><td>com.mycompany.mydsl</td><td>Maven 'groupId'</td></tr>
<tr><td>artifactId</td><td>com.mycompany.mydsl</td><td>Maven 'artifactId'</td></tr>
<tr><td>version</td><td>0.1.0-SNAPSHOT</td><td>Maven 'version'</td></tr>
<tr><td>packageName</td><td>com.mycompany.mydsl</td><td>Java Package (Should be most of the times identical to the 'groupId')</td></tr>
<tr><td>packagePath</td><td>com/mycompany/mydsl</td><td>Same as package, but instead of '.' the '/' is used as separator</td></tr>
<tr><td>appName</td><td>my2ndapp</td><td>Application and Docker repository name with least one lowercase, alpha-numeric characters, optionally separated by periods, dashes or underscores.  ('a'-'z', '0'-'9', '-', '_', No spaces)</td></tr>
<tr><td>company</td><td>mycompany99</td><td>Docker ID must be between 4 and 30 characters long, and can only contain numbers and lowercase letters ('a'-'z', '0'-'9', No spaces)</td></tr>
</table>

## Finalize the setup
In order to build the new project in Linux, you need to make the file 'mvnw' executable:

```
cd my2ndapp 
chmod +x mvnw
```

To build the application, see [docker-maven-java-app](https://github.com/fuinorg/docker-maven-java-app) for an explanation.


## Snapshots

Snapshots can be found on the [OSS Sonatype Snapshots Repository](http://oss.sonatype.org/content/repositories/snapshots/org/fuin "Snapshot Repository"). 

Add the following to your .m2/settings.xml to enable snapshots:

```xml
<repository>
    <id>sonatype.oss.snapshots</id>
    <name>Sonatype OSS Snapshot Repository</name>
    <url>http://oss.sonatype.org/content/repositories/snapshots</url>
    <releases>
        <enabled>false</enabled>
    </releases>
    <snapshots>
        <enabled>true</enabled>
    </snapshots>
</repository>
```

## More Archteypes

If you're looking for more Maven archetypes, take a look at [Open Archetypes](https://github.com/open-archetypes "Open Archetypes").
