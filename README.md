# TWS is a Translator Writing System.
To install the TWS:

1. Edit pgen/Makefile.  All but one of lines 12-16 should be
   commented.  For Linux machines, uncomment line 12.   For CISE Sun
   machines, uncomment line 15.

2. While in 'tws' directory, simply type 'make'.

About Tiny:
Tiny is a language implemented over TWS. Tiny runs on a stack based TWS virutal machine.
The Tiny folder contains four main files:
CodeGenerator.c: This is the source file for the code generator.

Constrainer.c:  This  is  the source file for the contextual constrainer.

lex.tiny, parse.tiny in the parser folder inside the tiny folder. These are lexical and parsing specifications  for  Tiny. parse.tiny describes Tiny's syntax.

tc:   This  is  the Tiny Compiler/Interpreter.  It's nothing more than a shell script, that invokes  the  scanner/parser,
then  the  constrainer, then the code generator, and finally the interpreter.  As these as executed, their effect  is  as
follows:

1)   The  parser  produces a file called _TREE, in your current directory (the 'tiny' directory).

2)   The constrainer reads in the _TREE file, traverses  the tree,  adds  constraining information to it, and writes
     it back out.

3)   The code generator reads in the tree, traverses  it  to generate code, and produces a file called _CODE in your
     current directory. It also updates the new (slightly) modified tree.

4)   The  interpreter reads in the _CODE file, and simulates the execution of the program in it.

Features of Tiny:
 * Types: integer
          char
          bool
          enum
          const
 * for statement
 * if case
 * repeat statement
 * case statement
 * loop statement with exit statement
 * swap statement A :=: B
 * succ, pred and ord for integers and characters and enumerated types
 * read statement
 * output statement
 * Functions and Procedures
* commenting using curly braces '{' '}'
