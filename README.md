# twitter-scrapper
A small Ruby script for scrapping and classifying tweets to create a training dataset for CNN

# Scrap

* Create an application on Twitter
* Get your keys and tokens and set them as env variables (check the scrapper file for the names ; you can create a `credentials.*` script that does this for you)
* Run the scrapper and get the results in scraps/

The scrapper tries to clean up tweets by removing \`RT @user:', links, unprintable characters, and adding whitespace between punctuation signs (this should help CNN classifiers recognize separate words better)

For now the scrapper will only read tweets with language set to french or undefined, this will be configurable later on

# Classify

* Run the classify script after running the scapper (supports classifying multiple runs at once)
* The script will show you a tweet. Press left if the tweet sentiment is positive, up if neutral or right if negative. You can skip a tweet by pressing down if it is not relevant or contains garbage data (this can happen)
* You will find your results in output/run-{timestamp}
