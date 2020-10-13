---
title: Blog Posts
pagination:
    data: collections.blog
    size: 2
    alias: blogs
---

{%- for blog in blogs %}
- [{{ blog.data.title }}]({{ blog.url }})
{%- endfor %}

{% if pagination.href.previous %}
	<a href="{{ pagination.href.previous }}">previous page</a>
{% endif %}
{% if pagination.href.next %}
	<a href="{{ pagination.href.next }}">next page</a>
{% endif %}
