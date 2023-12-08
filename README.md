# INFO 201 Lab: Cleaning and Reshaping
November 23, 2023

1 Dawg dash running times
Here we use UW/Alaska Airlines Dawgs Dash results data from Oct 8, 2023, file “dawgs-dash-5k-
2023.csv.bz2”. This was a 5k run on campus (where several of your team members participated
,), and the dataset contains their running time and basic demographics (age and gender). The
variables are
rank : place in the race. It is min rank, so if several runners share the same time, all they get
the lowest rank there, but the next ones will be ranked lower by the number of shared-time
runners.
category : in the form age | gender where gender is “M” or “F”, or empty.
time : either mm:ss or hh:mm:ss, depending on if the time was less or more than 1h.
For context: top athletes run 5k in less than 15 minutes, when you walk with a good pace,
you do 5k in about 1 hour.
bib : bib number of the runner
1. Load the Dawgs Dash dataset and ensure it is good.
2. What are the data types of the columns category and time?
Hint: this is printed under the column names when you print the data frame, you can also
query those individually with class
3. Convert the time to duration, but so that format “mm:ss” is understood as minutes-seconds,
and “hh:mm:ss” is understood as hours, minutes, seconds.
See info201 book, Ch 15.2 Date and time.
4. Look at the time of 3 fastest, and 3 slowest runners. You can just use head and tail as data
is ordered by time. Do the results look sensible?
5. Finally, make a histogram of the running times.
1
2 Reshape
Here we use UAH lower troposphere data, wide form UAH-lower-troposphere-wide.csv.bz2.
1. Load the dataset, and ensure it is good.
We only need variable year, month, globe, nopol, sopol below, you can just drop all the other
columns.
2. Now reshape the dataset into a long form: put all the values into a column temperature and
the regions globe, nopol, sopol into a column region.
Store the long form dataset into a variable.
3. Finally, take your long form dataset and reshape it back into the wide form. The result should
look like the original data!
