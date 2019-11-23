
This folder contains various processing class that are used to perform analytical task on GitHub data. Individual metrics are obtained.

All these class use load and dbconnect read data from S3 and store it to database respectively.


#To count the commits in specific language
psql -h 10.0.0.14 -p 5432 -U dbuser -W resultdb
# 1: run users.csv and store to resultdb.
spark-submit main.py 1
to run user_load with larger memory
spark-submit --driver-memory 8g --executor-memory 8g --master spark://ec2-100-20-13-37.us-west-2.compute.amazonaws.com:7077 main.py 11


Options:
      2: count local commits
      22: count Commits for a user from s3 [s3 data]")
      3: count followers for a user [local]
      33:count followers for a user [s3]
      4: count projects owner by user [local]
      44: count project owned by user [s3]
      

