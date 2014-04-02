# My title

Tap into [The Echo Nest's](http://the.echonest.com/) Musical Brain for the best music search, information, recommendations and remix tools on the web.

Pyechonest is an open source Python library for the Echo Nest API.  With Pyechonest you have Python access to the entire set of API methods including:

* **artist** - search for artists by name, description, or attribute, and get back detailed information about any artist including audio, similar artists, blogs, familiarity, hotttnesss, news, reviews, urls and video.
* **song** - search songs by artist, title, description, or attribute (tempo, duration, etc) and get detailed information back about each song, such as hotttnesss, audio_summary, or tracks.
* **track** - upload a track to the Echo Nest and receive summary information about the track including key, duration, mode, tempo, time signature along with detailed track info including timbre, pitch, rhythm and loudness information.

## Install
There are a few different ways you can install pyechonest:

* Use setuptools: `easy_install -U pyechonest`
* Download the zipfile from the [releases](https://github.com/echonest/pyechonest/releases) page and install it. 
* Checkout the source: `git clone git://github.com/echonest/pyechonest.git` and install it yourself.
   
## Getting Started
* Install Pyechonest
* **Get an API key** - to use the Echo Nest API you need an Echo Nest API key.  You can get one for free at [developer.echonest.com](http://developer.echonest.com).
* **Set the API** key - you can do this one of two ways:
* set an environment variable named `ECHO_NEST_API_KEY` to your API key
* Include this snippet of code at the beginning of your python scripts:

```python
    from pyechonest import config
    config.ECHO_NEST_API_KEY="YOUR API KEY"
```

* Check out the [docs](http://echonest.github.com/pyechonest/) and examples below.

## Examples
*All examples assume you have already setup your api key!*

Find artists that are similar to 'Bikini Kill':

```python
from pyechonest import artist
bk = artist.Artist('bikini kill')
print "Artists similar to: %s:" % (bk.name,)
for similar_artist in bk.similar: print "\t%s" % (similar_artist.name,)
```



-![alt text](http://i.imgur.com/WWLYo.gif "Frustrated cat can't believe this is the 12th time he's clicked on an auto-linked README.md URL")