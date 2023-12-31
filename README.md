_This framework is **highly experimental** and **very likely** to change significantly_

# feeder

`feeder` is a small Python framework that helps you generate [JSON Feeds][jsonfeed.org].


## Usage

Install from PyPI:

```
python3 -m pip install json-feeder
```

Create a directory for your new feed, the start the new feed with:

```
feeder startfeed
```

`settings.py`, `feed.py` and `generate.py` files will be created for you.

To get started simply update the `get_items()` function in `feed.py` to return a list of `FeedItems`.

Generate the feed with:

```
python3 generate.py
```

The following settings can be configured:

- `FEED_FUNCTION` the path to a Python function that will return a list of `FeedItem` objects.
- `FEED_FILENAME` the filename on disk for the feed. If you are using Github Pages then this should be set to `out/feed.json` or similar.
- `FEED_URL` the remote url of the feed. This is used to ensure that duplicates are not added to the file.
- `FEED_TITLE` is the title of your feed.
- `FEED_HOMEPAGE_URL` is the homepage of your feed, this is optional.
- `FEED_ICON` is a url to an icon that feed readers might use for your feed. Very optional.
- `FEED_VERSION` defaults to "1.1" and represents the JSON Feed version.
- `FEED_MAX_ITEMS` limits the number of items to output in the feed. Default is 100.



### Runnings Tests

```
python3 -m unittest discover
```


  [jsonfeed.org]: https://www.jsonfeed.org
