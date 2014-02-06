# Purpose
To make migrating from RSS feed to JSON-based API as seemless as possible.

# Methods

## init( xml )
starts the parsing process

### Returns
array of RSS items

### Parameters

#### xml
XML string

### Example usage
<code>
var feedInfo = RSSParser.init( '<?xml version="1.0" encoding="UTF-8" ?> <rss version="2.0"> <channel> <title>RSS Title</title> <description>This is an example of an RSS feed</description> <link>http://www.someexamplerssdomain.com/main.html</link> <lastBuildDate>Mon, 06 Sep 2010 00:01:00 +0000 </lastBuildDate> <pubDate>Mon, 06 Sep 2009 16:20:00 +0000 </pubDate> <ttl>1800</ttl> <item> <title>Example entry</title> <description>Here is some text containing an interesting description.</description> <link>http://www.wikipedia.org/</link> <guid>unique string per item</guid> <pubDate>Mon, 06 Sep 2009 16:20:00 +0000 </pubDate> </item> </channel> </rss>' );
</code>

Sample RSS taken from Wikipedia
