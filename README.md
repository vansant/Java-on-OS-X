Java-8-on-OS-X-Mavericks
======================

Java Development on OS X Mavericks

##Download the Java (Standard Edition) Developer Kit 
Visit http://www.oracle.com/technetwork/java/javase/downloads/index.html to get the most recent version of the Java Platform (JDK). At the time of this writing it is version 8u5 and the OS X download is named jdk-8u5-macosx-x64.dmg.

##Java 8 Installation - Standard
Open jdk-8u5-macosx-x64.dmg and double click on JDK 8 Update 05.pkg and follow the on screen instructions.

## Java 8 Installation - Without Admin Rights

###Install Java Binaries from the Apple Disk Image (.dmg) to ~/java
Mount the jdk-8u5-macosx-x64.dmg and drag the JDK 8 Update 05.pkg to the desktop.

Run in terminal: 
* $cd Desktop
* $pkgutil --expand JDK\ 8\ Update\ 05.pkg folder
* $cd folder
* $cp jdk18005.pkg/Payload files.gz
* $gunzip files.gz
* $cpio -iv < files
* $mkdir ~/java
* $cp -r Contents/Home ~/java 

### Add $JAVA_HOME Environment Variable and Add $JAVA_HOME to $PATH
Run in terminal:
* $nano ~/.bash_profile
* Add the following export statments
* export JAVA_HOME=(~/java/Home)
* export PATH=$JAVA_HOME/bin:$PATH
* Save ~/.bash_profile and close nano
* $source ~/.bash_profile
* $which java
* $which javac

