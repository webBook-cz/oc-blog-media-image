##Usage:

Use this markup to keep backward compatibility with first featured image 

{% if post.metadata.media_image %}
    {% set mainimagepath = post.metadata.media_image|media %}
{% else %}
    {% set mainimagepath = post.featured_images[0].path %}
{% endif %}

``` html
<img class="img-fluid" src="{{ mainimagepath }}" alt="{{ post.title }}">
```