# Notes on the Midterm

* _Correctness    (out of 40):_ 40
* _Good Practices (out of 10):_ 8
* _Docs / Testing (out of 10):_ 10

_Details on the grading criteria for the midterm can be found on [Canvas](https://canvas.slu.edu/courses/28045/rubrics/23671)._

It total, for the several comments I made below about style, I've deducted 2 points from _Good Practices_.

You did a great job with docstrings and tests!

## Step 1
* Note where you are computing `mean()` -- it is inside the loops. So, it will recalcualte the mean after reading each item. That's unnecessary and can be saved until the end, right before returning it.

## Step 2
* Your choice to break this into two separate sets of loops is a bit confusing. Rather than storing everything in a rate_list and then checking, you could have done the checks as you read in the data.

## Step 3
* Your choice to explicitly define all conditions instead of just using the else as the "anything that doesn't match my exception" criteria causes a little bit of confusion. Better to have `else: adjusted_price = before_adj_price`.

## Step 4
* Your choice to use exception handling here is interesting. It looks like it's meant to catch anything weird that might happen in getting the price and accumulating it -- maybe that's your way of handling Nones. Blunt exception handling like this, though, is not best practice.
