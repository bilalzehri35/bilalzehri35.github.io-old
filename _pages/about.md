---
layout: page
title: About 
permalink: /about
comments: false
---
The Margalla Today, founded in 2021 by Founder & Editor in Chief Raheem Jamali, is dedicated to reporting on current issues that are insufficiently covered by mainstream media. The websiteâ€™s mission is to dig beneath the headlines, provide expert reporting and commentary from a neutral point of view and offer an outlet for original work by exceptional journalists & responsible citizens.

The Margalla Today aspires for honest and credible reporting and is careful about fact-checking. We strive that our reporting meet the highest standards and focus on the issues that matter most.

We do not tell any of our contributors what to write, and the website does not always agree with the views of its writers and bloggers. We are proud to have created a home for provocative and talented writers and to give them the freedom to pursue a story wherever it takes them.

<div class="list-authors mt-5">
{% for author in site.authors %}   
    <div id="{{ author[1].name }}" class="authorbox position-relative pb-5 pt-5 mb-4 mt-4 border">   
        <div class="row">
            <div class="wrapavname col-md-3 text-center">
                {% if author[1].gravatar %}
                <img  class="author-thumb" src="https://www.gravatar.com/avatar/{{ author[1].gravatar }}?s=250&d=mm&r=x" alt="{{ author.display_name }}">
                {% else %}
                <img  class="author-thumb" src="{{site.baseurl}}/{{ author[1].avatar }}" alt="{{ author.display_name }}">
                {% endif %}

                <p class="mt-4 mb-0 small text-center">

                    {% if author[1].web %}
                        <a target="_blank" class="d-inline-block mx-1 text-dark" href="{{ author[1].web }}"><i class="fa fa-link"></i></a> 
                    {% endif %}

                    {% if author[1].twitter %}
                        <a target="_blank" class="d-inline-block mx-1 text-dark" href="{{ author[1].twitter }}"><i class="fab fa-twitter"></i></a>
                    {% endif %}

                    {% if author[1].email %}
                        <a class="d-inline-block mx-1 text-dark" href="mailto:{{ author[1].email }}"><i class="fa fa-envelope"></i></a>
                    {% endif %}

                </p>
                
            </div>
            <div class="col-md-9">
                <h3>{{ author[1].display_name }}</h3>
                <p class="mt-3 mb-0">{{ author[1].description }}</p> 
            </div>
        </div> 
    </div>    
{% endfor %}
</div>
