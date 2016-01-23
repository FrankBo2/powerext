## powerEXT Application Framework ##

powerEXT Application Framework is an Open Source based middleware and Application Framework, that enables IBM Power System i (IBM AS/400, IBM iSeries) users to embrace these new technologies by evoking the worlds most sofisticated WEB 2.0/RIA userinterface for enterprise systems - Ext JS.

powerEXT Application Framework is GNU GPL v3 licensed.

The download requires i5/OS V5R4M0 (or higher), WDS, SQL and powerEXT Core.

For more information on version changes please go to the forum that is available from the homepage at http://www.powerEXT.com .

Use Version 1.4 Installation Guide to install latest version

### **IMPORTANT! You have to install powerEXT Core before installation of the Application Framework - Core is NOT a part of this anymore.** ###



## powerEXT Core ##

powerEXT Core is an Open Source productivity tool.

Includes:
Special version of CGIDEV2:
- UTF8/16 file support,
- Responce Object Support,
- Variable length 65535 support,

powerEXT Core API: HTTP connecter & Productivity Services
(see the installation document for at complete list of subprocedures)

powerEXT Core is MIT licensed.

The download requires i5/OS V5R2M0 (or higher) and WDS.

Use Version 4.2 Installation Guide to install latest version.


## Updates ##

### 2015.06.02 powerEXT Core 5.0: ###

- V5R4M0 as earliest release supported

- Inline support for YAJL JSON reader/writer (included in the package)

- Misc. improvements in core sub-procedures

- Upload of this new version is moved to: http://powerext.com


### 2013.01.15 powerEXT Core 4.11: ###

jsonToXML subprocedure now replace blanks in JSON id's to
default underscore or by a character passed as an parameter.


### 2012.06.15 powerEXT Core 4.10: ###

new subprocedures added for easy reading of JSON

- getExtVarJson(urlparm:jsonPropertyId:defaultValue)

- jsonToField(jsonAddr:jsonSize:jsonPropertyId:defaultValue)


### 2012.06.08 powerEXT Core 4.9: ###

new subprocedures added to calculate and check hash strings

- hashGen(password:type:ccsid)
- hashCheck(password:hash:type:ccsid)


### 2012.03.16 powerEXT Core 4.8: ###

Support for 5250/STRPCCMD long URL (max 2048)

see PXURL\_QT in library PEXTCD2 for example


### 2012.01.29 powerEXT Core 4.7: ###

**new subprocedure:**

- uniqueUUID

Misc. minor improvements in xmlReader

### 2011.11.27 powerEXT Core 4.6: ###

**new subprocedures that handles special UTF-8 characters in EBCDIC:**

- encodeUTF8unit
- hexUTF8unit
- decimalUTF8unit
- replaceUTF8unit
- convertUTF8unit

For more information visit:
http://powerext.org/powerforum/showthread.php?t=1683

### 2011.11.15 powerEXT Core 4.5: ###

**new subprocedures:**

http://powerext.org/powerforum/showthread.php?t=1682



### 2011.09.30 powerEXT Core 4.4: ###

**new subprocedures**

**chgExtVar - check if a variable is in a input string from the browser**

**convCase - converts a string to eiter upper or lower case**

**new XML Tools**

**PXXMLXMLCM - decompresses compressed XML**

**PXXMLRPGCM - creates powerEXT RPGLE code based on an existing XML document**

**Minor bug in xmlReader() corrected**


### 2011.08.24 powerEXT Core 4.3: ###

**Fix in CGIDEV2 about lost storage addresses**

**Minor Fix in CSV to XML converter**


### 2011.07.15 powerEXT Core 4.2: ###

**New Apache test environment included**

**XMLreader - support for `<![CDATA[ ... ]]>` sections**

**XMLreader - support for non-encoded special char in CDATA section**

**Fix in CSV to XML converter**


### 2011.03.10 powerEXT Core 4.1: ###

New subprocedures

convCCSdcbs()
cvtHex2Char()
cvtChar2Hex()

### 2010.10.19 powerEXT Core 4.0: ###

### **IMPORTANT! powerEXT Core 4.x is not object compatible with earlier Core versions due to change of max varying field length from 32767 to 65535, existing programs that uses Core has to be recompiled after installation** ###


All variable length fields changed from 32767 to 65535.

New subprocedures

csvDelimiter()
convCCS()
storeFromStmf()
storeToStmf()
storeToField()

### 2010.06.23 powerEXT Core 3.1: ###
enhances the store methods to handle EBCDIC x'15' from templates as CRLF EBCDIC x'0d25' in output to stmf's.
<p>
new method encodeRPG used for database based RPGLE program generators (handling of speciel encoding of ')<br>
<br>
<br>
<br>
<h3>2010.05.19 powerEXT Core 3.0:</h3>
Version 3.0 introduces <b>Dynamic Memory Stores</b> and a number of methods to support them<br>
<ul><li>storeNew() - provides a handle to a dynamic memory store<br>
</li><li>storeInz() - initializes a store<br>
</li><li>storeAppend() - appends data by %addr and %size to a store<br>
</li><li>storeAppendText() - appends static text or textfields to a store<br>
</li><li>storeAddr() - returns the current %addr of a store<br>
</li><li>storeSize() - returns the current %size of a store<br>
</li><li>storeFree() - frees up memory allocated to a store<br>
up to 1000 concurrent memory stores can be active<p>
store 0 shares memory with the HTTP Response Object/Output buffer<br>
<p>
getExtInputRaw() - reads raw HTTP POST input into a store<p>
xmlToStmf() - writes any memory to an IFS file<p>
xmlInXPath() - searches for element in current XPath<p>
echoCgiDev2() - writes CGIDEV2 compatible templates<p>
Example programs added<p></li></ul>

<h3>2010.05.14 powerEXT Core 2.0:</h3>
Version 2.0 completes the methods for writing and reading of different data types (XML, JSON, CSV and HTML)<p>
<code>Creates__________ Reads</code><p>
<code>Output in________ Input From_______ Read method</code><p>
<code>XML______________ XML______________ XMLreader</code><p>
<code>JSON_____________ JSONtoXML________ XMLreader</code><p>
<code>CSV______________ CSVtoXML_________ XMLreader</code><p>
<code>HTML_____________ HTML is XML______ XMLreader</code><p>
<p>
<code>Writes To________ Reads From</code><p>
<code>MEMORY___________ MEMORY</code><p>
<code>IFS______________ IFS</code><p>
<code>BROWSER__________ BROWSER</code><p>
<p>
<h3>Version 1.x</h3>
2010.03.06 Core: A minor change in the installation procedure of powerEXT Core (removing output(none) in the API generation)<p>
2010.03.21 Core 1.2: Support for reading XML files stored in the IFS added<p>
2010.03.22 Framework: Download updated with Core Version 1.2<p>
2010.04.05 Core 1.3: Support added for serving binary files from the IFS echoBinToClient()<p>
2010.04.05 Core 1.3: UTF-8/16 support to xmlFromStmf added<p>
2010.04.21 Core 1.4: More XML support subprocedures added: xmlGetDepth, xmlGetXPath, xmlAddrOuter, xmlSizeOuter, xmlAddrInner, xmlSizeInner, xmlReaderCase<p>
2010.05.03 Core 1.5: XML Support for reading HTML style attributes (att="123", att='123', att=123). XML DOM Support for HTML <code>&lt;SCRIPT&gt;</code> and <code>&lt;STYLE&gt;</code> sections<p>
<p>

