_This framework is **highly experimental** and **very likely** to change significantly_

# feeder

`feeder` is a small Python framework that helps you generate JSON Feeds.


### Usage

Start a new feed with:

```
feeder startfeed
```

A `settings.py` and `generate.py` file will be created for you.

The following settings are important:

- `FEED_FUNCTION` the path to a Python function that will return a list of `FeedItem` objects.
- `FEED_FILENAME` the filename on disk for the feed. If you are using Github Pages then this should be set to `out/feed.json` or similar.
- `FEED_URL` the remote url of the feed. This is used to ensure that duplicates are not added to the file.
- `FEED_TITLE` is the title of your feed
- `FEED_HOMEPAGE_URL` is the homepage of your feed, this is optional

Once you've updated your `settings.py` and created your `FEED_FUNCTION` you can generate your feed by running:

```
python3 generate.py
```


### Runnings Tests

```
python3 -m unittest discover
