---
layout: about
title: about
permalink: /
description: Giving machines the ability to see

profile:
  align: right
  image: prof_pic.jpg

news: false  # includes a list of news items
selected_papers: false # includes a list of papers marked as "selected={true}"
social: true  # includes social icons at the bottom of the page
---

Hey! I am a final year electronics undergrad student at Veermata Jijabai Technological Institute ([VJTI](https://vjti.ac.in/)). Throughout my undergrad I have explored many fields be it Robotics, Computer Vision, Data Science etc. The one that struck with me is Computer Vision. 

The thing that fascinates me the most is how humans are able to percieve the environment through visual sensory organs and specially how babies are able to interpret this information and learn. The long-term goal is to emulate the same behviour in machines specially in self-driving cars.

Currently, I am working on deepfakes detection as part of my undergrad thesis. Previously, I have worked a lot in the field of video analytics through internships and personal projects.

I am open for opportunities in the field of computer vision and robotics. 

<br>

# Experience

{% for experience in site.data.experience %}
<div>
    {% if experience.title %}
    <h4 class="title font-weight-bold">{{experience.title}}</h4>
    {% endif %}
    {% if experience.role %}
    <h6 class="title font-weight-bold">{{experience.role}}</h6>
    {% endif %}
    {% if experience.year %}
    <span class="badge bg-dark font-weight-bold">
        {{ experience.year }}
    </span>
    {% endif %}
    {% if experience.description %}
        <ul class="items">
            {% for item in experience.description %}
                <li>
                    {% if item.contents %}
                        <span class="item-title">{{ item.title }}</span>
                        <ul class="subitems">
                        {% for subitem in item.contents %}
                            <li><span class="subitem">{{ subitem }}</span></li>
                        {% endfor %}
                        </ul>
                    {% else %}
                        <span class="item">{{ item }}</span>
                    {% endif %}
                </li>
            {% endfor %}
        </ul>
    {% endif %}
    {% if content.items %}
        <ul class="items">
            {% for item in content.items %}
                <li>
                    {% if item.contents %}
                        <span class="item-title">{{ item.title }}</span>
                        <ul class="subitems">
                        {% for subitem in item.contents %}
                            <li><span class="subitem">{{ subitem }}</span></li>
                        {% endfor %}
                        </ul>
                    {% else %}
                        <span class="item">{{ item }}</span>
                    {% endif %}
                </li>
            {% endfor %}
        </ul>
    {% endif %}
</div>
{% endfor %}