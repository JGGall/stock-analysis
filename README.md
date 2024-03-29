# VBA Challenge

## Overview
The purpose of this analysis was to take the code already written to analyze the 2017 and 2018 performance of a certain group of green energy stocks and refactor it so that it would perform the analysis more efficiently, and thus in less time.


## Results
The performance of the stock of twelve green energy corporations varied a great deal between 2017 and 2018. The original code and the refactored code produced the same result: three columns featuring the twelve companies arranged alphbetically by ticker designation, the total daily volume of each, and the percentage return of each for each year. The annual percentage return was colored green if the return was a positive number, and it was colored red if it was a negative number.
The following screenshots illustrate the 2017 and 2018 output of the original and refactored versions of the code, as the output was exactly the same:

![analysis_2017](Resources/analysis_2017.png)

![analysis_2018](Resources/analysis_2018.png)


The original code looped through all of the rows of one ticker to get the total volume for the year. Then it got the starting and ending prices of that same ticker, output the data, and moved on to the next ticker.

By means of refactoring, the code becomes more efficient by avoiding some of the looping. The refactored code sends trading volume, starting prices, and ending prices to three arrays, and then needs only to loop through those arrays in order to output the data to the workseet.

Here is an illustration of the pertinent section of the refactored code:

![Refactored_code](Resources/Refactored_code.png)

The refactored code reduced the run time of the program from about 0.65 and 0.64 seconds for 2017 and 2018, respectively, to 0.13 and 0.13 seconds.
The following are images taken from message boxes that state the run time of the slower original code and the more efficient refactored code:

![slower_2017](Resources/slower_2017.png)

![slower_2018](Resources/slower_2018.png)

![VBA_Challenge_2017](Resources/VBA_Challenge_2017.png)

![VBA_Challenge_2018](Resources/VBA_Challenge_2018.png)

## Summary
#### What are the advantages or disadvantages of refactoring code?
##### *Advantages*
Refactored code enables the program to run without looping through rows unless it is necessary for it to do so. It is thus able to run more efficiently, requiring less time to perform the calculations. In a small dataset this would make little difference, but it leads to much greater speed when the program is analyzing very large quantities of data. 
##### *Disadvantages*
Refactored code is more complicated to write and to understand.


#### How do these pros and cons apply to refactoring the original VBA script?

*Pros*

The VBA script analyzes a dataset that is 3013 lines long. It is impressive to note that even with that moderate amount of data, the refactored code ran in only 20% of the time the original code required--a savings, of course, of 80%.

*Cons*

The effort required to refactor the original code might not be worthwhile if the analysis is intended to be run only once or only infrequently, as even the original code ran in less than one second. Code should be refactored if the amount of data to be analyzed is large, and the efficiency it produces is useful.
