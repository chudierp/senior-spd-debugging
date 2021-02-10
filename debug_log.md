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
changed "topping" to topping_type. Also, the redirect method had an endpoint in it, instead of the function that you want to redirect to. It was '/' when it should be 'home'. Then I used the trace backward technique starting at line 89 where the call is made to add the pizza to the db. I discovered that the pizza_order_submit() was retrieving the wrong names of the input fields in the form. However, this still didn't fix the bug. I noticed that db.session.commit() was called in other areas after making calls to the database. So I added it after adding to the db when submitting an order, and before making a query call in the home function.



## Exercise 2

[[Your answer goes here!]]
- I added a .env file in directory to store API key. I then corrected the url to make the correct API call. I was getting  KeyError: 'temperature'. So I looked at line 54 and noticed 'temp' was spelled out as 'temperature' in the JSON data, so when I corrected the spelling, the weather app worked but when I looked over the results I noticed that although I selected Fahrenheit, it was still displaying it in Kelvin so I changed the API call to units=imperial, and went to the results.html file  

## Exercise 3

[[Your answer goes here!]]
- [IndexError: list index out of range] line 37. Solution was I changed the index variable from the left subarray to the right.
- [TypeError: list indices must be integers or slices, not float]: I changed line 48 from the classic division sign to double-slash for “floor” division (rounds down to nearest whole number).
- [Sorted list of nums isn't actually sorted] the index for the sorted array wasn't being updated in both while loops that take care of extra numbers that haven't been visited in either halves of the subarray
