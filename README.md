mkttool
=======

Marketing tool which for a given blog it will crawl and gather information about blog articles metrics (such as words number, number of links, headings, etc)

The tool is incomplete because it is a side project to learn Ruby and Ruby on Rails.

The idea is to build a marketing tool that works for every blog. Given an URL, the tool should crawl all internall links, and for every link that represents an article it do some actions:

* counts number o words;
* counts number of links;
* counts number of headins;
* give number of shares on Facebook, Twitter and LinkedIn

Better, the tool should identify if the URL inserted by the user is or not a blog. It can be done by checking the pattern of blog structure (Wordpress, blogger and typepad has their own structure that can be found on 90%) 

This tool take some advantages of other technologies such as Anemone, Nokigiri and boilerpipe.

The data is stored using MongoDB.

All blogs inserted on database should be updated time by time. If a user insert an URL that not exists on database, the tool is using Resque to start 4 threads that will start the crawling process and store data on MongoDB.

There is a infinite scroll for data representation.

NOTE: Please understand, this tool is a way for me to start using Ruby and Ruby on Rails, so there is a lot of work to do.
