---
layout: page
title: Schedule
---

# U.S. Centers for Disease Control and Prevention

[Recommendations from the CDC](http://www.cdc.gov/vaccines/parents/downloads/parent-ver-sch-0-6yrs.pdf) are summarized as follows:

## By vaccine

<table>
    <tr>
        <th>Vaccine</th>
        <th>Diseases</th>
        <th>When</th>
    </tr>
    {% for v in site.data.vax %}
    <tr>
        <td>{{ v.name }}</td>
        <td>{% for d in v.diseases %}<a href="{{ site.baseurl }}/diseases/#{{ d|slugify }}">{{ d }}</a>{% if forloop.last == false %}, {% endif %}{% endfor %}</td>
        <td><ol>{% for s in v.schedule %}<li>{{ s }}</li>{% endfor %}</ol></td>
    </tr>
    {% endfor %}
</table>
