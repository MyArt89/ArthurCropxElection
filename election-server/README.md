# election
The future election system
REST API
/election
show the Top Leading Score of the selected Campaign.
The only Generated Campaign , number may Change for Other Campaigns
election/electionScore/campaign?Id=1

User with with Id = 2 votes for User with Id 9 on Campaign Number 1 
/election/vote?campaign=1&user=2&candidate=9

I used Get Method instead of Post as shown In the Example.

I did not use Many To Many at the
User Candidate Campaign because I didn't see any need for it.

When using Spring Each JpaRepository uses a new and separate EntityManager 
session to the data base so many requests may be called for the same 
Table by many users without interference as long as the same voter can 
not vote more than once in parallel .  
