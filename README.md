
![Banner image](images/github-header-banner.png)

This is the homepage for the EDI Inspector, a desktop application designed to let you view, validate, and edit 
DI data within an intuitive editor.
It works alongside the BerryWave API for EDI <https://www.berrywave-edi.com/>,
an on-premise solution that enables you to seamlessly integrate EDI capabilities into your production workflows.

### Community Edition - Public Beta

A beta version of the free Community Edition is now available. You can access it using the link provided below, along with the accompanying setup instructions.

### Cross-Platform: Linux, Mac, and Windows

This release is distributed as a standalone Java “fat” JAR that can be run on any system with Java installed.
Native installers for macOS (.dmg) and Microsoft Windows (.msi) will be included with the official release.

### Data Privacy

The application operates entirely locally and does not rely on any cloud services. All data remains securely on your desktop and is never transmitted elsewhere.

### Community and Enterprise Editions

The Community Edition is free and provides a rich set of fully-functional features.

* View EDI content for X12 and EDIFACT in an EDI-aware editor window
* With color-highlighting for the many delimiters, terminators, and other syntax characters
* Validate structural correctness of EDI enveloping
* Repair structural errors
* Save modified EDI content

The Enterprise Edition is available from BerryWave Software with a site license
and includes all the features in the Community Edition plus additional features.

* Support for HL7 and TRADACOMS
* Perform full compliance checking via EDI models for specific document/version pairs
* Repair compliance errors
* Generate EDI acknowledgments
* Industry-specific inspections
  * claim balancing for 837 health care claims
  * customized inspections created by BerryWave Software for your critical transactions

### Running the Application

Platform-specific installers will be included as an option in future releases.
With the current Beta release, the application is launched from the command line
and uses Java separately installed on your computer.

**Prerequisite:** Java 21 or later. Verify with:

```sh

java --version

```

**Start the application**

Download the runnable jar and then start it from the command line:

```sh

java -jar edi-inspector-0.9.0-beta.1.jar

```

### User interface provided via your browser

The EDI Inspector interface runs in a browser tab.
The application communicates with your browser through a port on your local machine. 
By default, it selects an available port and opens a new tab in your default browser for easy access.

### Configuring a specific port

If you’d rather not have the application automatically select an available port, you can specify a particular port yourself via the command line.
For example:

```sh

java -jar edi-inspector-0.9.0-beta.1.jar  --server.port=8085

```


### Opening the application in your browser

When the application starts, it prints a local URL to the terminal. You can open this URL manually in your web browser.

This is useful if your browser does not allow the application to open a new tab automatically.

For example, you may see:

```
EDI Inspector started
Open in browser:
http://localhost:12345
```

Copy this URL and paste it into your browser’s address bar to access the application.