---
layout: default
title: HODOR-BLOG
description: aardio-文章列表
---

<ul>
  {% for post in site.posts %}
    <li>
      <a href="/aardio{{ post.url }}">{{ post.description }}--{{ post.url }}</a>
    </li>
  {% endfor %}
</ul>
<nav class="pagination" role="navigation">
    {% if paginator.previous_page %}
    <a class="previous pagination__newer btn btn-small btn-tertiary" href="{{ paginator.previous_page_path }}">&larr; 上一页</a>
    {% endif %}
    <span class="page_num pagination__page-number">{{ paginator.page }} / {{ paginator.total_pages }}</span>
    {% if paginator.next_page %}
    <a class="next pagination__older btn btn-small btn-tertiary" href="{{ paginator.next_page_path }}">下一页 &rarr;</a>
    {% endif %}
</nav>
