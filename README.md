Frequently in life you'll need to convert from one unit to another: feet to meters, hours to seconds, degrees to radians, etc. Usually, the conversion simply involves a simple conversion factor, meaning that you multiply or divide by a real number.
In this assignment, you'll input a length as some number of feet and inches, and convert that to a number of other length values. Finally, you'll print out the results in a nice format. See the examples below.

How to ask for user input: In your program you'll need to prompt the user to enter the number of feet and the number of inches to convert. The input function is not covered until slideset 3, but it's pretty easy. To get the values of the feet and inches into two variables inputFeet and inputInches, you'll include the following two statements:

inputFeet = int( input("Enter number of feet: ") )
inputInches = int( input("Enter number of inches: ") )
When each statement is executed, it prints the prompt (e.g., "Enter number of feet: ") on the screen, and waits for the user to enter a number. After the user types in a number, say 10000, this number is read by the program as a string, say "10000". Then the function int() will convert that string into the corresponding integer value which will be stored in the variable inputFeet. The second statement will do an analogous thing for variable inputInches. From there you're good to go. Notice we didn't name those variables feet and inches because we'll use those for some other values.
You can assume that the year entered is a positive integer. (It would be easy to convert this program to accept floats; that would only require changing one word in the input statements above. Can you guess what you'd change?) Your program doesn't have to check that and doesn't have to work if the user enters a bad value. We won't test your program on illegal values.

Doing the conversions: After you've input those two values, you'll then do the conversions indicated in the following table. We suggest you do them in this order.

inches	inputFeet times 12, plus inputInches
feet	inches divided by 12
yards	feet divided by 3
miles	feet divided by 5280
meters	feet times 0.3048
centimeters	meters times 100
millimeters	centimeters times 10
kilometers	meters divided by 1000
You will then print out a nice report of the conversion following the sample output below. There is a single space after each colon and two spaces before the items that are indented. Leave blank lines where shown. You don't need to round any values. You should follow this model exactly. (Long decimal fractions may vary slightly; that's OK.)

Note that your program must work for arbitrary legal input values, not merely the values illustrated below.

> python ConvertUnits.py
Enter number of feet: 5
Enter number of inches: 6

5 feet and 6 inches equals:

English Units
  feet: 5.5
  inches: 66
  yards: 1.8333333333333333
  miles: 0.0010416666666666667 

Metric Units
  meters: 1.6764000000000001
  centimeters: 167.64000000000001
  millimeters: 1676.4
  kilometers: 0.0016764000000000002

> python ConvertUnits.py
Enter number of feet: 20000
Enter number of inches: 0

20000 feet and 0 inches equals:

English Units
  feet: 20000.0
  inches: 240000
  yards: 6666.666666666667
  miles: 3.787878787878788

Metric Units
  meters: 6096.0
  centimeters: 609600.0
  millimeters: 6096000.0
  kilometers: 6.096

>
Turning in the Assignment:
The program should be in a file named ConvertUnits.py. Submit the file via Canvas before the deadline shown at the top of this page. Submit it to the assignment hw2 under the assignments sections by uploading your python file.
Your file must compile and run before submission. It must also contain a header with the following format:

# File: ConvertUnits.py
# Student: 
# UT EID:
# Course Name: CS303E
# 
# Date:
# Description of Program: 
If you submit multiple times to Canvas, it will rename your file name to something like ConvertUnits-1.py, ConvertUnits-2.py, etc. Don't worry about that; we'll grade the latest version.


Programming Tips:
Many assignments this semester will include this section called Programming Tips. In general, these are not hard requirements about this specific assignment; they are suggestions to help you become better programmers. So read and apply them!
Naming Variables: It's typically considered lousy programming practice to use single letter variable names. It's almost always much better to use descriptive names. Obvious variable names for this assignment are inches, feet, miles, etc.

Also, it's always a good idea to comment any part of your code that would be unclear to someone reading it later. The individual steps of this algorithm are individually pretty clear, especially if you use descriptive variable names, so it's not really necessary to comment them. But there needs to be an overall comment that says what the program accomplishes. The question to ask yourself is: If someone besides me looks at this code, how hard will they have to work to understand what's going on?

Output format: As explained in slide set 1, there are multiple ways to run your program. If you run in interactive mode (in the Python loop), the system will automatically display the result of every command (unless the result is None). If that result is a string, it will display with string quotes ('answer'). If you're running the program in batch mode (from the command line, as e.g. python myProgram.py) or explicitly print a string, it won't appear with string quotes. If you run your program in batch mode the only things you'll see displayed are the things you explicitly print; it won't display the results of individual commands. The following is in interactive mode:

>>> string = "my string"
>>> string
'my string'
>>> print(string)
my string
>>> 
If your string output doesn't match what's shown in the assignment sample output because of the presence or absence of string quotes, that may be the reason. Usually, it's not an issue to worry about.
But remember, you must turn in a file that contains the code to do this computation. So it's not adequate to just run the steps in interactive mode. You can do that while you're debugging the steps; but you need a complete program stored in a file for your submission.
