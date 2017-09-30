# hugo-fabric
Hugo Fabric Theme, forked from https://github.com/wd/hexo-fabric.

![hugo-fabric screenshot](https://raw.githubusercontent.com/wd/hugo-fabric/master/images/tn.png)

# Features

* Support archives (But archives page and tags page didn't support pagination :( )
* Tags list
* RSS link and social account links
* Disqus support
* Use Highlight.js for code highlight

# Installation

First clone this repository in the `themes/` directory:

```
$ cd themes/
$ git clone https://github.com/wd/hugo-fabric
```

Second, specify `hugo-fabric` as your default theme in the config.toml file. Just add the line

```
theme = "hugo-fabric"
```

Please check the `exampleSite` directory for an example site.

# Hugo settings

Set rss link name, default is rss.xml.

```
[outputs]
home = [ "HTML", "RSS" ]

[outputFormats]
[outputFormats.RSS]
mediatype = "application/rss"
baseName = "atom"
```

# Theme settings

Put settings below into your config.toml.

```
[params]
  author = "wd"
  [params.theme]
    subtitle = "happy every day"
    post_type = "page" # For archive
    archive_post_type = "archives"

    # According to https://discuss.gohugo.io/t/how-to-access-the-top-level-rsslink-from-a-post/2044, we have to set this ourself
    site_rsslink = "atom.xml"

    # social account
    github_user = "wd"
    twitter_user = "wd"
    disqus_shortname = "wdicc"

    # post sharing
    facebook_like = true
    twitter_tweet_button = true
    google_plus_one = true
    google_plus_one_size = "midum"
    addthis_profile_id = "wd"
```

# Favicon

There is a default favicon with this theme, you may want to change it. Just put it at `themes/hugo-fabric/static/images/fav.ico`.

# Code highlight

If you want to change to your favourite highlight style, just download the css file and replace `themes/hugo-fabric/static/css/hljs.css`. Since all languages package are too big, the CDN version only include 23 languages support. If you want more languages, please download a custome version of highlightjs and modify `layouts/partials/head.html`.

# Archive support

Create a new file `hugo new archives.md`, and edit this file, add the following line in front matter.

```
type = "archives"
```

# Todo

* TOC support

# Others

* https://github.com/wd/hexo2hugo
* https://discuss.gohugo.io/t/blog-archives-page/2577/17
