# Stock Analysis

## Overview of Project

In order to determine the best "Green" stocks to invest in, a workbook was created to analyze total volume traded and the return on 12 different stocks on an annualized basis. Additionally, the VBA macro used to perform these functions was refactored to reduce the time spent performing the macro. 

## Analysis and Results

### Initial Code

For the first draft of this macro a loop was created that cycled through each ticker being analyzed. For each ticker the macro looped through all the data and found the annualized total volume traded, beginning price, and ending price. The prices were used to calculate the return for each ticker. The spreadsheet was then formatted to make it more easily readable.

Image 1: Initial macro results and runtime

![2018 initial results and runtime](https://github.com/TravisTornquist/stock-analysis/blob/main/Resources/VBA_Challenge_2018.png)

The macro ran in a little over half a second.

### Refactored Code

For the refactored code, a variable was created to act as an index relating to each ticker. Additional arrays were then created to store trading volume, beginning price, and end price for each index. A loop was then created to run through the data a single time, storing information for the specific index and incrementing the index each time the data moved to a new ticker.

Image 2: Refactored macro results and runtime

![2018 refactored results and runtime](https://github.com/TravisTornquist/stock-analysis/blob/main/Resources/VBA_Challenge_2018_Refactored.png)

The macro ran in less than a tenth of a second.


## Summary

### Refactoring as a General Practice

Refactoring code can be a valuable step in the development process. For complicated macros or particularly large data sets refactoring can result in significant long term time savings by reducing runtime of the code. It isn’t always valuable to refactor code though, since a macro that is already running quickly won’t have enough time savings to make up for the time spent refactoring the code.

### Refactoring this Stock Analysis

The initial macro for this stock analysis ran in a little over half of a second. After refactoring the code runs nearly half a second faster. The benefit of this refactor is a fairly small time savings each time the code is run. The macro is so much more efficient because it loops through the data only once rather than once for every ticker. The disadvantage of this refactor is that the time spent refactoring is far greater than the time savings. Although the new code runs more efficiently, it would have saved time in the long run keeping the original code.
