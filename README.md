# reddit hacks

This is a compendium of rough code to demonstrate how to interact with new
reddit API features.

## Libraries

The `redditclient` module provides a basic API client. Currently it only
supports signing in and the upcoming "flair" feature.

## Tools

The `flairsync` script provides a simple way to maintain a subreddit's flair
using a local CSV file.

## Example commands

1) Set flair templates to contents of CSV file

```
cat flair.csv
  text,css,editable
  ,aaa,off
python flairsync.py -t subredditname flair.csv
```

2) Set user flair to contents of CSV file

```
cat test.csv
  user,text,css
  intortus,zzr600,kawasaki
flairsync.py -c intortus.cookie example test.csv
```