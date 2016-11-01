---
layout: page
title: Members 
tagline: (as of September 2016)
group: navigation
---
{% include JB/setup %}

<table id="database-members" class="display" cellspacing="0" width="100%">
        <thead>
            <tr>
                <th>Name</th>
				<th>University / Company</th>
				<th>City</th>
				<th>Country</th>
            </tr>
        </thead>
        <tfoot>
            <tr>
                <th>Name</th>
				<th>University / Company</th>
				<th>City</th>
				<th>Country</th>
            </tr>
        </tfoot>
        <tbody>
            {% for member in site.members %}
                <tr>
                    {% if member.website == "#" %}
    				    <td>{{ member.name}}</td>
                    {% else %}
                        <td><a href="{{member.website}}">{{ member.name}}</a></td>
                    {% endif %}
    				<td>{{ member.university}}</td>    
    				<td>{{ member.city}}</td>
    				<td>{{ member.country}}</td>
                </tr>
			{% endfor %}
        </tbody>
    </table>
