---
layout: page
title: Confs
permalink: /confs/
description: Configurations for your every day life
---

{% for file in site.static_files %}
  {% if file.path contains '/confs' %}
    {% highlight bash %}
{% include_relative {{file.path | slice: 1, 100}} %}
    {% endhighlight bash %}
  {% endif %}
{% endfor %}
