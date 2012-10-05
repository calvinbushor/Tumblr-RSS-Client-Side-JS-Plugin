Tumblr-RSS-Client-Side-JS-Plugin
================================

Fetch an RSS feed from a given tumblr url and parse it using a client side JavaScript plugin.

@requires jQuery v1.8.*

Installation
Put tumblr-rss.js before the end body script tag in your page.

<script src="/javascripts/tumblr-rss.js"></script>

Start the script by creating a new instance of the tumblr Object.

var tumblr = new TumblrRSS(selector, url, posts);

selector: The jQuery selected element(s) you want to replace with the parsed rss.
url: The url to the tumblr blog.
posts: How many posts you want to parse and display.

Run the script by calling .start() on the tumblr Object you created.
tumblr.start();

Example:
Fetch the RSS feed from the tumblr blog at the url defined in the second parameter. The script will parse one post into html and the elements that match the class blogroll will be updated with the generated HTML.

var tumblr = new TumblrRSS($('.blogroll'), 'http://calvinbushor.tumblr.com/', 1);
tumblr.start();

