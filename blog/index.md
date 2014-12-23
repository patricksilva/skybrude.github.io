---
title: Skybrude Consulting, LLC - Blog
layout: default
titlehead: Skybrude Blog
---



<div class="container bs-docs-container">
<div class="bs-docs-section">
<h1 class="page-header">Latest Entries</h1>


<table class="listing">
{% for post in site.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <tr><td class="listing-seperator">{{ y }}</td></td></tr>
  {% endif %}
  <tr>
  <td class="listing-item">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time></td>
    <td class="listing-item"><a href="{{ site.url }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></td>
  </tr>
{% endfor %}
</table>

</div>
</div>
