Download Link: https://assignmentchef.com/product/solved-cpe211-project-12-simple-calculator
<br>



<h2>&lt;Starting Project 12&gt;</h2>




<ul>

 <li>Open a terminal window and move (cd) into the <strong>Project_12 </strong>directory created in the</li>

</ul>




<ul>

 <li>Download all needed files from Canvas into this directory. Once you have finished with the program and it compiles without syntax errors, run the executable and verify that the output for your program matches the output from the provided solution executable</li>

</ul>




<strong><em> </em></strong>

<strong><em> </em></strong>

<strong><em><u>NOTE: Output of your program is to match the output of the sample solution.</u></em></strong><strong><em>  <u>This match includes all information written to the terminal by the program</u></em></strong><strong> <u>&lt;Project 12 Description&gt;</u></strong>




You will write a program that performs the following tasks for a simple mathematical calculator:




<ul>

 <li>Open a user-specified file for input. Prompt for the name of the file, read it into a string variable, echo print it to the terminal and then open it.  If the file is not opened, enter into a loop that prints out an error message, resets the input file stream variable <strong>(see the hints section),</strong> obtains a new file name and tries to open the new file.  The loop continues until the user successfully enters a valid file name or presses ctrl-c to exit</li>

 <li>If the input file is empty, your program should indicate that the input file was empty as shown by the sample solution – note that an empty input file message only is printed out for an empty input file. <strong>(see the hints section on how to perform this test)</strong></li>

</ul>




<ul>

 <li>The input file contains several lines of information for processing. There are two types of lines: one for <strong>Math</strong> calculations and one for <strong>Trig</strong>

  <ol>

   <li><strong>Math calculation line</strong>: <strong>Math</strong>,  Operator, Value1,  Value2

    <ol>

     <li>Operator is +, -, *, / or % (for add, subtract, multiply, divide or modulo)</li>

     <li>Value1 is the first (left) operand for the operator</li>

    </ol></li>

  </ol></li>

</ul>

<ul>

 <li>Value2 is the second(right) operand for the operator</li>

</ul>

<ol>

 <li><strong>Trig calculation line</strong>: <strong>Trig</strong>, Operation, Degrees or Radians indicator, Angle Value

  <ol>

   <li>Operation is s, c or t (for sine, cosine or tangent)</li>

   <li>Degrees or Radians indicator is d or r</li>

  </ol></li>

</ol>

<ul>

 <li>Angle Value Is the angle in the same units provided by the Degrees or Radians indicator</li>

</ul>

<ol start="3">

 <li><strong>For Trig calculations use 3.14159265 for the value of pi. </strong></li>

 <li><strong>Remember that the trig functions expect the angle in radians not degrees </strong></li>

</ol>

<ol>

 <li>Look at the provided input files for further understanding of the expected input.</li>

</ol>




<ul>

 <li>All values are <strong>double</strong> values except for the values used with the modulo operation which requires both operands be integers.</li>

 <li>Possible input file errors are:

  <ol>

   <li>Invalid calculation type – calculation type is not <strong>Math</strong> or <strong>Trig</strong>.</li>

  </ol></li>

</ul>

<table width="217">

 <tbody>

  <tr>

   <td width="217">Two different error messages</td>

  </tr>

 </tbody>

</table>

<ol>

 <li>Invalid operator for Math</li>

 <li>Invalid operation for Trig</li>

</ol>




<ul>

 <li>Output formatting uses the default output configuration ç (7) Output lines look like the following:

  <ol>

   <li>Add: 4 + 6 = 10</li>

   <li>sin(degrees): sin(45) = 0.707107</li>

   <li>Identifiers for output for <strong>Math</strong> calculations are: Add, Sub, Mul, Div, Mod</li>

   <li>Identifiers for output for <strong>Trig</strong> calculations are: sin, cos, tan</li>

  </ol></li>

</ul>




<ul>

 <li>Run the sample solution for the provided input file to see the format of the output</li>

 <li><strong>All output is to the terminal. Output of your program is to match that of the sample solution </strong></li>

</ul>




<ul>

 <li>Functions can be used in this program, although it is not a requirement.</li>

 <li>This program can easily be completed using loops and if statements (or switch statement)</li>

</ul>




<strong> </strong>

<h2>&lt;Project 12 C++ Hints&gt;</h2>




<ol>

 <li>Resetting the input stream variable: In Dev C++ and g++, the clear function must be used on a file stream that is repeatedly reopened in a loop. Therefore use the following statement in your while loop that executes until a valid filename is entered:</li>

</ol>




<strong>Input_file_stream_var.clear(); </strong>

<strong> </strong>

Where <strong>Input_file_stream_var</strong> is the name of your input file stream variable




<ol start="2">

 <li>Testing for an empty input file is performed by using a priming read, and then testing the status of the file stream after the priming read – before the while loop is entered. In this case, if the file stream is in the fail state (or the eof bit is true) after the priming read, print out an appropriate message and terminate the program.  Otherwise proceed to the loop to process and read the rest of the input file</li>

</ol>




<ol start="3">

 <li>Use a while loop to read and process all information in the input file (or a do-while loop can be used)</li>

</ol>




<ol start="4">

 <li>Each line in the input file will contain a calculation type, a type of operation identifier and two values to use with that operation. <strong>All values are separated by spaces.  Use extraction for all reads</strong>

  <ol>

   <li>Calculation type will be a single word of: <strong>Math or Trig</strong></li>

   <li>Operator will be a single character (+, -, *, /, %, s, c or t)</li>

   <li>For Math, the left operand is the first value and the right operand is the second value</li>

   <li><strong>For Math, all operands are of data double except for the mod operator which requires both operands be integers. </strong></li>

   <li>For Trig, the first value is <strong>d or r</strong> indicating degrees or radians</li>

   <li>For Trig, the second value is the angle in degrees or radians</li>

  </ol></li>

</ol>




<ol start="5">

 <li><strong>All numbers are of data type double except for the values used with the modulo operator </strong></li>

</ol>




<ol start="6">

 <li><strong>Output is to use the default format configuration</strong>, and all output is to the terminal</li>

</ol>




<ol start="7">

 <li>Output is required to match the output provided by the sample solution</li>

</ol>




<ol start="8">

 <li>Use a single loop with a priming read to read the information from the input file. Each loop iteration processes one line from the input file and outputs the results of the calculation.</li>

</ol>




<ol start="9">

 <li>In the loop use nested if-then-else-if statements to process the information in the input file. Or, use nested switch statements. Or, use a combination of switch and if-then-else-if statements.</li>

</ol>




<ol start="10">

 <li>Error messages for invalid input file and empty input file have 47 characters on the top and bottom lines.</li>

</ol>


