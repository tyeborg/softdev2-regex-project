# Software Development 2: Regex Project

The objective of this project is to write a program that accepts four pieces of information (that are specific from the user): `name`, `date of birth`, `phone number`, `postcode`. Furthermore, the program will tend to ask the users for input until `q` is entered in which all the information that was entered is transferred into a txt file called: `output.txt`.

<img width="1236" alt="Screen Shot 2022-08-26 at 2 09 42 AM" src="https://user-images.githubusercontent.com/96035297/186795391-9024e589-7aea-4ba9-bb0d-4d8980ba3e68.png">

## Installation & Execution
* Clone this repository: `git clone https://github.com/tyeborg/softdev2-regex-project.git`
* Open your terminal, and in the project directory prepare to compile `main.cpp`
  *  Mac OS: `g++ main.cpp -o main`.
  * Windows: `cl main.cpp` followed with `/EHa` as this program attempts to catch an exception that’s raised by something other than a throw.
* Run the program by entering the following: `./main`.

## Additional Functionality
Throughout the process of entering input for the `date of birth`, `phone number`, or `postcode`, users will have the option to skip the providence of input for a given section and proceed to the next prompt. To enable the skip function, the user will have to enter a blank statement after the prompt. 

In the output file, the result will be classified as `(not available)` for the section that was skipped.  This option is excluded for the `name` prompt because the name input distinguishes the upcoming prompt input/information by the name entered by the user.

<img width="1236" alt="program-functionality-01" src="https://user-images.githubusercontent.com/96035297/187001913-ef8d5772-61f2-4ad9-a903-ee4980945bf7.png">

<img width="1235" alt="program-functionality-02" src="https://user-images.githubusercontent.com/96035297/187002506-b8af9fbc-e7e8-4b9e-82ff-d2aeb4865d27.png">

## Appropriate Input Conventions
The program will ensure that the information entered by the users will be in the correct format. If the information is not in the correct format, the program will re-prompt the user until their input is considered valid or if `q` or a blank space is entered. 

* The name must only contain letters and appropriate symbols.
  * For example, the following are acceptable:
    * Mary O’Neil
    * Jean-Luc Picard
  * The following are not acceptable:
    * Kevin4 – contains a number.
    * Pelumi @Roehampton – contains an inappropriate symbol.
   
* The date of birth must use the format `yyyy/mm/dd` – this is to allow quick sorting of dates.
  * For example, the following are acceptable:
    * `2021/01/24`
    * `2021/10/01`
  * The following are not acceptable:
    * `21/10/15` – year must be four digits.
    * `2021/1/16` – month must be two digits.
    * `2021/01/1` – day must be two digits.
    * `2021/13/12` – there is no month greater than 12.
    * `2021/05/32` – there is no day greater than 31.
  * Ensure the date is valid (only the correct number of days for a month are stored, including leap years):
    * `2021/04/31` – is invalid, as April only has 30 days.
    * `2021/02/29` – is invalid, as February only has 29 days in 2021.
    * `2020/02/29` – is valid, as February had 29 days in 2020.
    
* Phone numbers are of the right length, starting with a `0`.
  * For example, the following are acceptable:
    * 01224565501
    * 07777000000
    * 01234 567890 – a space after the 5th digit is valid.
  * The following are not acceptable:
    * 9520111111 – doesn’t start with a `0`.
    * 01234 – isn’t 11 digits long.
    
* Postcodes must follow the correct format for a postcode. That is one to two uppercase letters, one to two numbers, a space, a number, then two uppercase letters.
  * For example, the following are acceptable:
    * SW15 1PU
    * E1 5RF
  * The following are not acceptable:
    * SSS5 9PU – has three letters at the start.
    * S154 9LP – has three numbers before the space.
    
## Languages & Tools
<p float="left">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=cpp,vscode" />
  </a>
</p>
