# blog
<!DOCTYPE html>
{% load blog_tags %}
{% load static %}
<html lang="en" dir="ltr">
  <head>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" integrity="sha384-JcKb8q3iqJ61gNV9KGb8thSsNjpSL0n8PARn9HuZOnIxN0hoP+VmmDGMN5t9UJ0Z" crossorigin="anonymous">
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js" integrity="sha384-B4gt1jrGC7Jh4AgTPSdUtOBvfO8shuf57BaghqFfPlYxofvL8/KUEfYiJOMMV+rV" crossorigin="anonymous"></script>
<link rel="stylesheet" href="{% static 'css/blogApp.css' %}">
    <meta charset="utf-8">
    <title>{% block title_block %}{% endblock %}</title>
  </head>
  <body>
    <div class="content">
      {% block content %}{% endblock %}
    </div>
    <div class="sidebar">
      <h2>My Blog</h2>
      <p>Total number of posts published here :<span id="pcount">{% my_tag %}</span></p>
      <h3>Latest Posts:</h3>{%show_latest_posts 5%}
    </div>
  </body>
</html>
