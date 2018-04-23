# NIH---Task4
Included is work for Task 4 of the proficiency test. 

Research Completed and Problems: 

Laptop Properties: 

Windows 10 - 64bit
Visual Studio 2017 with Anaconda

Java Installation:
-  Have installed JDK and JRE 10, but Javabridge was unable to discover the location of JVM and JRE using Registry entries, so I copied Java to a location without spaces and created JDK_HOME and JAVA_HOME environment variables pointing to it.

Cell Profiler Source Installation:
1. Started source installation of CellProfiler using directions at https://github.com/CellProfiler/CellProfiler/wiki/Source-installation-%28Windows%29
However, found that pip installation of various (javabridge, MySqlDb, etc) was was unable to find compatible versions for my machine.

2. Switched to Conda based installation and created a Python enviroment using directions at https://github.com/CellProfiler/CellProfiler/wiki/Conda-Installation. It was unable to discover Java using Registry entries. However, after further inspecting the code I found that it can could also JRE_HOME environment variable, so used the same.

Cell Profiler Source Execution:
- Starting Cellprofiler using __main__.py found that Wx installed with the Conda installation above was incompatible. Upon researching issues on CellProfiler Github, discovered that it needed classic Wx. So downloaded and installed classic Wx from SourceForge (https://sourceforge.net/projects/wxpython/files/wxPython/3.0.2.0/)

Cell Profiler Source Debugging:
- I was able to do source debugging in Visual Studio by executing from a local copy of the master branch and from the CellProfiler installation site-packages. 
- In debug mode, I was able to run Cellprofiler and create a project, load images, create a pipeline with modules and execute the pipeline.

Using Cellprofiler Programmatically:
- It appears that documentation about the programmatic use of Cellprofiler is very sparse. There was only page with very little information at https://github.com/CellProfiler/CellProfiler/wiki/CellProfiler-as-a-Python-package

- I started reviewing source code to understand Cellprofiler, especially test code in files such as test_measureimageoccupiedarea.py.

Cellprofiler Study:
- I have reviewed the Cellprofiler website including the following:
 - https://github.com/CellProfiler/CellProfiler/wiki/Module-structure-and-data-storage-retrieval
 - https://github.com/CellProfiler/CellProfiler/wiki/Orientation-to-CellProfiler-code
 - http://cellprofiler.org/tutorials/ 
