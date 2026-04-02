---
permalink: /
title: "Biography"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
{% include base_path %}

<div id="biography"></div>

I am a Postdoctoral Research Fellow in Cheng Kar-Shun Robotics Institute (CKSRI) and Department of Electrical and Computer Engineering, the Hong Kong University of Science and Technology (HKUST), collaborating with [Prof. Fumin Zhang](https://fumin-home.hkust.edu.hk/).

I obtained my Ph.D. degree in Robotic Engineering from the Harbin Institute of Technology (Shenzhen), under the supervision of [Prof. Xin Wang](https://homepage.hit.edu.cn/wangxin). From 2023 to 2024, I had joint training at the Chair of Robotics, AI, and Real-Time Systems at the Technical University of Munich, Germany, working under the guidance of [Prof. Alois Knoll](https://www.professoren.tum.de/en/knoll-alois-christian/). I received National Scholarships for Graduate Students in 2020 and 2024 and won the Best Paper Award at the 18th International Conference on Intelligent Robotics and Applications (ICIRA 2025).

My research interests are centered on marine robotics, robotic vision, and deep reinforcement learning. Welcome to contact me for academic collaboration in the field of marine robotics at eelinhong@ust.hk.

<h2 id="news">News</h2>

- **03/26** 👏👏👏 One paper was accepted by **OCEANS 2026** as an oral paper. I will present it in Sanya.
- Example: One paper accepted by **Conference/Journal Name**, 2026.
- Example: Started as a Postdoctoral Research Fellow at **HKUST**, 2025.

<h2 id="publications">Publications</h2>

{% if site.author.googlescholar %}
<div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% if site.publication_category %}
  {% for category in site.publication_category %}
    {% assign title_shown = false %}
    {% for post in site.publications reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      {% unless title_shown %}
<h3>{{ category[1].title }}</h3>
<hr />
        {% assign title_shown = true %}
      {% endunless %}
      {% include archive-single.html %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}

<h2 id="talks">Talks</h2>

{% if site.talkmap_link == true %}
<p><a href="/talkmap.html">See a map of all the places I've given a talk.</a></p>
{% endif %}

{% for post in site.talks reversed %}
  {% include archive-single-talk.html %}
{% endfor %}

<h2 id="teaching">Teaching</h2>

{% for post in site.teaching reversed %}
  {% include archive-single.html %}
{% endfor %}

<h2 id="services">Services</h2>

- Add your professional services here.
- Example: Reviewer for **IEEE T-RO / ICRA / IROS**.
- Example: Session chair / organizer / committee member.
