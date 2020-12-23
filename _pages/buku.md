---
layout: page
title: Kumpulan Buku Sekolah Elektronik (BSE)
description: Halaman ini berisi kumpulanBuku Sekolah Elektronik (BSE) SD, SMP, SMA, dll terdiri dari buku guru, buku siswa, komik pendidikan yang sangat berguna bagi para pembaca.
permalink: /bse
pagination: 
  enabled: true
  category: buku
  permalink: /:num/
---

<div class="row mt-3">
<div class="col-md-8 main-loop">
<h4 class="font-weight-bold spanborder"><span>Kategori Buku</span></h4>
{% for post in paginator.posts %}
{% include main-card.html %}
{% endfor %} 
<div class="mt-5">
   {% if paginator.total_pages > 1 %}
  <ul class="pager">
      {% if paginator.first_page %}
      <li class="previous left">
          <a href="{{ paginator.first_page_path | prepend: site.baseurl | replace: '//', '/' }}">First</a>
      </li>
      {% endif %}
      {% if paginator.previous_page %}
      <li class="previous">
          <a href="{{ paginator.previous_page_path | prepend: site.baseurl | replace: '//', '/' }}" title="Halaman Sebelumnya"><span class="glyphicon glyphicon-chevron-left"></span></a>
      </li>
      {% endif %}
      {% if paginator.page_trail %}
        {% for trail in paginator.page_trail %}
          <li {% if page.url == trail.path %}class="disabled"{% endif %}>
              <a href="{{ trail.path | prepend: site.baseurl | replace: '//', '/' }}" title="{{trail.title}}">{{ trail.num }}</a>
          </li>
        {% endfor %}
      {% endif %}
      {% if paginator.next_page %}
      <li class="next">
          <a href="{{ paginator.next_page_path | prepend: site.baseurl | replace: '//', '/' }}" title="Halaman Selanjutnya"><span class="glyphicon glyphicon-chevron-right"></span></a>
      </li>
      {% endif %}
       {% if paginator.last_page %}
      <li class="previous last">
          <a href="{{ paginator.last_page_path | prepend: site.baseurl | replace: '//', '/' }}">Last</a>
      </li>
      {% endif %}
  </ul>
  {% endif %}
        </div>
    </div></div>
