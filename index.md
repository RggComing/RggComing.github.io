---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: iOS development blog
description: iOS 开发记录
---

<h2>{{ page.title }}</h2>
<p>iOS开发记录</p>
<ul>
　　{% for category in site.categories %}
	<h2>{{ category | first }}</h2>
	<span>{{ category | last | size }} 篇文章</span>
	<ul class="arc-list">
		{% for post in category.last %}
			<li>{{ post.date | date:"%d/%m/%Y"}}<a href="{{ post.url }}">{{ post.title }}</a></li>
		{% endfor %}
	</ul>
	{% endfor %}
</ul>
