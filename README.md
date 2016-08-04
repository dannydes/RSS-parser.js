# Purpose
To make migrating from RSS feed to JSON-based API as seemless as possible.

# Methods

## Constructor - Feed( [source] )
initializes the <code>items</code> property

### Parameters

#### [source]
* If a string, it is treated as an RSS string and passed to the <code>parse()</code> method.
* If an object, it is treated as such, mapping its <code>items</code> property to that of an RSS.js Feed.
* If ommitted, an empty <code>items</code> array is created.

## Feed.parse( xml )
parses RSS string and sets the <code>items</code> property

### Parameters

#### xml
RSS string

### Example usage
``` javascript
var feedInfo = new Feed( '<?xml version="1.0" encoding="UTF-8" ?> <rss version="2.0"> <channel> <title>RSS Title</title>\
	<description>This is an example of an RSS feed</description> <link>http://www.someexamplerssdomain.com/main.html</link>\
	<lastBuildDate>Mon, 06 Sep 2010 00:01:00 +0000 </lastBuildDate> <pubDate>Mon, 06 Sep 2009 16:20:00 +0000 </pubDate> <ttl>\
	1800</ttl> <item> <title>Example entry</title> <description>Here is some text containing an interesting description.\
	</description> <link>http://www.wikipedia.org/</link> <guid>unique string per item</guid> <pubDate>Mon, 06 Sep 2009\
	 16:20:00 +0000 </pubDate> </item> </channel> </rss>' );
console.log( feedInfo.items[0].title );
```

Sample RSS taken from Wikipedia
