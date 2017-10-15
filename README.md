# custom-eclipse-ide
A maven eclipse plugin project for building customized eclipse IDE.

## Goals

The project has these goals:

* To build customized eclipse IDE with customized feature set, by pulling features from update sites, instead prescribed feature sets of the official releases.

## Usage

    git clone https://github.com/apuex/custom-eclipse-ide.git
    
### Add Repositories
    
    cd custom-eclipse-ide/releng/repo.config

Add you favorite feature repository site to the &lt;repositories/&gt; section, with your favorite text editor.

### Create Your Customized Eclipse Project
    There are already pre-packed custom eclipse ide projects included for reference. You may

* Edit the releng/xxx.product/xxx.product or,
* Copy/Paste/Find/Replace..., and add it as a module to releng/pom.xml enjoy.

### Add Features/Plugins to Customized Eclipse
Add eclipse features instead of individual plugins, if your favorite feature is already packaged as feature, because it is too verbose to add individual plugins.

### Build Package

    mvn package

### Run

    unzip xxx.zip
    xxx/eclipse

## Contribution to This Project

* Bugfixes/Enhancements are welcome.
* Do not submit your own customized eclipse product project, or eclipse feature set to this project.

