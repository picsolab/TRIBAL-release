# TRIBAL
This git provides information about the TRIBAL project. The project outcome, including sharable data and programs, will be posted here when available.

## Dataset

This project uses a Twitter corpus collected in 2016. The details of our Twitter corpus and the collection process can be found in our paper [1]. In summary, our data collection was based on those "exclusive followers" -- i.e., Twitter users who followed only one presidential election candidate but not the other, whom we assume to be supporters of the candidates. To test this hypothesis, we examined the extent to which the exclusive followers expressed their support explicitly. We examined the odds ratios based on a set of most frequently observed support or disapproval hashtags. The hashtags are either from the campaign slogans of the candidates or are simply stating the support. The four hashtags of supporting Trump are highly associated with "exclusively following Trump" (11-24 times more likely), while the other four hashtags of supporting Clinton (especially "#ImWithHer" and "#DumpTrump") are associated with "exclusively following Clinton" (4.46-13 times more likely). 

The data collection involves multiple steps. 
1. We acquired the followers of Trump and Clinton at two time points, respectively. These two are Aug. 30, 2016, and Nov. 15, 2016 (one week after the election). Then, we cross-identified the users who exclusively followed Trump at both time points (not following Clinton), and vice versa for Clinton. 
2. After getting the list of exclusive followers, we acquired the user profile of a sampled 600k users from each set, and further among which we obtained a stratified sample of 25% users based on the level of user activity defined by the tweet count. The users are segmented into ten quantiles, where each of them contains 10% of all population based on the amount of tweets users published. Then, for each quantile, we randomly sample 25% of the users to construct the final set of users so that our users are representative of the Twitter population with respect to different levels of Twitter activities. The sampling ratio is limited as 25% due to the data collection capacity. 
3. We acquired the timeline tweets of the resultant set of users (over 300k users in total). We further retrieved users who posted non-retweet tweets within a 9-month period (between 06/2016 and 02/2017), which resulted in over 214K users.

The dataset released here include:
* The IDs of 214K users from two groups:
** con group (Trump supporters)  : 111,528; filename: `users_ids_con.csv.zip`
** lib group (Clinton supporters): 102,499; filename: `users_ids_lib.csv.zip`
* The IDs of 32M non-retweet tweets posted within the 9-month period.
** total number of tweets: 32,435,958; filename: `tweets_org_ids.csv.zip`

## References
[1] Yan, M., Wen, X., Lin, Y.-R., Deng, L. (2017). Quantifying Content Polarization on Twitter. In Proceedings of 2017 IEEE International Conference on Collaboration and Internet Computing (IEEE CIC 2017) 
