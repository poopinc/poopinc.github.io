---
layout: page
title: About
permalink: /about/
---
<p class="text-justify">{{ site.description }}</p>
<h1 class="page-name">Team</h1>
<div class="spacing_settings">
<div class="row">


{% assign Employees = site.data.team %}
    {% for employee in Employees %}
        <div class="spacing_settings_controller">
        <div class="card mb-2" style="width: 18rem;">
        {% if employee.image_url %}
                <img src="{{ employee.image_url }}" class="card-img-top" alt="{{ employee.name }}">
        {% else %}
                <img src="https://thumbs.dreamstime.com/b/no-user-profile-picture-hand-drawn-illustration-53840792.jpg" class="card-img-top" alt="{{ employee.name }}">
        {% endif %}
            <div class="card-body">
            <h5 class="card-title">{{ employee.name }}</h5>
            <p class="card-text">{{ employee.job }}</p>
            <!-- Instagram Links -->
            {% if employee.instagram_user %}
                <a href="https://www.instagram.com/{{ employee.instagram_user }}" class="btn btn-dark btn-sm">Instagram</a>
            {% endif %}
            <!-- Twitter Links -->
            {% if employee.twitter_user %}
                <a href="https://twitter.com/{{ employee.twitter_user }}" class="btn btn-dark btn-sm">Twitter</a>
            {% endif %}
            </div>
        </div>
        </div>
        {% else %}
            <h1>no one work here</h1>
        {% endfor %}
</div>
</div>