# **Java Installation Debugging**

Unlike COMP1000, where you used the Processing IDE, 1010 focuses on the broader Java language, Processing uses it's own branch of Java integrated into the program itself so no other setup is required. Although you may encounter some issues when trying to setup your development environment with either Eclipse or Visual Studio Code. These instructions were made for Windows, I will add notes for MacOS later, but with Eclipse the processes are pretty much the exact same.

## **Installing Java**

* [Oracle Java 15.0.1 JDK](https://download.oracle.com/otn-pub/java/jdk/15.0.1%2B9/51f4f36ad4ef43e39d0dfdbaf6549e32/jdk-15.0.1_windows-x64_bin.exe)
* [Eclipse Installer](https://www.eclipse.org/downloads/download.php?file=/oomph/epp/2020-09/R/eclipse-inst-jre-win64.exe&mirror_id=1051)

First you should open Command Prompt or your equivalent terminal application and run `java -version`. Depending on the following output you should attempt the following:

```
C:\Users\Test>java -version
'java' is not recognized as an internal or external command,
operable program or batch file.
```

If it doesn't come up with an error but instead displays information tied to an existing install that does not match the Java 15.0.1 you are trying to install then try the following:

```
java version "1.8.0_XXX"
<More information about installed version>
```

1. Run the executable you downloaded for the Java JDK.
2. Click 'Next' on this screen.

<img src="Resources/Setup/JDKInstall01.png" alt="JDKInstall01" width="200"/>