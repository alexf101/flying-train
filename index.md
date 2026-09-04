---
layout: default
title: Driving the Flying Train
---

<div style="text-align: center; margin: 0 0 2rem;">
  <img src="{{ '/cover.jpeg' | relative_url }}" alt="Comic-style illustration: a determined pilot gripping the wheel of a flying steam train that loops through the clouds" style="max-width: 320px; width: 100%; border-radius: 6px; box-shadow: 0 8px 30px rgba(0,0,0,0.15), 0 2px 8px rgba(0,0,0,0.1);">
</div>

# Driving the Flying Train

*A guide for office workers on mastering AI workflows*

Are you a "Human in the Loop"? Learn to take control of the loop instead, driving your AI system from the front seat, where you belong.

**Alex Finkel** · with Brinley Hosking

---

We need to move from "human in the loop" to "human drives the loop." The difference matters: one makes you an approver, the other keeps you in charge.

This is a collection of ideas, models and practical techniques for getting more out of AI — built from real experience, not theory. It's written for people in offices and teams, not software engineers. Each chapter stands alone; read what's useful, skip what isn't.

## Chapters

{% assign sorted = site.chapters | sort: "order" %}
{% for ch in sorted %}
**{{ ch.order }}. [{{ ch.title }}]({{ ch.url | relative_url }})** · {{ ch.status }}

{{ ch.description }}

{% endfor %}
