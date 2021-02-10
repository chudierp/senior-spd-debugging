# Debug Log

**Explain how you used the the techniques covered (Trace Forward, Trace Backward, Divide & Conquer) to uncover the bugs in each exercise. Be specific!**

In your explanations, you may want to answer:

- What is the expected vs. actual output?
- If there is a stack trace, what useful information does it contain?
- Which technique did you use, on which line numbers?
- What assumptions did you have about each line of code, and which ones were proven to be wrong?

_Example: I noticed that the program should show pizza orders once a new order is made, and that it wasn't showing any. So, I used the trace forward technique starting on line 13. I discovered the bug on line 27 was caused by a typo of 'pzza' instead of 'pizza'._

_Then I noticed another bug ..._

## Exercise 1

[[Your answer goes here!]]
TypeError: 'topping' is an invalid keyword argument for PizzaTopping
changed "topping" to topping_type



## Exercise 2

[[Your answer goes here!]]
- I added a .env file in directory to store API key. I then corrected the url to make the correct API call. I was getting  KeyError: 'temperature'. So I looked at line 54 and noticed 'temp' was spelled out as 'temperature' in the JSON data, so when I corrected the spelling, the weather app worked but when I looked over the results I noticed that although I selected Fahrenheit, it was still displaying it in Kelvin so I changed the API call to units=imperial, and went to the results.html file  

## Exercise 3

[[Your answer goes here!]]
- [IndexError: list index out of range] line 37. Solution was I changed the index variable from the left subarray to the right.
- [TypeError: list indices must be integers or slices, not float]: I changed line 48 from the classic division sign to double-slash for “floor” division (rounds down to nearest whole number).
- [Sorted list of nums isn't actually sorted] the index for the sorted array wasn't being updated in both while loops that take care of extra numbers that haven't been visited in either halves of the subarray
