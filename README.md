# Monty Hall Problem - Statistical Analysis by Mass Simulation

<h2>Overview of the problem</h2>
1. There are 3 doors. Behind one door is a car, and behind the other two doors are goats. 
2. You pick a door, any door, which you think has a car in it, but you don't open it. 
3. The game master then opens a door containing a goat (from the two remaining doors).
4. You are given the option to switch to the remaining door, or stay with the door you have selected. Which one has the better odds?

More information: https://en.wikipedia.org/wiki/Monty_Hall_problem

<h2>About the simulation</h2>
The Monty Hall problem is a famous, seemingly paradoxical problem in conditional probability and reasoning using Bayes' theorem. Information affects your decision that at first glance seems as though it shouldn't.

This is a statistics problem that has been bothering me for a while now, and I decided to analyze it by simulating 2 million games and seeing what the win ratio would tell us about certain strategies.

The answer to the problem is to switch doors, because you are more likely to win (about 2/3 as likely). This is counter-intuitive and has never made sense to me in middle school, so clearing this confusion was the inspiration for this project.

<h2>Analysis (using 2 million data points)</h2>

<h4>Strategy 1 - Switch</h4>

Sample output:
>Win count: 666834.0

>Loss count: 333166.0

><b>Win ratio: 0.666834</b>

When I first saw this data, I got really excited. I've been told that the odds of winning are supposed to be around 2/3. 
This data supports this claim because 2/3 = 0.666666....
Through the use of 1 million data points, we can see that the win ratio (0.666834) is approaching this value.

<h4>Strategy 2 - Do Not Switch</h4>

Sample output:
>Win count: 333576.0

>Loss count: 666424.0

><b>Win ratio: 0.333576</b>

We can see that the win ratio is 0.333576 which is close to 1/3.

<h4>Conclusion</h4>
There is a clear difference in the odds of winning when using both strategies. If you do not switch, you will only win ~33% of the time. However, if you do switch, your chances of winning increase to ~66% of the time. 

I finally understand the problem after creating this model, and I hope this has helped you in a similar way. Feel free to test for greater amounts of data points by changing both instances of variable <i>numGames</i> in the <i>Statistics</i> class to a value >1000000.
