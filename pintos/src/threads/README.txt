Benjamin Cooper
Project 0
README.txt

To incorporate a new test script into pintos, the following steps were taken:

	1. A copy of the "alarm-multiple" file was made, renamed to "alarm-mega", and the
	   parameter "7" was changed to "70" to increase the number of alarm iterations.

	2. Using the "grep -r alarm-multiple *" and "grep -r alarm_multiple *" commands,
	   all the files that referenced the "alarm-multiple" script were located. Some of
	   these include:

		> tests.c - Which defines the basic operation of a test and contains a
		  structure that links each test to its associated code file.

		> tests.h - The header for tests.c

		> alarm-wait.c - Contains the thread waiting code that the alarm tests
		  rely on.

		> Make.tests - The makefile contains instructions on how to build the
		  program.

	3. By copying the references to "alarm-multiple" in these files, new references
	   to "alarm-mega" were added.

	4. Once pintos was cleaned and rebuilt, the "alarm-mega" script could be executed
	   just like any other test script.
