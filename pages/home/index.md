---
title: 
sidebar: home_sidebar
permalink: index.html
toc: false
---

<img src="{{ "images/AVsitterPlus-Logo.png" }}">
<br><br>
Welcome to the instructions for the AVsitterPlus&trade; pose system, as available in Second Life<sup>&reg;</sup>.

The AVsitterPlus scripts are available <a href="https://github.com/missyrestless/AVsitterPlus">here on GitHub</a> and licensed under the <a href="https://www.mozilla.org/en-US/MPL/2.0/">Mozilla Public License, Version 2.0</a>.

The AVsitterPlus Documentation covers the following topics:

- <a href="/avsitterplus_home.html">AVsitterPlus instructions</a>.
- <a href="/contribute.html">AVsitterPlus contributor guidelines</a>.
- <a href="/support.html">AVsitterPlus support options</a>.

<br>
The AVsitterPlus scripts can be freely obtained from the <a href='{{ site.script_github }}'>GitHub repository</a>; however if you would like to receive packaged versions of the latest release, and receive <a href='/updates.html'>in-world updates</a> of future releases, visit <a href='{{ site.marketplace }}'>SL Marketplace</a>.

Proceeds are shared with open-source contributors and will help support continued development of AVsitterPlus. Those who purchased AVsitterPlus in the past will continue to receive <a href="/updates.html">in-world updates</a> without needing to purchase it again.

# Latest News

<div class="post-list">
        {% for post in site.posts limit:3 %}


    <h2><a class="post-link" href="{{ post.url | remove: "/" }}">{{ post.title }}</a></h2>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }} /
            {% for tag in post.tags %}

                <a href="{{ "tag_" | append: tag | append: ".html"}}">{{tag}}</a>{% unless forloop.last %}, {% endunless%}

                {% endfor %}</span>
        <p>{% if page.summary %} {{ page.summary | strip_html | strip_newlines | truncate: 160 }} {% else %} {{ post.content | truncatewords: 50 | strip_html }} {% endif %}</p>

        {% endfor %}

        <p>
        <a href="feed.xml" class="btn btn-primary navbar-btn cursorNorm" role="button">RSS Subscribe{{tag}}</a>
        <br>
        See more posts from the <a href="news_archive.html">News Archive</a>.
        </p>

</div>
