# Search Google developer videos

This is a prototype API and application for searching transcripts and metadata for videos from the [Google Developers](https://www.youtube.com/user/GoogleDevelopers), [Android Developers](https://www.youtube.com/user/androiddevelopers) and [Chrome Developers](https://www.youtube.com/user/ChromeDevelopers) channels.

**Application**: [simpl.info/s](https://simpl.info/s)

**API**: [shearch.herokuapp.com?q=webrtc](http://shearch.herokuapp.com?q=webrtc)

With minor tweaking the app and API can be used to build search for any YouTube channel with manually captioned videos.

<br>

<a href="http://simpl.info/s"><img src="https://cloud.githubusercontent.com/assets/205226/9225876/b89fc926-4103-11e5-9f8e-1250aa511fcd.png" width="440px"></a>

[![JSON response from shearch.herokuapp.com?q=webrtc](https://cloud.githubusercontent.com/assets/205226/9225854/9b1fadda-4103-11e5-9d6a-e7646900571d.png)](http://shearch.herokuapp.com?q=webrtc)

## Transcripts

For those who prefer to access information by reading text rather than watching videos, the app provides downloadable transcripts:

[simpl.info/s?t=ngBy0H\_q-GY](http://simpl.info/s/t/?id=ngBy0H_q-GY)

[![Developer video transcript](https://cloud.githubusercontent.com/assets/205226/9225860/9fdfd516-4103-11e5-91a6-667949eaca1c.png)](http://simpl.info/s/t/?id=ngBy0H_q-GY,3i9WFgMuKHs)

The transcripts have Google Translate built in, so you can choose read them in a different language. Caption highlighting is synchronised with video playback — and you can tap or click on any part of a transcript to navigate through the video.

[![Google Translate French translation of developer video transcript](https://cloud.githubusercontent.com/assets/205226/9225859/9fca0b1e-4103-11e5-8ca1-aa9a5a95127e.png)](http://simpl.info/s/t/?id=ngBy0H_q-GY,3i9WFgMuKHs)

## Examples

Search for something:
[simpl.info/s](http://simpl.info/s)

Readable transcripts for one or more videos:
[simpl.info/s/t?id=ngBy0H\_q-GY,3i9WFgMuKHs](http://simpl.info/s/t?id=ngBy0H_q-GY,3i9WFgMuKHs)

Link to a query:
[simpl.info/s?q=breakpoint](http://simpl.info/s?q=breakpoint)

Data and transcript for a video:
[shearch.herokuapp.com/2UKPRbrw3Kk](http://shearch.herokuapp.com/2UKPRbrw3Kk)

Transcript only:
[shearch.herokuapp.com/t/2UKPRbrw3Kk](http://shearch.herokuapp.com/t/2UKPRbrw3Kk) or
[shearch.herokuapp.com/transcript/2UKPRbrw3Kk](http://shearch.herokuapp.com/transcript/2UKPRbrw3Kk) or
[shearch.herokuapp.com/captions/2UKPRbrw3Kk](http://shearch.herokuapp.com/captions/2UKPRbrw3Kk)

Multiple values — comma, semicolon or pipe delimiter, spaces OK:
[shearch.herokuapp.com/2UKPRbrw3Kk,iZZdhTUP5qg](http://shearch.herokuapp.com/2UKPRbrw3Kk,iZZdhTUP5qg)
[shearch.herokuapp.com/t/2UKPRbrw3Kk,
iZZdhTUP5qg](http://shearch.herokuapp.com/t/2UKPRbrw3Kk,%20iZZdhTUP5qg)

Search any field for a query, spaces OK — can be a bit slow:
[shearch.herokuapp.com?q=http 203](http://shearch.herokuapp.com/?q=http%20203)

More shortcuts: c for captions, s for speaker — speakers are parsed from
transcript:
[shearch.herokuapp.com?c=svg&s=alex](http://shearch.herokuapp.com/?c=svg&s=alex)

Specify ranges for commentCount, dislikeCount, favoriteCount, likeCount,
viewCount:
[shearch.herokuapp.com?speaker=Jake&viewCount&gt;10000](http://shearch.herokuapp.com/?speakers=Jake&viewCount%3E10000)

Use any of these values to specify order:
[shearch.herokuapp.com?speaker=Jake&viewCount&gt;10000&sort=viewCount](http://shearch.herokuapp.com/?speaker=Jake&viewCount%3E10000&sort=viewCount)

Add a hyphen for descending order:
[shearch.herokuapp.com?speaker=Jake&viewCount&gt;10000&sort=-viewCount](http://shearch.herokuapp.com/?speaker=Jake&viewCount%3E10000&sort=-viewCount)

Show items with titles that include 'Android'
[shearch.herokuapp.com?title=Android](http://shearch.herokuapp.com/?title=Android) or
[shearch.herokuapp.com?t=Android](http://shearch.herokuapp.com/?t=Android)

Items with speakers that include Reto and a title that includes Android:
[shearch.herokuapp.com?title=Android&speakers=Reto](http://shearch.herokuapp.com/?title=Android&speakers=Reto)
[shearch.herokuapp.com?t=Android&s=Reto](http://shearch.herokuapp.com/?t=Android&s=Reto)

Spaces are OK:
[shearch.herokuapp.com?speakers=Reto
Meier&title=Android](http://shearch.herokuapp.com/?speakers=Reto%20Meier&title=Android)

More complex stuff works too:
[shearch.herokuapp.com?(title=Android Wear|description=Android
Wear)&speakers=Reto](http://shearch.herokuapp.com/?(title=Android%20Wear%7Cdescription=Android%20Wear)&speakers=Reto)
[shearch.herokuapp.com?(title=Android Wear|description=Android
Wear)&speakers=[Reto,Wayne]](http://shearch.herokuapp.com/?(title=Android%20Wear%7Cdescription=Android%20Wear)&speakers=[Reto,Wayne])
[shearch.herokuapp.com?title="Android
Wear"|title=WebRTC](http://shearch.herokuapp.com/?title=%22Android%20Wear%22%7Ctitle=WebRTC)
[shearch.herokuapp.com?(title=Android Wear|description=Android
Wear)&speakers=Timothy](http://shearch.herokuapp.com/?(title=Android%20Wear%7Cdescription=Android%20Wear)&speakers=Timothy)

Fuzzy matching — with apologies to Wayne :):
[shearch.herokuapp.com?speakers=pekarsky~](http://shearch.herokuapp.com/?speakers=pekarsky~)

For dates, use 'from' and 'to', which can cope with anything Date can handle:
[shearch.herokuapp.com?from=Feb](http://shearch.herokuapp.com/?from=Feb) // assumes text-only is a
month this year
[shearch.herokuapp.com?from=April 2014](http://shearch.herokuapp.com/?from=April%202014)
[shearch.herokuapp.com?from=2013-03-01&to=2013-05-01](http://shearch.herokuapp.com/?from=2013-03-01&to=2013-05-01)
[shearch.herokuapp.com?from=2013&to=2014](http://shearch.herokuapp.com/?from=2013&to=2014) //
midnight, 1 January to midnight, 1 January

Get total for any quantity field — this query returns the total number of views
for all videos:
[shearch.herokuapp.com?count=views](http://shearch.herokuapp.com/?count=view)

Get total for any query and quantity field:
[shearch.herokuapp.com?speakers=butcher&count=views](http://shearch.herokuapp.com/?speakers=butcher&count=view)

Get all individual values for any quantity field for all videos — returns an
object keyed by amounts, values are number of occurrences for each amount:
[shearch.herokuapp.com?countall=views](http://shearch.herokuapp.com/?count=view)

Get all individual values for any quantity field for any query:
[shearch.herokuapp.com?speakers=reto&countall=views](http://shearch.herokuapp.com/?speakers=reto&countall=view)

Build a chart from results (views for videos that mention 'Chrome'):
[simpl.info/s/chart.html](http://simpl.info/s/chart.html)


## The code

[Issues](https://github.com/GoogleChrome/dev-video-search/issues) and pull requests welcome.

There are three code directories:

###[app](https://github.com/GoogleChrome/dev-video-search/tree/master/src/app)
The web client (as used at [simpl.info/s](https://simpl.info/s)). This will automatically choose the local Node middle layer (below) if run from localhost.

### [get](https://github.com/GoogleChrome/dev-video-search/tree/master/src/get)
Middle layer Node app to get data from the database. For testing, you can run
this locally with the app running from localhost. The live version is on
[Nodejitsu](https://www.nodejitsu.com/) at shearch.herokuapp.com, for queries like this:
[shearch.herokuapp.com?captions=svg&speaker=alex](http://shearch.herokuapp.com/?captions=svg&speaker=alex)
(same as [shearch.herokuapp.com?c=svg&s=alex](http://shearch.herokuapp.com/?c=svg&s=alex)).

###[put](https://github.com/GoogleChrome/dev-video-search/tree/master/src/put)
Node app to get YouTube data and transcripts, massage the response and put it in
a CouchDB database at [cloudant.com](https://cloudant.com/).


## FAQs

### Why didn't you use Firebase?

Cloudant has Lucene search built in, and is based on CouchDB, which is easy to use from Node.

Firebase can now be used with Elasticsearch, but at the start of the project required extra installation.

### Why didn't you just use MySQL or …

An SQL database with Lucene for full text search might have been more appropriate than CouchDB.

(This kind of search is actually much easier with Firebase now.)

### How was CouchDB?

Good in some ways, and quick. In particular, the JSON/HTTP/REST styles feels
fits well with Node/JavaScript development.

Problems came with full text search:

* Full text search is not built into CouchDB, though it can be added on with
Lucene or other search engines.
* CouchDB searches return entire documents, with no 'partial' results. (In my
case, a document represents all data for a video.) So, for example, to
return only captions that include 'Android Wear', it's necessary to retrieve all the
documents (in their entirety) that have captions that mention 'Android Wear'
then filter.
* CouchDB search queries cannot be combined: for example, 'get me all videos
from 2013 with WebRTC in the title'. So, again, you have to add your own filter.

### How big is the database?

Around 250MB, but more like 150MB without transcripts: the transcript for each
document is really just a convenience to make it quick and simple to retrieve
human readable transcripts, and replicates the captions (with a few tweaks).

### How often is the data updated?

At present the database is updated manually to avoid code changes breaking it.

### Why didn't you use io.js?

No big reason. Node.js has been around longer.

### How many videos have transcripts?

When the repo was created: 4312 videos, 3550 with transcripts.

### How did you get the speaker names?

With a bit of sneaky regexing these are parsed from transcripts.
NB: speaker names are not parsable for many captions, so speaker search results
may not always be complete.

### Why are caption matches returned as span elements?

The primary use for the caption matches is within HTML markup. Returning JSON
for each span might be neater and less verbose, but for most apps that would
entail extra effort transforming to HTML.

### How long does it take to store and index data?

This depends a lot on connectivity. From work, the app gets and inserts the
video data and transcripts in under three minutes. From home, it takes about 10
minutes.

Indexing takes about 10 minutes.

### What build tools do you use?

JSCS and JSHint with grunt and githooks to force validation on commit.

Chrome JSON formatting extensions, [pro.jsonlint.com](https://pro.jsonlint.com/)
and [regex101.com](https://regex101.com/) were very useful.


## TODO

* General code refactoring.
* Unit tests.
* Better error handling.
* Better Node socket handling: a lot of the code
  is deliberately synchronous to avoid errors.
* The shearch.herokuapp.com API is HTTP only as yet.
* Use the official [YouTube Captions API](https://developers.google.com/youtube/v3/guides/implementation/captions).
* Move to Firebase. When the project started it was a bit tricky to implement
  full-text search with Firebase, so Cloudant was chosen (which has full text search built in). It's now pretty simple to use
  Firebase with ElasticSearch, so the data will be ported at some stage.
* Database updates are done manually at the moment — mostly to avoid messing up the sample app. Easily automated.


## License

Copyright 2015 Google, Inc.

Licensed to the Apache Software Foundation (ASF) under one or more contributor license agreements. See the NOTICE file distributed with this work for additional information regarding copyright ownership. The ASF licenses this file to you under the Apache License, Version 2.0 (the “License”); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an “AS IS” BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.

Please note: this is not a Google product.
