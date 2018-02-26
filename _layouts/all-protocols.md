---
layout: category-page
---
<section>
    <div class="inner">
        <table>
            <thead>
                <tr>
                    <td>Type</td>
                    <td>Date</td>
                    <td>Number of appendices</td>
                </tr>
            </thead>
            <tbody>
            {% for post in site.categories['protocols'] %}
                <tr>
                    <td><a href="{{ post.url | absolute_url }}">{{ post.type }}</a></td>
                    <td>{{ post.date | date_to_string }}</td>
                    <td>{{ post.appendices | size }}</td>
                </tr>
            {% endfor %}
            </tbody>
        </table>
    </div>
</section>
