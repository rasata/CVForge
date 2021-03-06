## CVForge 1.0

Watch the demo videos on YouTube:
* https://youtu.be/irnBuvW2dEo Feature demonstration of version 0.2.0 beta
* https://youtu.be/vztRXJx6R44 Linux support of version 0.3.0 beta
* https://youtu.be/lmhwSU9VItE Feature demonstration of version 0.5.0 beta
* https://www.youtube.com/watch?v=PDQCJ47GEAw Shard creation demo


Project in maintenance. Feel free to send bug reports and feature wish lists.

Pre-built jars are available in the "build" directory.
ImageJ with Java8 is required.
If you encounter bugs or strange behaviour, please send a report to janmartens@live.de
A report should contain error messages, a list of steps leading to the bug and the image you used.  



CVForge aims to close the gap between the popular tool ImageJ and the powerful OpenCV library.
This plugin gives access to all methods of OpenCV, independent from it's version.
Expand and boost ImageJ with OpenCV's selection of powerful methods.
Use the guides and documentation on the OpenCV website for detailed information on efficient usage:
* http://docs.opencv.org/2.4/doc/tutorials/tutorials.html
* http://docs.opencv.org/2.4/modules/refman.html
* http://opencv.org/opencv-java-api.html



Check out the CVForge shards! They extend CVForge and simplify method usage.
ArmorShard:
* (to be released) [ArmorShard](https://github.com/m4dguy/ArmorShard): Offers simplified access and improved ImageJ integration of various OpenCV methods. Pick it up and take the lead!
* (to be released) [ImanShard](https://github.com/m4dguy/ImanShard): Image analysis shard for a handful of scenarios.
* [ShardDemo](https://github.com/m4dguy/ShardDemo): A demo example for developers.


 
## Why CVForge might be for you

* Expand your ImageJ functionality:
OpenCV is a massive library containing a vast selection of cutting-edge methods.
It is actively maintained and gets updated and extended regularly.
If ImageJ is missing something you are looking for, you may find it here.

* Considerable speed boost:
Under-the-hood usage of C/C++ implementations lets you perform many operations in the blink of an eye.
Most methods you already know from ImageJ run faster and smoother here.

* Comfortable user-interface: 
OpenCV is a complex library which is meant to be used by programmers.
CVForge provides a graphical user interface to use OpenCV in the most comfortable way possible.

* Agnostic of OpenCV version:
Download the latest OpenCV version or use an earlier one.
You are free to load and use your own build of the OpenCV library.
No matter your preference, you can switch between different versions on-the-fly and choose the one which suits you best.

* ImageJ integration:
Enhance your productivity by recording actions and running them as ImageJ macros.
Use ImageJ's regions of of interest to analyze only specific parts of your image.

* Interface for Scripting:
Convert ImageJ objects to OpenCV objects and vice versa.
CVForge itself uses converters and gives you access to them through the separate "CVForgeConversion" jar for your own scripts.

* Flexible and portable support:
No matter if Windows, Linux or Mac, CVForge runs on all major operating systems with only slight differences and full functionality.
Independent of x86 or x64 architectures, CVForge dynamically switches to the one currently used.

* Shard system:
Import your own or other jars with code based purely on OpenCV.
Use them to perform complex processing and analysis workflows and bring the results back into ImageJ.



## Installation

Installation:
* Copy "CVForge_[version number].jar" and "CVForgeConversion.jar" into the ImageJ plugin folder.
* To use OpenCV functions, you need to install an OpenCV jar (see the following sections). Manual installation is recommended.

Automated OpenCV jar installation (Windows):
* Launch CVForge from inside of ImageJ
* In CVForge, click "Plugin" > "Install"
* Navigate to the OpenCV folder you downloaded from the OpenCV website
* Navigate to the "build" > "java" directory
* Select and open the file "opencv-[version number].jar"
* CVForge will copy the necessary files into the plugins folder of ImageJ
* Fiji users must restart the application.

Manual OpenCV jar installation (Windows):
* Navigate to the OpenCV folder you downloaded from the OpenCV website
* Go to "build" > "java"
* Copy-paste the content of this folder (subfolers included!) into ImageJ's plugin folder
* CVForge will detect and list the installed jar

OpenCV installation (Linux/ Mac):
* Download and build OpenCV on your system
* Once an OpenCV version with a java module is installed, CVForge will find and detect the jar on your system


## Towards Fiji
CVForge was build and optimised for use with ImageJ.
Internal key processes inside Fiji are different from plain ImageJ. 
Thus, the following bugs may occur: 
* Installation bug:
Automated OpenCV jar installation may cause an error message to pop up.
Installation will we successful though, but the user must restart Fiji.
* OpenCV jar switch:
Switching OpenCV jars will be of no effect.
Only the jar Fiji's classloaders finds first, can be used. 


## Build and development instructions
Simple build:
* Download and extract the src directory.
* Download a working OpenCV jar (version is arbitrary).
* Build the CVForgeConversion module and export it as a jar (this jar MUST be named CVForgeConversion.jar).
* Build the ReflectionTools and the CVForge modules.
* Export plugins.config, ReflectionTools and CVForge into a single jar (this will be the plugin's main jar).
* You will need both generated jars to run CVForge in ImageJ.

Running and testing inside the IDE:
* Copy the CVForgeConversion and the OpenCV jars into your IDE's build target directory.
* Run Main.java
