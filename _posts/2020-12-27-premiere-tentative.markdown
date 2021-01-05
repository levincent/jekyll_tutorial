---
layout: post_vincent
title:  "Première tentative"
date:   2020-12-27 16:26:06 -0500
categories: jekyll super-public
tags: superbes vacances superbes-vacances
author: Vinnie
---

[mon essai de screenshot](/assets/test/IMG_1423.JPG)

<h3>liste des posts du site en cours</h3>

<ul>
{% for post in site.posts %}
<li>
<a href="{{ post.url }}">{{ post.title }}</a>
</li>
{% endfor %}
</ul>

<h3>liste des tags du site en cours:</h3>


<ul>
{% for tag in site.tags %}
  <h4>{{ tag[0] }}</h4>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
</ul>

<h3>liste des tags de la page en cours</h3>


{% for tag in page.tags %}

<li> {{ tag }} </li>

{% endfor %}


<hr>

<h3>Essai de data file </h3>

{% for experience in site.data.experiences %}

<li>{{ experience.company }}: {{ experience.occupation }}

{% endfor %}

<hr>

<h3>Tuto 18: static files </h3>

{% for file in site.static_files %}
{% if file.image %}
<img src="{{ file.path }}" alt="{{ file.name }}"> 
{% endif %}
{% endfor %}