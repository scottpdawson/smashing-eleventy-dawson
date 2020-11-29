---
title: Events
metaDescription: This is a sample meta description. If one is not present in your page/post's front matter, the default metadata.description will be used instead.
hero: /static/img/events.jpg
permalink: /events/index.html
eleventyNavigation:
  key: Events
  order: 2
---

Want to hear me play? Here are some upcoming events!

<table>
    <thead>
        <tr>
            <th>Date</th>
            <th>Title</th>
            <th>Location</th>
        </tr>    
    </thead>
    <tbody>
{%- for post in collections.events -%}
        <tr>
            <td>{{ post.date | readableDate }}</td>
            <td><a href="{{ post.url }}">{{ post.data.title }}</a></td>
            <td>{{ post.data.location }}</td>
        </tr>    
{%- endfor -%}
    </tbody>
</table>
