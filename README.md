# BerryWave EDI Inspector

![Banner image](images/github-header-banner.png)

This is the homepage for the EDI Inspector, a desktop application designed to let you view, validate, and edit EDI data
within an intuitive editor. It works alongside the [BerryWave API for EDI](https://www.berrywave-edi.com/), an
on-premise solution that enables you to seamlessly integrate EDI capabilities into your production workflows.

## Community Edition

The first release of the free Community Edition is now available. You can download it from the *Releases* page and run
it as described below. An Enterprise Edition is coming soon with additional features.

## Cross-Platform: Linux, Mac, and Windows

This release is distributed as a standalone Java "fat" JAR that can be run on any system with Java 21 installed. Native
installers for macOS (`.dmg`) and Microsoft Windows (`.msi`) are planned for later.

## Data Privacy

The application operates entirely locally and does not rely on any cloud services. All data remains securely on your
desktop and is never transmitted elsewhere.

## Community and Enterprise Editions

The Community Edition is free and provides a rich set of fully-functional features. The Enterprise Edition will soon be
available from BerryWave Software with a site license. Contact us for further details.

| Feature                                                    |        Community Edition        |               Enterprise Edition               |
|:-----------------------------------------------------------|:-------------------------------:|:----------------------------------------------:|
| View X12 and EDIFACT content in an EDI-aware editor        |                ✅                |                       ✅                        |
| Color-highlighting for delimiters, terminators, and syntax |                ✅                |                       ✅                        |
| Summary Overview of business content                       |                ✅                |                       ✅                        |
| Validate structural correctness of EDI enveloping          |                ✅                |                       ✅                        |
| Repair structural errors & save modified content           |                ✅                |                       ✅                        |
| Large file support                                         | Up 500 segments or 10 documents | Up to 100,000 segments and unlimited documents |
| Support for HL7 and TRADACOMS                              |                ❌                |                       ✅                        |
| Full compliance checking via EDI models (document/version) |                ❌                |                       ✅                        |
| Repair compliance errors                                   |                ❌                |                       ✅                        |
| Generate EDI acknowledgments                               |                ❌                |                       ✅                        |
| 837 Health Care Claim balancing                            |                ❌                |                       ✅                        |

---

## Running the Application

The application is launched from the command line and uses Java separately installed on your computer. Platform-specific
installers are planned as an option in future releases.

### Prerequisites

- **Java 21 (LTS) or later.** Verify your installation by running:
  ```bash
  java --version
  ```

### Download and Unzip

1. Use the **Releases** link to navigate to the assets for the latest release.
2. Download the `edi-inspector-1.0.0.zip` asset. *(Note: You can disregard the Source .zip and tar.gz assets generated
   by GitHub).*
3. Unzip it into an installation directory of your choice.

Once unzipped, your directory structure will look like this:

```
└── edi-inspector-1.0.0/
    ├── edi-inspector.sh
    ├── edi-inspector.bat
    └── edi-inspector-1.0.0.jar
```

### Start the Application 

Open your terminal or command prompt, navigate to your installation directory,
and run the script for your platform:

* Mac or Linux:

```sh
edi-inspector.sh
```

* Windows:

```sh
edi-inspector.bat
```

### User Interface Provided via your Browser

The EDI Inspector interface runs in a browser tab.
The application communicates with your browser through a port on your local machine.
By default, it selects an available port and opens a new tab in your default browser for easy access.

#### Automatically Opened Browser Tab

The application attempts to open a new tab in your default browser. In some environments,
it may be necessary to open the tab directly.

#### Opening a Browser Tab Yourself

When the application starts, it prints a local URL to the terminal.
You can copy and paste this URL manually into your web browser's address bar.

For example, you may see:

```
EDI Inspector started
Open in browser:
http://localhost:12345
```

### Configuring a Specific Port

If you would rather not have the application automatically select an available port,
you can lock down a specific port by editing the `application.yml` configuration file
that is created when the application starts.

The **About** menu choice inside the application shows you exactly where that file lives on your computer,
or you can find it in the `.ediinspector` folder within your user home directory.