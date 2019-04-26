# lejos-ev3-netbeans
Build.xml script for using NetBeans with LeJOS EV3 to develop Java applications for the LEGO MINDSTORMS EV3

Developed and tested in Apache NetBeans 11.0 running on Windows.

Copy build.xml and replace the default build.xml in your NetBeans project.

Overrides standard actions "Run", "Run file", "Debug" and "Debug file"
to compile a .jar file for the EV3 and uploads it to the brick via USB.

For the override to work the setting "Compile on Save" must be disabled
in the project properties, 'Build -> Compiling -> Compile on Save', 
as described in the header of this file.

Must target Java 7 in project properties to run on EV3, 
'Sources -> Source/Binary Format: -> JDK 7'.

The property "ev3.run.remote" in build.xml can be set to automatically start
the program after upload, but use with care as this will interfere with
the menu system running on the EV3. The preferred method is to upload
the program and start it from the menu.

When debugging a program, whether started remotely or from the EV3 menu,
Go to 'Debug -> Attach debugger...' and connect to the running program,
by default with Host: 10.0.1.1 and Port: 8000.


## Dependencies

* [Java JDK 8](https://www.oracle.com/technetwork/java/javaee/downloads/jdk8-downloads-2133151.html) OR [Java JDK 7](https://www.oracle.com/technetwork/java/javase/downloads/java-archive-downloads-javase7-521261.html)
* [Java JRE 7 for EV3](https://www.oracle.com/technetwork/java/embedded/downloads/javase/javaseemeddedev3-1982511.html)
* [NetBeans 11.0](https://netbeans.apache.org/download/nb110/nb110.html)
* [LeJOS EV3 0.9.1-beta](https://sourceforge.net/projects/ev3.lejos.p/files/)

### LeJOS windows installation instructions
<https://sourceforge.net/p/lejos/wiki/Windows%20Installation/>


### Inspiration taken from
<https://github.com/jabrena/liverobots/blob/master/build.xml>
