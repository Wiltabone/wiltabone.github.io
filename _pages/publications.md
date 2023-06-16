---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% assign publications = site.publications | sort: "year" | reverse %}
{% for pub in publications %}
<div class="pubitem">
  <div class="pubteaser">
  <a href="/download/{{pub.slug}}.pdf">
    <img
      src="/images/publication-pages/{{ pub.slug }}_small.jpg"
      alt="{{pub.slug}} publication teaser"
    />
  </a>
  </div>
    <div class="pubtitle">{{ pub.title }}</div>
    <div class="pubauthors">{{ pub.authors }}</div>
    <div class="pubinfo">{{ pub.publication }}, {{ pub.year}}</div>
    <div class="publinks">
    <a href="/download/{{pub.slug}}.pdf"><i class="fa fa-file-pdf"></i></a
    >&nbsp;&nbsp;
    <a href="{{pub.doi}}"><i class="fas fa-external-link-alt"></i></a>
  </div>
</div>
{% endfor %}
