# Step to step to install setup appuim with Eclips or intelliJ on mac 

# How to Install and Run the Project

## This is the Part One Setup For Mac OSX

### This File Will Help You to Setup The Project From Scratch

In this Guide you will install Appium, Android Studio, Android SDK, Setup Environment

# Requirements
First What you Need to Config This Project
1. Eclips IDE 
2. JDK (11 or Heigher)
3. Android Studio To Install Emelators, Android SDK
4. Environment Configuration 
5. Project Libraries Like HttpClient, Appium, Selenium
6. TestNG Plugin

# Outside Resourses
Now Let's see what we need from Outside Resourses
> Note : Maybe we Dont Need all Links Here but this is the best resources during configuration, installation process

1. TestNG Plugin Link : https://dl.bintray.com/testng-team/testng-eclipse-release/6.14.3/
2. TestNG Plugin Name : (TestNG)
3. TestNG Help Link for Images : https://www.toolsqa.com/testng/install-testng/
4. Download JDK : We Need to Download JDK from Brew CLI : https://mkyong.com/java/how-to-install-java-on-mac-osx/
5. Download Eclips from Official Version : https://www.eclipse.org/downloads/packages/release/2020-09/r/eclipse-ide-enterprise-java-developers
6. Uninstall JDK From Mac OSX : https://stackoverflow.com/questions/19039752/removing-java-8-jdk-from-mac
7. Download Npm (Node Package Manager) : https://nodejs.org/en/download/
8. Download Appium From Github : https://github.com/appium/appium-desktop/releases/tag/v1.18.3

# Configuration Process
Now Lets move to Configuration Process for your Environment 

First We Need to Configure JDK inside the OSX like bellow
1. Open Terminal App
2. Write This Command (java -version)
3. Click Enter

Now You will see one of two options
1. JDK is Not Installed on your machine
2. JDK has Version on your Machine

> If your machine doesn't have JDK Follow This Steps if has Check Next Section
# 1. Your Machine doesn't have JDK and Java is not Installed on your machine

Now We Need to Install JDK and we can install it from Brew CLI
1. Open Terminal App
2. write this command brew update
3. write this command brew tap adoptopenjdk/openjdk
4. brew search jdk

Now What you will See inside your Terminal ...

'''
==> Casks
adoptopenjdk                             adoptopenjdk12                           adoptopenjdk13-openj9                    adoptopenjdk8-openj9-jre
adoptopenjdk10                           adoptopenjdk12-jre                       adoptopenjdk13-openj9-jre                adoptopenjdk8-openj9-jre-large
adoptopenjdk11                           adoptopenjdk12-openj9                    adoptopenjdk13-openj9-jre-large          adoptopenjdk8-openj9-large
adoptopenjdk11-jre                       adoptopenjdk12-openj9-jre                adoptopenjdk13-openj9-large              adoptopenjdk9
adoptopenjdk11-openj9                    adoptopenjdk12-openj9-jre-large          adoptopenjdk8                         oracle-jdk
adoptopenjdk11-openj9-jre                adoptopenjdk12-openj9-large              adoptopenjdk8                          oracle-jdk-javadoc
adoptopenjdk11-openj9-jre-large          adoptopenjdk13                           adoptopenjdk8-jre                        sapmachine-jdk
adoptopenjdk11-openj9-large              adoptopenjdk13-jre                       adoptopenjdk8-openj9
'''

A lot of Options because you are searching about Jdk Now We Need to Pick our own JDK To Use
You should pick Version 11 or Heigher to install JDK on your Machine
then Write this command inside your Terminal

brew cask install adoptopenjdk13
> Note : adoptopenjdk13 this is the Value We Picked from Previus List
After Terminal Finish the Installation Process you can write Commands Again
Now Write this command : java -version
you will see a Message Like this 

'''
openjdk version "13.0.2" 2020-01-14
OpenJDK Runtime Environment AdoptOpenJDK (build 13.0.2+8)
OpenJDK 64-Bit Server VM AdoptOpenJDK (build 13.0.2+8, mixed mode, sharing)
'''

This Message Means your machine now has JDK Version 13 and Java Virtual Machine Installed Successfully
Now First Step Done ...

