# My Calculator Project

This is a simple calculator I made using Java. I tried to apply what we learned about OOP and Clean Code by dividing the project into 3 different classes to make the code organized.

## What it can do:
- It does the 4 main operations: `+`, `-`, `*`, `/`.
- It works with normal numbers and decimal numbers (like 2.5 or 3.14).
- It handles errors: if you type letters by mistake, it won't crash, it will ask you to enter a valid number again.
- It protects against division by zero (shows an error message instead of crashing).

## Project Structure (UML)
This is how my classes interact with each other:

```mermaid
classDiagram
    class Main {
        +main(args: String[]) void
    }
    class Calculator {
        +add(num1: double, num2: double) double
        +subtract(num1: double, num2: double) double
        +multiply(num1: double, num2: double) double
        +divide(num1: double, num2: double) double
    }
    class InputValidator {
        -scanner: Scanner
        +getValidNumber(prompt: String) double
        +getValidOperator() char
    }

    Main --> Calculator : Uses
    Main --> InputValidator : Uses
