---
layout: category-page
---
{% for post in site.categories['events'] limit: 10 %}
<section>
    <div class="inner">
        <header class="major">
            <h2><a href="{{ post.url | absolute_url }}">{{ post.title }}</a></h2>
        </header>
        <p>
            {{ post.content | strip_html | truncatewords: 100 }}
        </p>
        <p>
            <strong>{{ post.date | date_to_string }}</strong>
            <ul class="actions">
                <li><a class="button next" href="{{ post.url | absolute_url }}">Read more</a><li>
            </ul>
        </p>
    </div>
</section>
{% endfor %}
