# Oishi

A hexo theme based on [Landscape plus](https://github.com/xiangming/landscape-plus) 

## Demo

[Antônio Carlos](http://acfreitas.com/)

## Usage

``` bash
$ git clone https://github.com/acfreitas/oishi.git themes/oishi
```
## Requirements

Hexo 2.7+ 

## Configure

_config.yml

```yml
# Header
menu:
  Home: /
  Archives: /archives

# Content
excerpt_link: ...
fancybox: false

# Sidebar
sidebar: 
widgets:
- category
- tag
- tagcloud
- archive
- recent_posts
- links

# Links
links:

# Miscellaneous
google_analytics:
favicon: /favicon.png
twitter:
google_plus:
fb_admins: 
fb_app_id:

# Duoshuo
duoshuo_shortname: 

# Baidu share
baidushare: false

# scrollUp image
scrollUp: image

# social
social:
  github: https://github.com/username
```

## Translation

languages/default.yml

```yml
archive: Archives
categories: Categories
recent_posts: Recent
tags: Tags
tagcloud: Tag Cloud
links: Links
excerpt_link: More
share: Share
search: Search
prev: Prev
next: Next
comment: Comment
contents: Contents
page: Page %d
menu: Menu
rss: RSS
showsidebar: Show Sidebar
hidesidebar: Hide Sidebar
updated: Updated
```
layout/_partial/post/nav.ejs

```js

<% if (post.prev || post.next){ %>
<nav id="article-nav">
  <% if (post.prev){ %>
    <a href="<%- url_for(post.prev.path) %>" id="article-nav-newer" class="article-nav-link-wrap">
      <strong class="article-nav-caption">Recent</strong>
      <div class="article-nav-title">
        <% if (post.prev.title){ %>
          <%= post.prev.title %>
        <% } else { %>
          (no title)
        <% } %>
      </div>
    </a>
  <% } %>
  <% if (post.next){ %>
    <a href="<%- url_for(post.next.path) %>" id="article-nav-older" class="article-nav-link-wrap">
      <strong class="article-nav-caption">Older</strong>
      <div class="article-nav-title"><%= post.next.title %></div>
    </a>
  <% } %>
</nav>
<% } %>
```

## Icons

source/logo.png
and 
source/favicon.ico

## More information

* [Read the documentation](http://hexo.io/)
* [See the theme list](https://github.com/hexojs/hexo/wiki/Themes)
