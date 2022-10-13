# movie_project
##Reporting: wrangle_report
- Documentation
After gathering the three files used in this Project, i accessed them indiviually and below are the summary of
each file:
- A. "twitter archive enhanced file" which was assigned as "twitter_df" having #2356 rows × 17 columns
#tweet_id
#in_reply_to_status_id
#in_reply_to_user_id
#timestamp
#source #text
#retweeted_status_id #retweeted_status_user_id
#retweeted_status_timestamp #expanded_urls
#rating_numerator
#rating_denominator #name
#doggo
#floofer
#pupper #puppo
- B. "image prediction file" which was assigned as "Image_df" having #2075 rows × 12 columns #tweet_id
#jpg_url
#img_num #p1 #p1_conf
#p1_dog #p2 #p2_conf
#p2_dog #p3 #p3_conf
#p3_dog
- C. tweets_df which was gotten from the twitter API on @weratedogs having #2354 rows × 3 columns
#favorite_count #retweet_count
#tweet_id
A common column here is the tweet_id which was used to merge the 3 tables together for visualisation at
the end of the wrangling act Project. This was so because we needed data that was only for dogs and since
the first two files contained data that were not only for dogs we had to filter out the data not for dogs by
first filtering only dog images on the predictions file, which showed True for dog image with a high
percentage confirming it being a dog(Some numerator rating of decimls were also removed). And then
merging this new data with the "twitter archive enhanced" file, which merged only the True dog image
prediction tweet_id and corresponding tweet_id in the twitter archive enhanced", which was then merged
with the corresponding tweet_id of the retweet and favourite count tables that is the tweets_df. A copy of
these files were made giving a diferrent naming before any wrangling process was done. ta_df=
twitter_df.copy() ip_df= image_df.copy() tw_df= tweets_df.copy()
Notes
The Dogtionary explains the various stages of dog: doggo, pupper, puppo, and floof(er) (via the
#WeRateDogs book on Amazon)
Image Predictions File was gotten by running Twitter archive enhanced through a neural network that can
classify breeds of dogs*.
Enhanced Twitter Archive
The WeRateDogs Twitter archive contains basic tweet data for all 5000+ of their tweets, but not everything.
One column the archive does contain though: each tweet's text, which I used to extract rating, dog name,
**Errors Found and how it was treated..
- A. Visual Assesment we found
1. Inconsistent representation of NaN (null values) we have None also as a representation.
(#twitter_archive_enhanced table)
2. "a","an" and "the" as name of dog (#twitter_archive_enhanced table)
3. #22, has "such" as a dog name (#twitter_archive_enhanced table)
4. #2326, has "quite" as a dog name (#twitter_archive_enhanced table)
5. Inconsistent representation of data name (Small and big case-types of names) (#image_prediction
table)
6. Underscore included in the names of Dogs (#image_prediction table)
7. there are data that are not dogs (#image_prediction table)
- B. Programatical Assessments
Using
twitter_df.name.unique(),twitter_df.rating_denominator.unique(),twitter_df['rating_numerator'].value_counts(
it confirmed the visual assessment that some names of dogs are not acurrate e.g "Unaccepted","mad"
1. (#correct Fwed to Fred, correct Billl to Bill, correct Joshwa to Joshua, correct Bobb to Bob, correct
Jockson to Jackson)
2. Correct the denominators back to 10
3. we would analyse this data and correct some assuming they were typographical errors and inaccurate
data
a. since they are good dogs and the ratings are majorly above 10 and below 16 (i found out that on
@weratedog's page the highest rating's for dogs is 15/10 which is named after their dog's foundation
15over10.)
and dog "stage" (i.e. doggo, floofer, pupper, and puppo) to make this Twitter archive "enhanced." Of the
5000+ tweets, I have filtered for tweets with ratings only (there are 2356).
- Conclusion
All errors listed were corrected and the merged table wwa used for Visualization to know the correlation
between the Dog Ratings and the Retweet counts an also the Dog Ratings and the Favorite counts .
References
www.google.com
https://www.geeksforgeeks.org
https://twitter.com/dog_rates
