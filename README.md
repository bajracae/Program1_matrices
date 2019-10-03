# Program1_matrices
Operating System 1 Program 1

-Notes-
Overview: 
=> write a shell script that calculates basic matrix operations using input from either a file or stdin.
=> input is whole number separated by tabs into a rectangular matrix
=> able to print the
   => dimensions of a matrix
   => transpose a matrix
   => calculate mean vector of a matrix
   => add two matrices
   => multipy two matrices
=> general format of the matrix command is: matrix OPERATION [ARGUMENT]

Specifications:
=> program must perform the following ops: dims, transpose, mean, add, and multiply
=> dims, transpose, mean, either perform their ops on file name MATRIX or on a matrix provided via stdin
=> add and multipy don't need to process input via stdin
=> dims print dimensions of matrix as # of rows, space, then # of columns
=> transpose reflect the elements of the matrix along the main diagonal (MxN becomes NxM)
=> mean take in MxN matrix and return an 1xN row vector, where the first element is the mean of column one and so on
=> add take two MxN matrices and add them together element-wise to produce MxN matrix, add should return error if matrices don't have same dimensions
=> multiply take an MxN and NxP matrix and produces MxP matrix
=> check that given input file is readable beforing trying to read it
=> not required to test if the input file itself is valid
=> valid matrix is:
   => tab-delimited table with at least one element
   => each element is a signed int
   => every entry is defined
   => table is rectangular
=> grading script does not send input into matrix program
=> not allowed to send matrices with characteristics as output from script either
=> don't have these outputs:
   => empty matrix
   => matrix where final entry on a row is followed by a tab character
   => matrix with empty lines
   => matrix with any element that is blank or not int
=> if input is valid, program output only stdoout, return value = 0
=> if invalid, program should output onlyt to stderr, return value =/= 0
=> program will be tested with matrices up to 100 x 100
=> use temp files and not arrays
=> use process id as part of name of temps
=> use trap to catch interrupt, hangup, terminate signals to remove temp files if prog is terminated unexpectedly
=> all values and results must be integers
=> use expr to do calculations, works only with whole numbers
=> round to the nearest integer
=> proper round: (a + (b/2)*( (a>0)*2-1 )) / b

Hints:
=> write each part as separate function
=> need the read command alot 
   => one line at time from stdin buffer and stores the line in REPLY variable
   => used in a while loop where file is redirected to stdin of the while loop
   => read < myfile muliple times will repeatedly read the first line of myfile
=> expr command and the shell can have conflict over special characters, use backslashes
   => expr 5 \* \( 4 + 2 \)

