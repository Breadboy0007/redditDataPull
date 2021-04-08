# redditDataPull
Data pull from api.pushshift.io

This code is used to find the most popular subreddit submissions relative to specified time periods.

Giver an ordered list of epoch timestamps denoted E(0), ... , E(n-3), E(n-2), E(n-1), E(n) this code :
1. Counts the number of comments made between E(0) and E(1) for each existing submission within a given subreddit
2. Returns a list of the titles for the top X submissions based on number of comments made during the time period E(0) to E(1)
3. Returns the number of comments made between the time period from E(0) to E(1) for each of the top X submissions 
4. Moves on to the next time period between E(1) and E(2)
5. Finishes when it is done with the time period E(n-1) to E(n)
6. Returns a dataframe with columns=X and rows=n+1
