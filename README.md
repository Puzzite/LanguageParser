# Language Parser

This repository contains a C++ implementation of a lexer and recursive descent parser for a simple structured programming language. The system tokenizes input source code, checks for syntax correctness, and prints the parsing process.

## Features

- Tokenizes source code into identifiers, numbers, reserved words, and symbols  
- Validates grammar using recursive descent parsing  
- Reports lexical and syntactic errors with line numbers  
- Enforces rules for variable declaration and usage with a symbol table  
- Supports key language constructs like:
  - Variable declarations  
  - Assignments  
  - If-else conditionals  
  - While loops  
  - Input/output  
  - Function calls  

## Supported Grammar Highlights

- **Keywords**: `program`, `begin`, `end`, `if`, `then`, `else`, `while`, `loop`, `input`, `output`, `int`, `float`, `double`, `call`  
- **Symbols**: `:=`, `<>`, `=`, `<`, `>`, `+`, `-`, `*`, `/`, `(`, `)`, `,`, `:`, `;`  
- **Identifiers**: start with a letter or underscore, followed by alphanumerics or underscores  
- **Numbers**: up to 10 digits, optionally with a decimal point  

## Example Code

program
x, y : int;
begin
  input x;
  if (x < 10) then
    y := x + 1;
  else
    y := x - 1;
  end if;
  output y;
end;

## Example Output
'''
PROGRAM  
DECL_SEC  
DECL  
ID_LIST  
ID_LIST  
STMT_SEC  
STMT  
INPUT  
ID_LIST  
STMT  
IF_STMT  
COMP  
OPERAND  
OPERAND  
...

## Error Reporting
'''
[Lexer Error] Line 3: Illegal symbol: @  
[Parse Error] Line 5: Expected ';', got 'end'
'''

## File Structure

- main.cpp – contains the full lexer and parser implementation
- README.md – project documentation
- example.hawk – sample source code (optional)



