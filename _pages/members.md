---
layout: page
title: members
permalink: /members/
description: meet the chefs
nav: members
---

<div class="members">
  {% assign sorted_members = site.members | sort: "first_name" %}
    <div class="grid">
      {% for member in sorted_members %}
        {% include members.html %}
      {% endfor %}
    </div>
</div>

