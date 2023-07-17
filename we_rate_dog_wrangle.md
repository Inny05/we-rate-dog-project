# WeRateDogs Wrangle report</div>
## Data gathering

>Three datasets were used for this project which I gathered using different methods. To start this project, I imported different librarieswhuch include; (pandas, tweepy, seaborn, matplotlib, json, request, etc.). The first dataset was a csv file which I read using the pandas library, the second data set was obtained using the request library. While for the last dataset, I scraped from twitter using tweepy to access the Twitter Api.

## Data assessing

>The data acquired required cleaning as it was messy. I identified 10 issues and fixed them. The issues I identified were; wrong data types, missing values in rows and columns, duplicate values in columns and rows.

To commence cleaning the data, I merged the datasets into one document. After assessing the data manually and programmatically, it was discovered that columns like; _retweeted_status_id, retweeted_status_user_id, retweeted_status_timestamp, in_reply_to_status_id and in_reply_to_userid had over 2000 missing values and would have to be dropped. I discovered that the tweet_id column had duplicate columns, and its data type was an integer instead of an object data type.

I also discovered that the doggo, pupper, floofer and puppo which are dog growth stages, were recorded in columns, instead of having it all merged into one column.
The timestamp and retweeted_status_timestamp were recorded as object data types instead of datetime objects.

## Data cleaning

>Tidiness issues To clean the dataset I had two tidiness issues which includes having multiple datasets to work with and having different columns for the dog stages. To sort this, a copy of the datasets was stored in another variable and merged into one dataset on the tweet ID using a left join and the dog stages were also merged into one column.

Quality issues_ Columns with too many missing values were dropped using the pandas ‘drop’ function, and duplicate columns were also dropped. Rows with missing values were also dropped using the ‘dropna’_ function. The columns dropped include using the drop function include: in reply to status id, in reply to user id, retweeted status id, retweet count, retweeted status user id, retweeted status timestamp and expanded urls. The rows dropped using the dropna function include: p1, p1 conf, p1 dog, p2, p2 conf, p2 dog, p3, p3 conf,p3 dog, favorite count.

Columns with wrong data types were converted to the correct data type using the ‘astype’ function.The tweet ID was converted to an object data type, the timestamp column was converted to a datetime data type using the ‘_pd.todatetime’ function. Two columns were also converted to the category which include: The dog stage columns and the tweet Id columns using the astype('category') function. The rating numerator and the rating denominator columns were converted to float data type using the astype('float') function. The source name was extracted using the split function to get the last word which is the source name.

## Data visualization 
>From my visualizations, I observed that the iphone accounts for the source of about 90% of the tweets. The golden retriever dog specie was the most predicted specie of dog and the labrador retriever was the second most predicted dog specie.

Finally, I stored the clean data as a _'twitter_archivemaster.csv' file.
