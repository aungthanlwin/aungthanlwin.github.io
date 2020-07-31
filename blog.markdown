---
layout: page
title: PERSONAL BLOG
permalink: /blog/
---
<div class="row">
  {% for post in site.posts limit:3 %}
  <div class="col-md-4">
    <a href="{{ BASE_PATH }}{{ post.url }}">
    <h2>{{ post.title | truncate:24 }}
    </h2>
    </a>
	<hr />
	<p>{% if post.thumbnail %}
	<img src="{{ post.thumbnail }}" style="height: 100%; width:100%;" align="center" />
	{% else %}
	<img src="/images/nothumbnail.png"
  style="height: 100%; width: 100%;" align="center" />
	{% endif %}</p>
	<p>&nbsp;</p>
	<p>
	{{ post.content | strip_html | truncatewords:20 }}
	</p>
	<p>
	<a class="btn" href="{{ BASE_PATH }}{{ post.url }}">Read more...</a>
	</p>
  </div>
  {% endfor %}
</div>

{% for post in site.posts limit:15 offset:3 %}
<hr />
<div class="row">
  <div class="col-md-6" style ="margin: 0 0 0 0; padding: 0 0 0 0">
    {% if post.thumbnail %}
	<img src="{{ post.thumbnail }}" style="height: 50%; width:50%;" align="center" />
	{% else %}
	<img src="/images/nothumbnail.png" style="height: 50%; width:50%;" align="center" />
	{% endif %}
  </div>
  <div class="col-md-6" style ="margin: 0 0 0 0; padding: 0 0 0 0; ">
    <p><a href="{{ BASE_PATH }}{{ post.url }}"><h3>{{ post.title }}</h3></a></p>
	<p>{{ post.content | strip_html | truncatewords: 40 }}
	</p>
  </div>
</div>
{% endfor %}
