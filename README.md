KickAss API
========
Web scraper for kickass.to

Currently supports 3 methods

`getAllShows(cb)` Returns an object array of all TV Shows on kickass.to/tv/show/ in the form `{show: showname, slug: kat-slug, provider: 'kickass'}`

`getAllEpisodes(data, cb)` Data is JSON object same as one returned in `getAllShows` returns multi-dimensional array with magnet URL string in the form `episodes[season][episode]`

`cb` is the callback function passed to the methods and will be of the form `function cb(error, result)`

IMPORTANT
==============
This is not meant for constant use due to the amount of requests made to the KickAss site. This is mainly to build an initial database of shows and episodes. [The hourly and daily dumps](http://kickass.to/api/) can then be used once the db is set up.