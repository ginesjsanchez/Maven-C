# Maven-C
Parent poms and tools to mavenize C/C++ projects

This is an initial version extracted from a case study of successful mavenization of a C++ project. Need more generalization work removed or adapting the parts that were specific to that project.

The C part must be completed for executable and libraries. Only the C++ has been tested.

The project had specific poms for the generation of SOAP libraries and services that I have yet to review and upload.

Pom organization:

./parent-pom
.	|
.	|--/nar-parent-pom
.			|
.			|--/c-parent-pom
.			|
.			|--/cpp-parent-pom
.					|
.					|--/lib-parent-pom
.					|
.					|--/stlib-parent-pom
.					|
.					|--/exe-parent-pom
.			

In Settings.xml profile properties

    <profile>
		<id>cpp</id>
		<properties>
			<cygwinDir>XXXXXX</cygwinDir>
			
			<sysIncDir>${cygwinDir}/usr/include</sysIncDir>
			<sysIncDir2>${cygwinDir}/usr/local/include</sysIncDir2>
			<sysLibDir1>${cygwinDir}/lib</sysLibDir1>		
			<sysLibDir2>${cygwinDir}/usr/local/lib</sysLibDir2>
			
			<cppCheckDir>${cygwinDir}/bin</cppCheckDir>
			
			<oraDir>XXXXXX</oraDir>
			<oraClientDir>${oraDir}\instantclient_19_12</oraClientDir>
		</properties>
    </profile>

