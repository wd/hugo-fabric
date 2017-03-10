# hugo-fabric
Hugo Fabric Theme, forked from https://github.com/wd/hexo-fabric. You can visit the live demo at https://wdicc.com.

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

# Theme settings

Put settings below into your config.toml.

```
[params]
  author = "wd"
  [params.theme]
    subtitle = "happy every day"
    post_type = "page" # For archive
    archive_post_type = "archives"

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

# Archive support

Create a new file `hugo new archives.md`, and edit this file, add the following line in front matter.

```
type = "archives"
```
