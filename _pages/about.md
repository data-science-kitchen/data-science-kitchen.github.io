---
layout: page
permalink: /
title:
nav:
news: true  # includes a list of news items
---

<div class="text-center mt-5">
  <img class="img-fluid" src="{{ 'dsk-logo.png' | prepend: '/assets/img/' | prepend: site.baseurl }}">
</div>

<div class="col mt-4">
  <h3 class="title text-center font-weight-bold">Machine learning, delivered fresh from the oven</h3>
</div>

<div class="col mt-4">
  <h3 class="title text-center font-weight-bold"></h3>
</div>

<div class="col text-justify p-0">
We are a group of data science and machine learning enthusiasts, doing open source research for fun in our free time. Founded in November 2020, our objective is to publish interesting machine learning research, learn from each other and continuously develop our data science skillset. We particularly enjoy participating in machine learning challenges and competitions. Our research interests primarily focus on natural language processing and explainable machine learning, but we do not limit ourselves to these subject areas and are generally open to ideas from a broad range of application domains.
<br/><br/>
</div>

<div class="news">
  <h2>news</h2>
  {% if site.news  %}
    <div class="table-responsive">
      <table class="table table-sm table-borderless">
      {% assign news = site.news | reverse %}
      {% for item in news limit: site.news_limit %}
        <tr>
          <th scope="row">{{ item.date | date: "%b %-d, %Y" }}</th>
          <td>
            {% if item.inline %}
              {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
            {% else %}
              <a class="news-title" href="{{ item.url | relative_url }}">{{ item.title }}</a>
            {% endif %}
          </td>
        </tr>
      {% endfor %}
      </table>
    </div>
  {% else %}
    <p>No news so far...</p>
  {% endif %}
</div>

<!--
<div class="news mt-3 p-0">
  <h1 class="title mb-4 p-0">news</h1>
  {% assign news = site.news | reverse %}
  {% for item in news limit: site.news_limit %}
    <div class="row p-0">
      <div class="col-sm-2 p-0">
        <span class="badge info-color-dark font-weight-bold text-uppercase align-middle date ml-3">
          {{ item.date | date: "%b %-d, %Y" }}
        </span>
      </div>
      <div class="col-sm-10 mt-2 mt-sm-0 ml-3 ml-md-0 p-0 font-weight-light text">
        <p>{{ item.content | remove: '<p>' | remove: '</p>' | emojify }}</p>
      </div>
    </div>
  {% endfor %}
</div>
-->
