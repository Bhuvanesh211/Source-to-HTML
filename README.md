# Source to HTML

## Project Overview
The **Source to HTML** project aims to parse C source code and generate an equivalent HTML file that can be viewed in a web browser. The HTML file displays the source code with syntax highlighting, using predefined colors for reserved keywords, preprocessor directives, numerical constants, strings, and ASCII characters.

## Importance of Syntax Highlighting
Syntax highlighting is a crucial feature in modern text editors and Integrated Development Environments (IDEs). It displays source code in various colors and fonts, improving readability and allowing developers to detect syntax errors early. This feature is widely implemented in popular IDEs such as Visual Studio Code, Sublime Text, and Notepad++, and is essential for writing clean, readable code. It also enhances understanding of code snippets in manuals and websites.

Syntax highlighting benefits include:
- **Improved readability**: Highlighting keywords, comments, and strings in different colors makes it easier to follow the structure of the code.
- **Error detection**: Different colors for string literals, preprocessor directives, and matching braces help in spotting errors like missing delimiters or unmatched braces.
- **Code navigation**: Programmers can easily distinguish between comments, code, and preprocessor directives, enhancing the debugging and development process.

## Project Features
- Accepts a C source file as input.
- Provides an option to specify the output HTML file name.
- Optionally adds line numbers to the output HTML file.
- Syntax highlighting for:
  - Reserved keywords
  - Preprocessor directives
  - Numerical constants
  - Strings
  - ASCII characters
  - Comments
- Uses a state-event parser engine for processing the input source file.

### State-Event Parser Engine
The parser engine operates using a **state-event** approach with the following states:
1. **Idle State**: The default state at program start-up.
2. **Word Identification**: Transitions into this state when a keyword, identifier, or constant is detected.
3. **Comment Handling**: Handles both single-line (`//`) and multi-line (`/* */`) comments.
4. **Preprocessor Handling**: Detects and processes preprocessor directives (`#include`, `#define`, etc.).
5. **String Handling**: Recognizes and highlights string literals.
6. **Number Handling**: Identifies numeric constants.

The transitions between states are triggered by the following events:
- Detection of a keyword, comment, string, or preprocessor directive.
- End of a keyword, comment, or string literal.
- End of file.

After processing the source code, the application generates an HTML file with syntax highlighting based on the states.

## Future Enhancements
- **Error Handling**: Future versions of the project may include error handling to detect and report syntax errors.
- **Support for Multiple Languages**: The parser can be extended to support other programming languages like Python, Java, etc.
  
## Usage
1. **Input**: Provide a C source file to the application.
2. **Output**: The application generates an HTML file with syntax-highlighted code.
3. **Options**:
   - Specify an output file name.
   - Add line numbers to the output file.

## Prerequisites
- C programming knowledge is required to understand and contribute to this project.
- Basic understanding of HTML and web browsers.

By implementing this project, you will strengthen your understanding of C programming, as well as gain insight into syntax highlighting and file parsing techniques.

 ## Installation

1. Clone the repository or download the project files.
2. Open a terminal and navigate to the project directory.
3. Compile the project using the following command:

   ```
   gcc *.c 

   ./a.exe <source file name> <html file you name>
