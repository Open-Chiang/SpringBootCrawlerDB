# Java Crawler Setup

**Keywords**: Crawler4j, Jsoup, Spring Boot, Spring Data JPA, PostgreSQL, Multi-threading, Image crawler.

A Spring Boot web crawler setup/example:  crawler4j for crawling, Jsoup for parsing, Spring Data JPA as ORM, PostgreSQL or direct files output as persistence.

It will be crawling [pixabay.com](https://pixabay.com/) 800~p beautiful images as a working example.

I uploaded two versions: 

**CrawlerLocalFiles**: stores local image files in a folder.

**CrawlerWithDB**: this one can switch between three output modes: stores as local files, stores into PostgreSQL or does both. It's set by a keyword in the application.properties.


# Quick Installation

I included a fat jar(CrawlerLocalFiles) at the top level folder. Download it, you will need Java 8 jre, run `java -jar CrawlerLocalFiles.jar` in command line. You gonna see links flying through. A new folder named `images` will appears with freshly crawled jpgs in it. It will keep working till you hit exit `ctrl + c`, or crawled all the links follows the domain: https://pixabay.com/en/ (I have no idea how long it gonna take). 


## Side Node for pixabay.com

pixabay.com offers 4 sizes/tiers of images:

1. thumbnail 
2. around 800p  <==== We're getting this here, and only this.
3. around 1440p
4. 4k+

Tier 3 is behind a CAPTCHA; Tier 4 is behind authentication.


## Side Nodes of the crawler4j

Crawler4j doesn't crawl links in HTML attribute 'srcset', so I have to prase it with Jsoup and send that links back to the crawl pool. 


## Credits

[Tom H](http://www.saturnringstation.com/portfolio)

## Usage

Education only

## License

The MIT License
