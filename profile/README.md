# PHP Alchemist

## Purpose

The idea behind PHP Alchemist is to put libraries, products, and 
knowledge back into the PHP community. Some libraries started 
as thought-experiments and stayed that way.  Meanwhile, others turned
into libraries to put out there.


## Contributions

PHP Alchemist is very open to contributions to our projects. 
Please note that we ask that you adhear to our [coding standard](#coding-standards). 
As a disclaimer, please note that most of our projects have an intended direction
and ones that do not follow that vision may not be accepted.

# Coding Standards
This document outlines the coding standards for PHP projects, adhering to the Symfony Coding Standards and incorporating
specific configurations from the provided `.editorconfig` file. Users of JetBrains' products will find the editorconfig
to be the most helpful.

## **1. General Code Style**

- **Character Set**: Use UTF-8 encoding for all PHP files.
- **Line Endings**: Use Unix-style line endings (`LF`).
- **Indentation**: Use 4 spaces per indentation level; do not use tabs.
- **Maximum Line Length**: Limit lines to 120 characters.
- **Final Newline**: A single newline is required at the end of the file.
- **Blank Lines**:
    - A single blank line is required before return statements.
    - Do not use more than a single blank line to separate code.
    - A single blank line is required after methods and properties.
    - Namespaces should be surrounded by single blank lines.
    - A single blank line should exist before and after the collection of `use` statements.

## **2. Naming Conventions**

- **Classes**: Use `PascalCase` (e.g., `ClassName`).
- **Methods and Functions**: Use `camelCase` (e.g., `methodName`).
- **Variables**: Use `camelCase` (e.g., `$variableName`).
- **Constants**: Use `UPPER_SNAKE_CASE` (e.g., `CONSTANT_NAME`).
- **Interfaces**: Suffix with `Interface` (e.g., `LoggerInterface`).
- **Abstract Classes**: Prefix with `Abstract` (e.g., `AbstractController`).
- **Traits**: Suffix with `Trait` (e.g., `SingletonTrait`).

## **3. File Naming**

- **Class Files**: Name files after the class they contain, using `PascalCase` (e.g., `UserProfile.php`).
- **Configuration Files**: Use `snake_case` (e.g., `database_config.php`).

## **4. Directory Structure**

- **Interfaces**: Store all interfaces in a `Contract/` folder (e.g., `src/Contract/LoggerInterface.php`).
- **Abstract Classes**: Store all abstract classes in an `Abstract/` folder (e.g., `src/Abstract/AbstractService.php`).
- **Controllers**: Place controllers inside the `Controller/` folder (e.g., `src/Controller/UserController.php`).
- **Services**: Place service classes in a `Service/` folder (e.g., `src/Service/UserService.php`).
- **Entities**: Place entity classes in an `Entity/` folder (e.g., `src/Entity/User.php`).

## **5. PHP Tags**

- Always use `<?php` tag but not the closing tag.
- Do not use short tags like `<?` or `<?=`.

## **6. Control Structures and Braces**

- Use one space after control structure keywords (e.g., `if`, `for`, `while`, `switch`).
- Always use braces `{}` for control structures, even for single-line statements.
- Place the opening brace on the same line as control structures (e.g., conditionals and loops).
- Place the opening brace on a new line for classes and functions.

## **7. Function and Method Calls**

- Do not add a space between the function name and the opening parenthesis.
- Place a single space after each comma in function arguments.

## **8. Return Type Declarations**

- A space is required before and after the `:` in return type declarations (e.g., `function foo() : string {}`).

## **9. Arrays and Multi-Line Declarations**

- Use the short array syntax `[]` instead of `array()`.
- For multiline arrays, place each element on a new line, ending with a trailing comma.
- Align subsequent assignment operations and multi-line function and array declarations on their operators for readability.

## **10. Documentation**

- Use PHPDoc blocks to document all classes, methods, and functions.
- Start the comment with `/**` and end with `*/`.
- Use `@param` and `@return` annotations to describe method parameters and return values.

## **11. Architectural Standards**

- **Autoloading**: Follow PSR-4 autoloading standards.
- **Namespaces**: Define namespaces for all classes, matching the directory structure.
- **Dependency Injection**: Prefer constructor injection for dependencies.
- **Controllers**: Keep controllers thin; delegate business logic to services.
- **Services**: Encapsulate reusable business logic in services.
- **Entities**: Represent database tables as entities, adhering to the Single Responsibility Principle.

## **12. Tools**

- **Psalm**: Use [Psalm](https://psalm.dev/) for static analysis to catch type errors and potential issues.
- **PHPStan**: Use [PHPStan](https://phpstan.org/) to enforce strict type checking and improve code quality.
- **PHP Magic Number Detector (phpmnd)**: Use [phpmnd](https://github.com/povils/phpmnd) to detect hardcoded numeric values that should be replaced with constants.
- **PHP CS Fixer**: Use [PHP CS Fixer](https://cs.symfony.com/) to automatically enforce coding standards.