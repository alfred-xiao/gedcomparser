gedcomparser
============

GEDCOM parser, convert an GEDCOM raw data file into XML

Usage:
  ./run.sh input_file output_file
  OR
  java -jar gedcomparser-1.0.jar input_file output_file

  e.g.
  ./run.sh input/input_1.txt output_1.txt
  
  NOTE: run.sh runs the jar file in the current folder, not in target folder

Maven Usage:
  - to compile
    mvn compile
  - to test
    mvn test
  - to make a jar file
    mvn package

Notes:
  - If source file contains lines with invalid format, they will be reported and parsing will stop there.
  - By default, 'mvn package' produces a jar file in the target folder
  - This project has been tested in Maven 3.1.1, JDK 1.7, under Linux

