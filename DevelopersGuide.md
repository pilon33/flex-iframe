
---

## Get Flex-IFrame sources ##
Follow the instructions [here](http://code.google.com/p/flex-iframe/source/checkout).


---

## Build Flex-IFrame ##

### Using Flex/Flash builder ###
You can import the `library` module and each of the examples as Flex projects.

### Using Maven ###
This is the preferred way to build Flex-IFrame, because it does much more than just compiling the SWC: it runs unit tests, generates the asdoc, builds the examples, packages the sources and the assembly you can find on the download page.

To build the project, you must have [Maven](http://maven.apache.org/download.html).

You must add some repositoires to Maven's [settings.xml](http://maven.apache.org/settings.html) file:
```
  <activeProfiles>
    <activeProfile>flex</activeProfile>
  </activeProfiles>

  <profiles>
    <profile>
      <id>flex</id>
      <repositories>
        <repository>
          <id>flex-mojos-repository</id>
          <url>http://repository.sonatype.org/content/groups/flexgroup/</url>
          <releases>
            <enabled>true</enabled>
          </releases>
          <snapshots>
            <enabled>false</enabled>
          </snapshots>
        </repository>
      </repositories>
      <pluginRepositories>
        <pluginRepository>
          <id>flex-mojos-plugin-repository</id>
          <url>http://repository.sonatype.org/content/groups/flexgroup/</url>
          <releases>
            <enabled>true</enabled>
          </releases>
          <snapshots>
            <enabled>false</enabled>
          </snapshots>
        </pluginRepository>
      </pluginRepositories>
    </profile>
  </profiles>
```

Then just run the following command at the root of the project:
```
mvn clean install
```