# 2. Your Machine already has JDK and Java Installed on your machine
> Note : If you Completed the Previus Step Completly or Your JDK is 11 or heigher Move to Next Section
Now you already has Jdk 10 or Lower on your Machine ... We Need to UnInstall it from Your machine
1. Open Terminal App
2. Write this Command : sudo rm -rf /Library/Java/*
3. Write this Command : sudo rm -rf /Library/PreferencePanes/Java*
4. Write this Command : sudo rm -rf /Library/Internet\ Plug-Ins/Java*
5. Write this Command : java -version

Now You should see a popup dialog tells you your machine does not have and JDK installed you need to Install one To Continue

> Note (If you still see Previus JDK Version on your machine and not deleted write This Command on your Terminal)

'''
sudo rm -rf /Library/PreferencePanes/JavaControlPanel.prefPane
sudo rm -rf /Library/Internet\ Plug-Ins/JavaAppletPlugin.plugin
sudo rm -rf /Library/LaunchAgents/com.oracle.java.Java-Updater.plist
sudo rm -rf /Library/LaunchDaemons/com.oracle.java.Helper-Tool.plist
sudo rm -rf /Library/Preferences/com.oracle.java.Helper-Tool.plist
sudo rm -rf /System/Library/Frameworks/JavaVM.framework
sudo rm -rf /var/db/receipts/com.oracle.jdk8u65.bom
sudo rm -rf /var/db/receipts/com.oracle.jdk8u65.plist
sudo rm -rf /var/db/receipts/com.oracle.jre.bom
sudo rm -rf /var/db/receipts/com.oracle.jre.plist
sudo rm -rf /var/root/Library/Preferences/com.oracle.javadeployment.plist
sudo rm -rf ~/Library/Preferences/com.oracle.java.JavaAppletPlugin.plist
sudo rm -rf ~/Library/Preferences/com.oracle.javadeployment.plist
sudo rm -rf ~/.oracle_jre_usage
'''

> Again this Commands just when the Jdk not Removed from Your Deivce if removed skip this commands

In This Step now Your JDK UnInstalled Successfully lets return to Previus Step to install New JDK and setup out New JDK


# Second Step
Now You Installed the JDK Successfully Lets Move to Next Part to Install Eclips IDE
You Can Download the IDE from this Link : https://www.eclipse.org/downloads/packages/release/2020-09/r/eclipse-ide-enterprise-java-developers
Click on macOS x86_64 Button to Download the IDE
Install the IDE to your Applications On your Machine
Now Run Eclips and Create Empty Java Project

Now Your IDE is Installed Successfully Lets move to Next part

# TestNG Step
We Need to Install TestNG Plugin to Eclips to Start Connection with Appium
1. Click on Help from Eclips IDE
2. Click on install new Software 
3. Click On Add Button
4. You will See a Dialog with Name, Link
5. Enter the Name : TestNG
6. Enter the Link : https://dl.bintray.com/testng-team/testng-eclipse-release/6.14.3/
7. Pick TestNG from The Options Bellow
8. Now Click On Finish

Now you should Restart Your Eclips IDE close and Reopen Again
In this Step you installed the IDE Successfully ...

# Clone Project Step
Now You Need to Clone The Repository form Gitlab
1. Open the Terminal App
2. Write cd Downloads/
3. write mkdir JynxProject
4. cd JynxProject/
5. git clone (your Repo Url)

Now Your Project Cloned Successfully

# Now You should Install Node.js
1. Open This Link : https://nodejs.org/en/download/
2. Click on macOs Installer
3. Install Node
4. Open your Terminal App
5. write this command npm install -g appium
6. write this command npm init -y

Now Node.js Installed Successfully

# Download Appium Step
1. Open This Link : https://github.com/appium/appium-desktop/releases/tag/v1.18.3
2. Click on Appium-mac-1.18.3.dmg and Download the Dmg File
3. Install Appium in your Applications
4. Open Appium

Now You Installed Appium Successfully

# Install Android Studio
1. Open This Link : https://developer.android.com/studio
2. Click on Download Button and Install the IDE
3. Open the IDE and Complete the Steps
4. Create Empty Android Project with Dummy Information for This Project
5. when Open The IDE Click on AVD Manager from Toolbar (Follow this Link to Install Emelator : https://developer.android.com/studio/run/managing-avds)
Now Your Android SDK , Emelators Installed Successfully


# Environment Variables Configuration
We Need to Config our Environment Variables inside The OSX
Now You Need to Find Your Android Root Path with Platform Tools Path
> Note : You Can get the Full Url from this Link : https://www.josharcher.uk/code/find-path-to-folder-on-mac/

1. click on any file inside your Finder
2. Right Click and click on Get Info
3. You can Find Your Root Path of your Machine inside Where Section Like this Users/opensooquser/Library/
4. Now Open Your Terminal App
5. Open Android Studio
6. Click on SDK Manager Icon inside Toolbar Now You will see the Path Like this /Users/opensooquser/Library/Android/sdk in the top of Dialog
7. Copy This Path /Users/opensooquser/Library/Android/sdk to Note
8. Write This Line Inside Your Note export ANDROID_SDK_ROOT=Your Path Here without Any Space
9. Write This Line Inside Your Note export ANDROID_HOME=Your Path Here without Any Space/platform-tools
10. Write This Line Inside your Note export PATH=${PATH}:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools

Now Your Note Will be Like This

'''
export ANDROID_HOME=/Users/opensooquser/Library/Android/sdk/platform-tools
export ANDROID_SDK_ROOT=/Users/opensooquser/Library/Android/sdk
export PATH=${PATH}:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools
'''

Now Open Your Terminal and Paste them inside the Terminal one after one not all of them one time
Now write this Line inside your Terminal : export JAVA_HOME=/Library/Java/JavaVirtualMachines/adoptopenjdk-13.jdk/Contents/Home
> Note Make Sure this value (adoptopenjdk-13.jdk) matches what you installed in first step
If You dont Remember what is the Version
Write java -version inside Terminal and you will find the Version

Now Your Note Should be like this

'''
export ANDROID_HOME=/Users/opensooquser/Library/Android/sdk/platform-tools
export ANDROID_SDK_ROOT=/Users/opensooquser/Library/Android/sdk

export PATH=${PATH}:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools

export JAVA_HOME=/Library/Java/JavaVirtualMachines/adoptopenjdk-13.jdk/Contents/Home
/Library/Java/JavaVirtualMachines/adoptopenjdk-13.jdk/Contents/Home
'''

Lets Open Appium and Click on Edit Configuration
your will see a white Dialog resize it from bottom and right you will see the 2 text fields waiting you to write paths
1. Android Home -> /Users/opensooquser/Library/Android/sdk/platform-tools
2. Java Home -> /Library/Java/JavaVirtualMachines/adoptopenjdk-13.jdk/Contents/Home

write them Like this Then Save and Restart Appium

# Validation Process
1. Open Your Terminal
2. write this Command printenv

Now Your will see your machine environment variables
you should validate the ANDROID_SDK_ROOT / ANDROID_HOME / JAVA_HOME
this 3 values should match the values inside your note
if all values matches then your Configuration is Ready

# Run Appium
1. Open Appium App
2. enter The Host 127.0.0.1
3. Enter the Port 4726
4. Click On start Server

# Import The Project inside Eclips
1. Open Eclips IDE
2. Click on File / Import
3. Maven Project / Existing Maven Project
4. Choose Jynx Folder
5. Click on Finish
6. Right Click on Appium Folder and Click on Build Path / Configure Build Path
7. Click On Libraries then Jars and Select All Jars
8. Click again on Add Jars then Select Selenium Jar and Click Finish
9. Open parallel.xml file and open it
10. Go to test you want to Run

'''
<test name="Note10">
	<parameter name="runAs" value="grid"></parameter>
	<parameter name="runOn" value="RF8N612N65H"></parameter>
	<parameter name="host" value="http://127.0.0.1:4726/wd/hub"></parameter>
		<classes>
			<class name="com.opensooq.automation.scenario.DeActivatedPost" />
			<class name="com.opensooq.automation.scenario.AddPost" />	
		</classes>
</test>
'''

change the Port inside Host Url to match the port in Appium
Now You should Move the Source Code From com folder
drag com folder inside main / java and paste it here
Now You Moved the Source Code to Root Package inside The Application

# Change the Apk Name
1. Open /Appium/src/luncherConfig.json
2. CHange the Apk Name to Match the Apk inside Apk Folder
3. Save Changes

# Change Paths Inside Config
1. Open LauncherConfig class inside Config Package and Write this In First Line : System.out.println("The Current Path is : " + new File("").getAbsolutePath());
2. Run Parallel.xml in TestNG you will see the Path inside First Line
3. Go To LauncherConfig Class and Change the Paths to be AS the same pathes in your device (src files inside jynix project take the same pathes where you located theme)

for example
private static final String APK_FILE_PREFIX = "/Users/opensooquser/Downloads/gitt/jynx/Appium/src/apks/";
private static final String LUNCHER_PATH = "/Users/opensooquser/Downloads/gitt/jynx/Appium/src/luncherConfig.json";
This Paths will be form the Print Line to Appium File it's mean
1. the Output of the Print Statement will be like this Users/opensooquser/Downloads/gitt/jynx/Appium
2. The Value Should be Like this When you paste it
private static final String LUNCHER_PATH = "/Users/opensooquser/Downloads/gitt/jynx/Appium/src/luncherConfig.json";

Also Change the Paths Inside Config Class to be like this
private static final String CONFIG_PATH = "/Users/opensooquser/Downloads/gitt/jynx/Appium/src/config.json";
private static final String STAGING_CONFIG_PATH = "/Users/opensooquser/Downloads/gitt/jynx/Appium/src/stagingConfig.json";

Now Start The Tests and You will see all tests working on Android and this Device can be decided from pararllel.xml 
<parameter name="runOn" value="{Here is the Device Number}"></parameter>

# Get Device Number
1. Open Terminal
2. Write this command adb devices
3. Pick the Device Number and Paste it in Prev Parameter
4. Now Run TestNG On This Deivce

# Dependencies Errors
If You see Missing Libraries or Dependencies after add All Jars and Selenium Jar
Add This Dependencies inside pom.xml inside <dependencies>

'''
<!-- https://mvnrepository.com/artifact/org.seleniumhq.selenium/selenium-java -->
<dependency>
    <groupId>org.seleniumhq.selenium</groupId>
    <artifactId>selenium-java</artifactId>
    <version>4.0.0-alpha-7</version>
</dependency>
		
<!-- https://mvnrepository.com/artifact/org.seleniumhq.selenium/selenium-api -->
<dependency>
    <groupId>org.seleniumhq.selenium</groupId>
    <artifactId>selenium-api</artifactId>
    <version>4.0.0-alpha-7</version>
</dependency>
		
<!-- https://mvnrepository.com/artifact/org.seleniumhq.selenium/selenium-server -->
<dependency>
    <groupId>org.seleniumhq.selenium</groupId>
    <artifactId>selenium-server</artifactId>
    <version>4.0.0-alpha-2</version>
</dependency>
		
<!-- https://mvnrepository.com/artifact/org.seleniumhq.selenium/selenium-support -->
<dependency>
    <groupId>org.seleniumhq.selenium</groupId>
    <artifactId>selenium-support</artifactId>
    <version>4.0.0-alpha-7</version>
</dependency>
		
<!-- https://mvnrepository.com/artifact/org.seleniumhq.selenium/selenium-remote-driver -->
<dependency>
    <groupId>org.seleniumhq.selenium</groupId>
    <artifactId>selenium-remote-driver</artifactId>
    <version>4.0.0-alpha-7</version>
</dependency>
		
<!-- https://mvnrepository.com/artifact/org.seleniumhq.selenium/selenium -->
<dependency>
    <groupId>org.seleniumhq.selenium</groupId>
    <artifactId>selenium</artifactId>
    <version>2.0rc2</version>
    <type>pom</type>
</dependency>
		
<!-- https://mvnrepository.com/artifact/org.seleniumhq.selenium/selenium-ie-driver -->
<dependency>
    <groupId>org.seleniumhq.selenium</groupId>
    <artifactId>selenium-ie-driver</artifactId>
    <version>4.0.0-alpha-7</version>
</dependency>
		
		
<!-- https://mvnrepository.com/artifact/io.appium/java-client -->
<dependency>
    <groupId>io.appium</groupId>
    <artifactId>java-client</artifactId>
    <version>7.4.1</version>
</dependency>
		
<!-- https://mvnrepository.com/artifact/com.comcast.magic-wand/appium -->
<dependency>
    <groupId>com.comcast.magic-wand</groupId>
    <artifactId>appium</artifactId>
    <version>4.0.3</version>
</dependency>
		
		
<dependency>
    <groupId>org.slf4j</groupId>
    <artifactId>slf4j-api</artifactId>
    <version>2.0.0-alpha1</version>
</dependency>

<dependency>
    <groupId>org.slf4j</groupId>
    <artifactId>slf4j-simple</artifactId>
    <version>2.0.0-alpha1</version>
</dependency>
		
<!-- https://mvnrepository.com/artifact/org.apache.httpcomponents/httpclient -->
<dependency>
    <groupId>org.apache.httpcomponents</groupId>
    <artifactId>httpclient</artifactId>
    <version>4.5.13</version>
</dependency>
		
		
<!-- https://mvnrepository.com/artifact/io.appium/java-client -->
<dependency>
    <groupId>io.appium</groupId>
    <artifactId>java-client</artifactId>
    <version>7.4.1</version>
</dependency>

<dependency>
    <groupId>org.testng</groupId>
    <artifactId>testng</artifactId>
    <version>7.3.0</version>
    <scope>test</scope>
</dependency>
''' 

2. Make Sure Your Build Block looks like this
'''
<build>

		<plugins>
		<plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-compiler-plugin</artifactId>
                <version>3.8.1</version>
                <configuration>
                    <release>11</release>
                </configuration>
            </plugin>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-surefire-plugin</artifactId>
				<version>3.0.0-M1</version>
				<configuration>
					<forkCount>3</forkCount>
					<reuseForks>false</reuseForks>
					<suiteXmlFiles>
						<file>parallel.xml</file>
					</suiteXmlFiles>
					<properties>
						<property>
							<name>suitethreadpoolsize</name>
							<value>2</value>
						</property>
					</properties>
				</configuration>
			</plugin>
		</plugins>
	</build>
'''


If you see JAVA_HOME / ANDROID_ROOT or Connection Refuse with This 2 Values the Problem in Server Side your JAVA_HOME / ANDROID_HOME is Invalid Inside Appium Configuration when You Clicked on Edit Configuration
Check this Values and should match the values inside Terminal when you use printenv command

