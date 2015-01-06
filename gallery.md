---
layout: page
description: "Gallerie"
header-img: "img/gvsg.jpg"
---

<script src="//ajax.googleapis.com/ajax/libs/jquery/1.11.2/jquery.min.js"></script>
<script src="/js/lightbox.min.js"></script>
<link href="/css/lightbox.css" rel="stylesheet" />

<p>Ho-Ho-Hearthstone Gallerie</p>

{% for gallery in site.data.galleries %}
	<h1>{{ gallery.description }}</h1>
	<ol>
		{% for image in gallery.images %}
			<li>
				{{ image.text }}<br>
				<a href="{{ gallery.imagefolder }}/{{ image.name }}" data-lightbox="{{ gallery.id }}" title="{{ image.text }}">
					<img src="{{ gallery.imagefolder }}/{{ image.thumb }}">
				</a>
			</li>
		{% endfor %}
	</ol>
{% endfor %}

<p>default footer for all gallery pages</p>
