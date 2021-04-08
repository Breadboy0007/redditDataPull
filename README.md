# redditDataPull
Data pull from api.pushshift.io

This code is used to find the most popular subreddit submissions relative to specified time periods.

Given an ordered list of epoch timestamps denoted E(0), E(1), E(2), ... , E(n-2), E(n-1), E(n) this code :
1. Counts the number of comments made between E(0) - E(1) for each existing submission within a given subreddit
2. Returns a list of the titles for the top X submissions based on number of comments made during the time period E(0) - E(1)
3. Returns the number of comments made in the time period E(0) - E(1) for each of the top X submissions 
4. Moves on to the next time period E(1) - E(2) and so on and finally finishes when it is done with the last time period E(n-1) to E(n)
5. Returns a dataframe with columns=X and rows=n+1
