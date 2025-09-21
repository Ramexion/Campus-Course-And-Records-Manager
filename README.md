Project Overview & How to Run

Campus Course & Records Manager (CCRM) is a modular, console-based Java SE application for managing students, courses, enrollment, grades, transcripts, and file utilities (CSV/JSON import/export, archiving). Designed for demonstration of OOP principles, modern I/O (NIO.2), Streams, Date/Time API, exception handling, interfaces, design patterns (Singleton, Builder), enums, lambdas, and recursion.[7][1]

- JDK Version: 17 or above recommended (tested with JDK 17)
- Run Instructions:  
  1. Compile:  
      `javac -d bin src/com/ccrm/*.java`
  2. Run:  
      `java -cp bin com.ccrm.Main`
- Commands: Application prompts for inputs (menus/options); see sample runs in `/docs/demo.txt`
- Assertions: Enable with  
      `java -ea -cp bin com.ccrm.Main`  
      For specific class/package:  
      `java -ea:com.ccrm.model.Student -cp bin com.ccrm.Main`

 Evolution of Java

- 1991–1995: Java prototype ("Oak") developed by Sun.
- 1996–1999: Java 1.0/1.2: Applets, AWT, Swing, Collections Framework.
- 2000–2004: J2EE emergence; EJB, Servlets, JDBC APIs.
- 2004: Java 5: Generics, Annotations, Enhanced for-loop, Autoboxing.
- 2010: Oracle acquires Java; Java 7: Try-with-resources, Fork/Join.
- 2014: Java 8: Lambda, Stream API, Optional, Date/Time API.
- 2017+: Modules (JPMS), local-variable type inference, records, pattern matching, continued functional expansion.

 Java ME vs SE vs EE Comparison

| Edition | Target Use              | APIs & Features                                              | Scope                                 |
|---------|-------------------------|--------------------------------------------------------------|---------------------------------------|
| Java ME | Embedded/mobile devices | Lightweight, device-specific libraries                       | Resource-restricted, small footprint  |
| Java SE | Desktop/server          | Core language, standard libraries (java.util, java.io, etc.) | General-purpose, standalone apps      |
| Java EE | Enterprise/web          | Built on SE; adds Servlets, EJB, JMS, JPA, etc.              | Distributed, multi-user, scalable apps|

- Jakarta EE is the successor to Java EE under Eclipse Foundation.
  

JDK, JRE, JVM Explanation

- JDK (Java Development Kit):  Full developer suite: compiler (`javac`), debugger, tools, and the JRE. Required for code development.
- JRE (Java Runtime Environment):  JVM plus runtime libraries for running (not compiling) Java apps; end-users may only need JRE.
- JVM (Java Virtual Machine):  Executes Java bytecode, ensuring platform independence. Interprets/compiles (`Just-In-Time`), loads, links, and initializes code.

Windows Install Steps (with Screenshots)

Windows Java JDK Installation:
1. Download JDK from Oracle/AdoptOpenJDK.
2. Run the installer, follow prompts.
3. Set `JAVA_HOME` and update `PATH`.
4. Verify:  `javac -version`.
   
   <img width="566" height="474" alt="Screenshot 2025-09-21 153411" src="https://github.com/user-attachments/assets/8b1f1880-39fb-418d-8de2-ce1b437e38c8" />


Mapping Table

| Syllabus Topic       | File/Class                                                              | Method/Section / Usage                                 |
| ---------------------| ------------------------------------------------------------------------| ------------------------------------------------------ |
|  Encapsulation       | `Student.java`, `Course.java`, `Semester.java`, `Person.java`           | private fields with setters/getters                    |
|  Inheritance         | `Person.java` (abstract), `Student.java`, `Enrollment.java`             | `Student` extends `Person`, relationships              |
|  Abstraction         | `Person.java` (abstract), `Course.java` (abstract-like structure)       | abstract methods, base class definitions               |
|  Polymorphism        | `CourseService.java`, `StudentService.java`                             | method overriding (e.g., handling objects differently) |
|  Exception Handling  | `ImportExportService.java`, `BackupService.java`, `StudentService.java` | `try/catch`, input validation, custom handling         |
|  NIO.2/Streams       | `ImportExportService.java`, `BackupService.java`                        | file read/write with streams, CSV import/export        |
|  Date/Time API       | `Semester.java`                                                         | `LocalDate`, date calculations                         |
|  Interface           | (Likely implemented in `Enrollment.java` or service layer)              | contracts for enrollment operations                    |
|  Abstract Class      | `Person.java`                                                           | abstract methods, superclass for `Student`             |
|  Nested Classes      | `Validator.java` (possible inner helper class)                          | static/inner utility definitions                       |
|  Enums               | `Grade.java`                                                            | letter grades + GPA mapping                            |
|  Lambda/Streams      | `CourseService.java`, `StudentService.java`                             | filtering courses/students with streams                |
|  Recursion           | `BackupService.java`                                                    | recursive directory backup/export                      |
|  Singleton Pattern   | `AppConfig.java`                                                        | `getInstance()` or configuration loading               |
|  Builder Pattern     | (Not explicitly present — but may be in `Student.java` or similar)      | object construction via helper methods                 |

 Notes on Assertions & Sample Commands

-  Assertions:  For internal program logic validation; disabled by default.
-  Enable assertions for all classes:   
  `java -ea -cp bin com.ccrm.Main`
-  Enable for package/class:   
  `java -ea:com.ccrm.model.Student -cp bin com.ccrm.Main`
-  Disable assertions:   
  `java -da -cp bin com.ccrm.Main`
-  Enable in system classes:   
  `java -esa -cp bin com.ccrm.Main`

