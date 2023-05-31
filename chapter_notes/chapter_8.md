```
program       -> declaration* EOF;

declaration   -> varDecl | statement ;

varDecl       -> "var" IDENTIFIER ( "=" expression)? ";";

statement     -> exprStmt | printStmt;

exprStmt      -> expression ";";

printStmt     -> "print" expression ";";

primary       -> "true" | "false" | "nil" | 
               | NUMBER | STRING
               | "(" expression ")"
               | IDENTIFIER ;
               
expression    -> assignment ;
assignment    -> IDENTIFIER "=" assignment 
               | equality ;
               
statement     -> exprStmt | printStmt | block;
block         -> "{" declaration* "}";
```