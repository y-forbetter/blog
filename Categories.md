---
layout: page
title: Categories/Tags(标签)
---

{% for category in site.categories %}
<h3>{{ category | first }}{{'('}}{{category | last | size}}{{')'}}</h3>
<ul class="arc-list">
    {% for post in category.last %}
        <li><a href="{{ post.url | relative_url }}">{{ post.title}}</a>{{'('}}{{ post.date | date:"%Y/%M/%D"}}{{')'}}</li>
    {% endfor %}
</ul>
{% endfor %}