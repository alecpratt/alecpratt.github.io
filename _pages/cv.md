---
layout: page
permalink: /cv/
title: CV
nav: true
nav_order: 2
cv_pdf: example_pdf.pdf
description:
#toc:
#  sidebar: left
---


<p> A copy of my resume can be downloaded 
<a href="/assets/pdf/example_pdf.pdf" download="pratta_resume.pdf"><strong>here</strong></a>
. </p>

{% for section in site.data.mycv %}
  <h3> {{ section.section }} </h3>
  <hr>

  {% if section.type == "datedlist" %}
    <div class="contentRow">
      <div class="dataColumnL>
        <strong> {{ section.item }} </strong>, <em> {{ section.location }} </em>
      </div>

      <div class="dataColumnR" align="right">
        {% if section.startdate %}
          {{ section.startdate }} to
        {% endif %}
        {{ section.enddate }} 
      </div>


    </div>



  {% else %}


  {% endif %}

{% endfor %}