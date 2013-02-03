TTRT
====

TTRT is a compiler and runtime environment for TTCN3(a language specification by ETSI) written in Java.
It's partial implementation of ETSI's TTCN3 specifications.

*Please go through TODO,ISSUES file before using it.

<h2>Features</h2>
1. Partial implementation of TTCN3 specification.
2. Has partial implementation of TRI(TTCN runtime specification).
3. Comes with GUI logger which shows component interaction and messaging in real time.
4. Component flows can be exported as PNG file for future references.

<h2>Limitations</h2>
  Some of the main limitations are-

1. Poor syntax error handling.
2. No support for some of the basic data types Set,Union,enums.. etc yet.
3. No support for Arrays and Ranges.
4. No support for procedure based messaging. 
5. No support for broadcast/multicast yet.
6. No support for TCI specification yet.
7. Compiler error reporting has limitations.

For more details check TODO file

<h2>Dependencies</h2>
1. Antlr3.
2. Tools.jar – Comes with standard jdk.
3. TRITCI.jar – Requires only if you are using TRI/TCI inter face. At present it provides only  implementation of TRI interface.

*Tested on Java 1.6 ubuntu

<h2>Config Files</h2>
1. <b>TTRT.config</b>- Used by TTRT.jar.
2. <b>Adapter.config</b>- Used by TRITCI.jar.

*More details are given in config files it self.

<h2>Usage</h2>
<b>java -jar TTCN.jar  [-d] <TTCN3 file></b>

*if -d option is specified it will only translate ttcn3 files to corresponding java files.



<b>example-</b>
java -jar TTCN.jar testcase.ttcn3.

*TTCN3 file should be the file which is main test script(includes control statement).
*It assumes ttcn3 files should be saved as .ttcn3 extension(to solve dependency on other ttcn3 modules).
*Please check testcases in test folder.

<h2>TRI usage<h2>
Please check example codes(com.shiv.ttcn.test.Adapter.java)

<b>Requirements</b><br>
TRITCI.jar (for adapter developments)

Main Classes-<br>
	TriFactory<br>
	TriCommunicationHandler<br>
	IChannelEvents<br>
  
<h2>TTCN References</h2>
core language-<a>http://www.etsi.org/deliver/etsi_es/201800_201899/20187301/04.04.01_60/es_20187301v040401p.pdf</a><br>
tri specification-<a>http://www.etsi.org/deliver/etsi_es/201800_201899/20187305/04.04.01_60/es_20187305v040401p.pdf</a><br>
tci specification- <a>http://www.etsi.org/deliver/etsi_es/201800_201899/20187306/04.04.01_60/es_20187306v040401p.pdf</a><br>


*Any code modifications/Bug reports/fixes/suggestions are welcome. :)

<b>verion 0.1</b>
