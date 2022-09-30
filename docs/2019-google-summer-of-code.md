This document is a summary of the work that was done for Google Summer of Code 2019.

Student: Jiwon Shin ([@js6450](https://github.com/js6450))

Mentor: Shawn Van Every ([@vanevery](https://github.com/vanevery))

Organization: [Processing Foundation](https://processingfoundation.org/)

# Project Links:

- [p5.serialport](https://github.com/p5-serial/p5.serialport) - A p5.js library that enables communication between your p5 sketch and Arduino (or another serial enabled device).
- [p5.serialcontrol](https://github.com/p5-serial/p5.serialcontrol) - GUI (Electron) application for use with p5.serialport
- [API Documentation Website](https://p5-serial.github.io/) - API documentation for p5.serialport

# Work Done

- Reorganize code base by creating a [p5-serial organization repository](https://github.com/p5-serial)
- Update and improvements to [p5.serialport](https://github.com/p5-serial/p5.serialport) - see commits [here](https://github.com/p5-serial/p5.serialport/search?q=author%3Ajs6450&type=Commits)
  - Multiple serial device connection feature added
    - Changed structure of p5.serialport libary to be modular to allow web clients to maintain individual list of serial devices connected, and vice versa.
  - Serial device close call enhanced to allow web client's direct close call to close serial device connection
  - Updated npm packages to its latest versions
  - Update code base to ES6 javascript, including [code examples](https://github.com/p5-serial/p5.serialport/tree/master/examples)
- Update functionality and styles of [p5.serialcontrol](https://github.com/p5-serial/p5.serialcontrol) - see commits [here](https://github.com/p5-serial/p5.serialcontrol/search?q=author%3Ajs6450&type=Commits)
  - Merged [feature-a11y](https://github.com/p5-serial/p5.serialcontrol/tree/feature-a11y/wenqi) branch that updated p5.serialcontrol application with accessible designs by @wenqi
    - Adjusted code in feature-a11y branch to disable parts that were still in development
  - User interface changed to reflect multiple serial device connection feature
    - Disconnect feature modified to close a specific serial port
    - Listing available serial ports excludes already connected serial ports
    - Master list indicates which ports remain connected
  - Updated serial console monitor to allow serial data to be read in ASCII
  - Generates p5.js code based on the number of connected ports and their names
  - Added menu bars to the application to link to license, Github repo, API documentation and code examples
    - Added application icons for packaging for various platforms
  - Package script available to package for Mac, Windows and Linux
  - Releases of the p5.serialcontrol application during GSoC 2019 (read release notes for major updates for each release):
    - [Alpha 7](https://github.com/p5-serial/p5.serialcontrol/releases/tag/0.0.7)
    - [Beta 1](https://github.com/p5-serial/p5.serialcontrol/releases/tag/0.1.0)
    - [Beta 1.1](https://github.com/p5-serial/p5.serialcontrol/releases/tag/0.1.1)
- Update [documentation website](https://p5-serial.github.io/) - see commits [here](https://github.com/p5-serial/p5-serial.github.io/search?q=author%3Ajs6450&type=Commits)
  - Used [jsdoc](https://github.com/jsdoc/jsdoc) to build documentation website (previous documentation website was built using YUI doc, which is now discontinued)
  - API documentation re-written for new updates to p5.serialport
- Added code examples to p5 web editor for users to quickly test p5.serialport and p5.serialcontrol application

# Potential Areas for Future Development

- Research about potential solution for HTTPS access for remote connection
- Generating p5.js code on the p5 web editor instead of doing so inside of the p5.serialcontrol application
