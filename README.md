# Data Wrangling

This Jupyter Notebook assists in data analysis of WeRateDogs dataset consisting of 3 subsets:
1. csv file (WeRateDogs tweet archive),
2. tsv file downloaded from a URL (Neural Network image Analysis results of WeRateDogs tweets),
3. data downloaded using Twitter API (WeRateDogs tweet statistics).
The data is combined into a one dataset, cleaned and analyzed. 3 insights are proposed.

The project consists of:
1. **wrangle_act_final.ipynb** - a Jupyter Notebook with code and comments,
2. **wrangle_act_final.html** - rendered HTML version of the file above,
3. **act_report.pdf** - a PDF with 3 insights, each having a visual and a short comment,
3. README - this readme ;]

## Project breakdown
1. **Gather** deals with importing data.
   1. Prepare the first part - load the WeRateDogs Twitter archive
   2. Prepare the second part - neural network predictions of the dog breed
   3. Prepare the third part - Twitter data
2. **Assess** prepares these for the Cleaning, i.e. quality and tidy steps
are assessed.
   1. Dog stages
   2. Retweets
   3. Rating numerator/denominator problems
   4. Names
   5. Object prediction names
3. **Cleaning** does the following:
   * removes nulls, retweets, unnecessary data
   * transforms tweet id type from integers to strings
   * rating correction
   * correction of dog names and object prediction names
   * rounds up dog stages into a single column
4. **Storing, analyzing and visualizing** sums up the results in
*twitter_archive_master.csv* file. 3 insights are proposed and 1 visual is created.

## Prerequisites - what You need to use this project

 1. Jupyter Notebook with Python 3 environment
 2. Python libraries:
    1. for data structure, calculations and dataset manipulation
       * **pandas**
       * **numpy**
    2. for visuals
       * **pyplot** (part of **matplotlib**)
    3. for importing data using a URL
       * **requests**
       * **StringIO** (part of **io**)
    4. for importing Twitter data
       * **tweepy**
    5. for converting json data to a Python dictionary
       * **json**
    6. for managing running time
       * **time**
3. WeRateDogs Twitter archive (this was provided by Udacity)
4. Neural Network Predictions of dog breed (this was provided by Udacity as a `.tsv`
  file to be pulled from [here](https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv).
5. Twitter Developer account - for importing tweet information, absent in `3.`

## Troubleshooting
This README covers the Data Wrangling project as part of the Udacity
Data Analyst for Enterprise Nanodegree. As a result, some parts of the source
code are not supported. If you want to check the code and any of the Prerequisites
are not met (e.g. files are missing) please consult the rendered HTML version of the Notebook.
The management of the archive is not flexible - only `.csv` file is accepted
and it must contain **tweet_id** column.
The URL for Neural Network Predictions `.tsv` was valid in 2019 and is not
guaranteed to be supported.
Twitter Developer details are absent in the `wrangle_act_final.ipynb` and must
be filled in. These are: _consumer_key_, _consumer_secret_, _access_token_,
_access_secret_.

## Acknowledgements
WeRateDogs files were provided by Udacity.

## License
This project is licensed under the terms of the MIT license.
