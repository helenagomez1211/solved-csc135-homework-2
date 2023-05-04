Download Link: https://assignmentchef.com/product/solved-csc135-homework-2
<br>
For homework #2, you are to use Dr. Racket.

NOTE: You are ONLY allowed to use the basic built-in functions listed near the top of page 2of the Scheme course notes. Any other function that you need MUST be defined by youas part of your solution(s). You must NEVER use the “set!” function.

NOTE: In Dr. Racket, please select the language called “R5RS”.

NOTE: You ARE allowed to use the functions “quotient” and “list?”.




Write the following Scheme functions:

—-

A. “appendInt” – takes two positive integers N and M, and returns an integerwhere M is tacked on the end of N.For example:

(appendInt 124 80534) will return 12480534(appendInt 2479 9634) will return 24799634(appendInt 5 456) will return 5456.

B. “listsMax” – takes two lists of integers of the same length, and returns a listwhere the elements are the max value of the two elements in the same positionof each list. You may assume that the two input lists are the same length.For example:

(listsMax ‘(2 5 11 25 9) ‘(2 9 10 20 12)) will return ‘(2 9 11 25 12)(listsMax ‘(3 4 3 8) ‘(7 5 6 2)) will return ‘(7 5 6 8)

C. “cycler” – takes a list L and an integer N, and returns an integer which is theresult of “cycling” N through the list L. “Cycling” is done by successivelyapplying the operations addition (+), subtraction (-) and multiplication (*) usingeach of the integers in L until they are exhausted. If the length of L is longerthan 3, then the +, -, and * operations repeat. You may assume that the list Lhas at least one number in it.For example:

(cycler ‘(3 8 2 6 4 5 5) 28) returns 245, because:

28 + 3 = 3131 – 8 = 2323 * 2 = 4646 + 6 = 5252 – 4 = 4848 * 5 = 240240 + 5 = 245

D. “functionWinner” – takes as input a Boolean function F, and two lists L and M.It returns:

the number 1 if list L is the “winner”the number 2 if list M is the “winner”the number 0 if the two lists are tied

The “winning” list is the one for which the function F has the most “true” answersamong the values in the two lists.For example:

(functionWinner isNeg ‘(8 -4 3 8) ‘(7 -3 -2 1 -5)) returns 2,because the second list has more negative numbers than the first list.

(functionWinner isEven ‘(8 -4 3 8) ‘(6 3 2 1 -4)) returns 0,because the two lists have the same number of evens in them.

E. “countTrue” – takes a list L (which may include sublists) and a Boolean function F,and returns a count of the number of elements in the list for which F returns true.Elements nested in sublists are included. You only need to handle functions F definedfor scalar inputs. For example:

(countTrue ‘(3 (2 1 -5) 6 (7 (2 (-3) 5))) isOdd) will return 6(countTrue ‘(3 (2 1 -5) 6 (7 (2 (-3) 5))) isNeg) will return 2

F. “badNumberRemover” – takes a list L that contains only numbers.It then builds a “remover” function based on L.

The resulting “remover” function can take a list of numbers, and return an identicallist except that the “bad” numbers have been removed. The “bad” numbers are any ofthose that were specified in the original list L.For example, if badNumberRemover was called as follows:

(define B (badNumberRemover ‘(42 13 4)))

then the produced function B would behave as follows:

(B ‘(83 2 17 42 9 100 42 13 17 29)) would return (83 2 17 9 100 17 29)

Your task is to write badNumberRemover, not P.You will probably find it useful to write one or more utility functions.Of course, badNumberRemover should work for any reasonable input list L,not just the one shown above.

=============================================================Submission instructions:

– Place all of your Scheme functions in ONE text file.– Test your functions in Racket before submitting the file in Canvas.– Include comments in your code clearly delineating each of the problems.