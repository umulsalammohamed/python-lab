partA
The `mkdir` command creates new directories, while `cd` moves into a directory. The `touch` command creates empty files such as `main.py`, `utils.py`, and `config.py`. The `echo` command with output redirection (`>`) writes the required text into `README.md`. The recursive directory listing command displays all the folders and files inside `python_lab`, including their structure and nesting.

Separating the project into `src`, `tests`, and `docs` is good practice because each folder has a specific purpose. The `src` folder contains the program's source code, the `tests` folder contains files used to test the program, and the `docs` folder contains documentation. This organization keeps the project neat, makes files easier to find, and makes the project easier to maintain as it grows.

PART C
My code
Utils.py
def square(n):
    return n ** 2


def is_even(n):
    return n % 2 == 0


def celsius_to_fahrenheit(c):
    return (c * 9 / 5) + 32
    main.py
    from utils import square, is_even, celsius_to_fahrenheit

number = float(input("Enter a number: "))

print("Square:", square(number))

if is_even(number):
    print("The number is even.")
else:
    print("The number is odd.")

print("Fahrenheit:", celsius_to_fahrenheit(number))


Python 3.13.7
PS C:\Users\HP\Desktop\python_lab> py src/main.py
Enter a number: 2
Square: 4.0
The number is even.
Fahrenheit: 35.6
PS C:\Users\HP\Desktop\python_lab> py src/main.py
Enter a number: 5
Square: 25.0
The number is odd.
Fahrenheit: 41.0
PS C:\Users\HP\Desktop\python_lab> py src/main.py
Enter a number: 4
Square: 16.0
The number is even.
Fahrenheit: 39.2

How Python imports connect main.py to utils.py:

Python's import system allows main.py to use functions defined in utils.py. The statement from utils import square, is_even, celsius_to_fahrenheit imports the three functions from the utils module into main.py. This allows the main program to use the functions without rewriting their code.

Testing:

I tested the program with three different input values: 2, 5, and 4. For each input, the program correctly calculated the square, determined whether the number was even or odd, and converted the Celsius value to Fahrenheit.