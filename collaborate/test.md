---
layout: post
title: "test"
purple-text-title: "test"
categories: Collaborate
doc_order_id: 6
---

{% for main in site.data.menu %}
    {{ main.main_item }}
        {% for submenu in main.sub_item %}
            {{ submenu.submenu_item }}
            {{ submenu.submenu_url }}
                {% for subsubmenu in submenu.subsubmenu %}
                    {{ subsubmenu.subsubmenu_item }}
                    {{ subsubmenu.subsubmenu_url }}
                        {% for subsubmenucontent in subsubmenu.subsubmenu_content %}
                            {{ subsubmenucontent.subsubmenu_content_name}}
                            {{ subsubmenucontent.subsubmenu_content_url }}
                        {% endfor %}
                {% endfor %}
        {% endfor %}
{% endfor %}

### **********************

<li class="no-padding">
        <ul class="collapsible collapsible-accordion">
{% for main in site.data.menu %}
    <li id="{{ main.main_item }}">
        <a  class="collapsible-header">
           <i class="material-icons">{{ main.main_item_icon }}</i>{{ main.main_item }}</a>
        </ul>
        {% for submenu in main.sub_item %}
            {{ submenu.submenu_item }}
            {{ submenu.submenu_url }}
                {% for subsubmenu in submenu.subsubmenu %}
                    {{ subsubmenu.subsubmenu_item }}
                    {{ subsubmenu.subsubmenu_url }}
                        {% for subsubmenucontent in subsubmenu.subsubmenu_content %}
                            {{ subsubmenucontent.subsubmenu_content_name}}
                            {{ subsubmenucontent.subsubmenu_content_url }}
                        {% endfor %}
                {% endfor %}
        {% endfor %}
{% endfor %}

</li>