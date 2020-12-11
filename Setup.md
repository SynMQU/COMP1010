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
2. Click `Next >` on this screen.

<img src="Resources/Setup/JDKInstall01.png" width="600"/>

3. Make sure you're installing in the program files directory, if elsewhere record the directory or change it. Then clicking `Next`.

<img src="Resources/Setup/JDKInstall02.png" width="600"/>

4. Wait for the installation process to conclude and then press `Close`.

<img src="Resources/Setup/JDKInstall03.png" width="600"/>

5. Run the `java -version` command again and see what it outputs

```
C:\Users\Test>java -version
java version "15.0.1" 2020-10-20
Java(TM) SE Runtime Environment (build 15.0.1+9-18)
Java HotSpot(TM) 64-Bit Server VM (build 15.0.1+9-18, mixed mode, sharing)
```

This is the correct output if the given installation is properly installed. Sometimes the system variables may still not be set up properly, so you should continue with the following:

6. When you have your windows search bar open type type `env` and choose `Edit the system environment variables`. Once open click on the `Environment Variables…` button.

<img src="Resources/Setup/EnvVarsSearch.png" width="600"/>

<img src="Resources/Setup/SystemProperties.png" width="600"/>

<img src="Resources/Setup/EnvironmentVariables.png" width="600"/>

7. Edit the `User variables` section from the `Path` group and edit or add the line for Java to have the path of `C:\Program Files\Java\jdk-15.0.1\bin`.

8. Edit or add the following entry in `System vairables` for `JAVA_HOME` with the path to the installed JDK as follows:

<img src="Resources/Setup/JavaHomeVar.png" width="600"/>