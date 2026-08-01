---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
exclude: true
---
# Tom's Blog

{% for blogpost in site.categories.blog %}
{% assign mypost = blogpost.slug %}

- [{{ blogpost.date| date: "%Y-%m-%d" }} - {{ blogpost.title }}]({{ site.baseurl }}/blog/{{ blogpost.date| date: "%Y/%m/%d" }}/{{ blogpost.slug }}.html)
{% endfor %}