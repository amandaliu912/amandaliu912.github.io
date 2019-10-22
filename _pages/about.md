---
title: "About"
permalink: /About/
header:
  image: "/images/pic04.jpg"

I am business analyst, looking for opportunities in data science field.
I have first Master degree in Accountancy,
and I just got second Master degree in Analytics.
I am a self-starter, quick learner and a problem solver,
who excels at exploratory analysis and machine learning.

---
{% include base_path %}
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
