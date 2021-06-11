# custom-eclipse-ide
A maven eclipse plugin project for building customized eclipse IDE.

## Goals

The project has these goals:

* To build customized eclipse IDE with customized feature set by pulling features from update sites when requirements cannot be met by feature sets of the official releases.

## Usage

    git clone https://github.com/apuex/custom-eclipse-ide.git
    
### Add Repositories
    
    cd custom-eclipse-ide/releng/repo.config
    vim pom.xml

Add you favorite feature repository site to the &lt;repositories/&gt; section, with your favorite text editor. 
Add Scala IDE repository, for instance, 

    ...
    <properties>
      <scala-ide-repo.url>http://downloads.typesafe.com/scalaide/sdk/lithium/e47/scala212/stable/site</scala-ide-repo.url>
    </properties>
    <repositories>
      ...
      <repository>
        <id>scala-ide</id>
        <url>${scala-ide-repo.url}</url>
        <layout>p2</layout>
      </repository>
    </repositories>
    ...

### Create Your Customized Eclipse Project
There are already pre-packed custom eclipse ide projects included for reference. You may

* Edit the releng/xxx.product/xxx.product or,
* Copy/Paste/Find/Replace, and add it as a module to releng/pom.xml... enjoy.

### Add Features/Plugins to Customized Eclipse
Add eclipse features instead of individual plugins, if your favorite feature is already packaged as feature, since it is too verbose to add individual plugins by hand.

### Build Package
Requires JDK 1.8+ and apache maven 3.6.3+
Maven 3.6.1 and 3.6.2 do not work with Tycho, see Bug 551674

    mvn package

### Run

    unzip xxx.zip
    xxx/eclipse

## Contribute to This Project

* Bugfixes/Enhancements are welcome.
* Do not submit your own eclipse customizations to this project.

