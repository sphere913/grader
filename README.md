grader-cli version 2.2

CONFIGURATION
=============

There are a couple of things you can configure manually in the script. (unfortunately not much yet..)

Those are:
	* input/output filename format (defaults are 'input.#.txt' and	'output.#.txt')
	* time limit (default is 1 second)
	* the compiler and compiling options for each language (the language is detected based on the file extension)

Note: the '#' character in the input/output filename description will be replaced by 1, 2, 3, ... for each test case. For example 'input.#.txt' means that the input files are: input.1.txt , input.2.txt , ... up to the maximum numbered test case existing in the current directory.

USAGE
=====

Just run the script with one parameter, the source code filename. 

Example:
	./grader.sh test.cpp

	The above command will first compile test.cpp and then run the executable for each test case of the form described by the user.
	After each run (and if the program terminates with exit code 0 within the time limit), the output is judged based on the given correct output files.

IMPORTANT NOTES
===============
	* Your program should read data from stdin and write on stdout. The required input/output redirections are handled automatically by the script.
	* Output is judged based on the given correct output files using the diff tool. As a result, the grading script might give wrong results for problems in which more than one outputs are considered correct by the problem statement.
	* The script, the source code and the test cases should be placed under the same directory.