---
layout: page
permalink: /first
title: "Student Projects: The First Year"
---

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Duis ultricies lacus sed turpis tincidunt id. In est ante in nibh mauris cursus. Nibh venenatis cras sed felis eget velit. Ultricies leo integer malesuada nunc vel risus. Eleifend mi in nulla posuere. Ipsum dolor sit amet consectetur adipiscing elit pellentesque. Leo duis ut diam quam nulla porttitor. Tincidunt eget nullam non nisi est sit amet facilisis magna. Ridiculus mus mauris vitae ultricies leo. Ac ut consequat semper viverra. Sed libero enim sed faucibus turpis in. Eu scelerisque felis imperdiet proin fermentum leo vel orci porta. Nunc consequat interdum varius sit.

## Table of Contents

{% assign projects = site.projects | where: 'layout','projects' %}

<ul class ="toc">
{% for project in projects %}
    <li><a href="#{{ project.label | slugify }}">{{ project.label }}</a> by {{ project.author }}</li>  
{% endfor %}
</ul>

{% for project in projects %}

<hr/>

  <div  class='exhibit-meta'>
    <h2 class='exhibit-title' id='{{ project.label | slugify }}'>{{ project.label }}</h2>
    <span class='exhibit-author'>by <em>{{ project.author }}</em></span>
  </div>

{% include reduced_parallax_image.html collection='projects' pid=project.pid y='50%' %}

{% capture text %}
{% include projects/{{project.pid}}.md %}
{% endcapture %}

  <div>{{ text | markdownify }}</div>

{% endfor %}
