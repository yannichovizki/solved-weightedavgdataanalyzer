Download Link: https://assignmentchef.com/product/solved-weightedavgdataanalyzer
<br>
make a new Java application called “WeightedAvgDataAnalyzer” (without the quotation marks), that modifies the DataAnalyzer.java in Horstmann Section 7.5, pp. 350-351 according to the specifications below.

The input file should be called ‘data.txt’ and should be created according to the highlighted instructions below. Note that even though you know the name of the input file, you should not hard-code this name into your program. Instead, <em>prompt the user for the name of the input file (which should be called ‘data.txt’)</em>.

The input file should contain (in order): the weight (a number greater than zero and less than or equal to 1), the number, n, of lowest numbers to drop, and the numbers to be averaged after dropping the lowest n values.

<em>You should also prompt the user for the name of the output file</em>, and then print your results to an output file with the name that the user specified.

Your program should allow the user to re-enter the input file name if one or more of the exceptions in the catch clauses are caught.

<ul>

 <li></li>

 <li>Your methods for getting data and printing results should each throw a FileNotFoundException which should be caught in the main method.</li>

 <li>Use try-with-resources statements ( https://docs.oracle.com/javase/tutorial/essential/exceptions/tryResourceClose.html )in your methods for getting and printing the data, and so avoid the need to explicitly close certain resources.</li>

 <li>In your readData method, use hasNextDouble to check ahead of time whether there’s a double in the data. That way when you try to get the nextDouble, your code won’t throw a NoSuchElementException.</li>

 <li>You can use a writeFile method that does all the work for your output (i.e., the writeFile method does not call a writeData method the way that Horstmann’s readFile method calls a readData method).</li>

 <li>Use a try-with-resources statement in your writeFile method when creating a new PrintWriter.</li>

</ul>

The inputValues come from a single line in a text file (data.txt) such as the following:

0.5 3 10 70 90 80 20

The output in the output file must give the weighted average, the data and weight that were used to calculate the weighted average, and the number of values dropped before the weighted average was calculated.

Your output should look very much like the following:

“The weighted average of the numbers is 42.5, when using the data 10.0, 70.0, 90.0, 80.0, 20.0, where 0.5 is the weight used, and the average is computed after dropping the

lowest 3 values.”

CREATING THE INPUT FILE:

To create the input file, while in NetBeans with your project open, first click to highlight the top-level folder of your project (on the Projects tab, in the upper left), which should be called WeightedAvgDataAnalyzer.

Then from the File menu do:

File-&gt;New File

Keep the Project name at the top; keep Filter blank

Categories choose Other (at the bottom of the categories list)

File Types choose Empty File (at the bottom of the files list)

Next&gt;

FileName: data.txt

Folder: this should be blank; if it’s not, delete whatever’s there

Finish

In the empty file data.txt that you just created, add a single line of data

like that shown in the example above, where the weight is a double

(greater than 0.0 and less than or equal to 1.0)

and the other numbers are the number, n, of lowest values to drop and

then the numbers to be averaged after dropping the lowest n values.