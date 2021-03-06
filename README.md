gedcomparser
============

GEDCOM parser, convert an GEDCOM raw data file into XML
-------------------------------------------------------

Usage (How to run)
------------------
* java -jar gedcomparser-1.0.jar input_file output_file
* e.g. java -jar gedcomparser-1.0.jar input/input_1.txt output_1.txt
  
Maven Usage (How to change source code)
---------------------------------------
* to compile
    mvn compile
* to test
    mvn test
* to make a jar file
    mvn package

Design and Development/Test
-------
* Spock/Groovy is used to writing tests, this make them more readable and intuitive
* StAX, a streaming API for XML, is used for writing target XML document. Streaming is very fast but often exhibits some limitations like forward-only.

Notes
-------
* If source file contains lines with invalid format, they will be reported and parsing will stop there.
* By default, 'mvn package' produces a jar file in the target folder
* This project has been tested in Maven 3.1.1, JDK 1.7, under Linux

Thoughts
---------
* To improve performance, we could introduce parallelism into this program by
1. Having separate threads to parse different sections of the raw data file
2. Having separate threads to work on different stages of parsing: Line parsing, converting parsed lines into XML elements, writing to XML target file, etc.
3. Combine the above two approaches
