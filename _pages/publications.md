---
title: "van der Sar Lab - Publications"
layout: gridlay
excerpt: "van der Sar Lab -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

## Group highlights

**At the end of this page, you can find the [full list of publications](#full-list-of-publications). All papers are also available on [arXiv](https://arxiv.org/search/?query=van+der+Sar+Toeno&searchtype=all&source=header).**

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>


## Patents
<em>    W H Peeters, JE R Jacobs, R Bezemer, T van der Sar, J Muehlsteff </em><br />  Green light photoplethysmography in transmission geometry <br /> <a href="https://patents.google.com/patent/WO2017001955A1/en?inventor=Toeno+VAN+DER+SAR"> WO2017001955A1 (2016) </a>

<em>    E R Jacobs, W H Peeters, J W Weekamp, J van Roosmalen, R Bezemer, I W F Paulussen, T van der Sar </em><br /> Fixation method for a nasal septum sensor for measuring medical parameters<br /> <a href="https://patents.google.com/patent/WO2016067153A1/en?inventor=Toeno+VAN+DER+SAR"> WO2016067153A1 (2015) </a>

<em>    W H Peeters, T van der Sar, E R Jacobs, G M Verbeek, J W Weekamp </em><br />  Flexible optical source for pulse oximetry <br /> <a href="https://patents.google.com/patent/EP3206572B1/en?inventor=Toeno+VAN+DER+SAR"> EP3206572B1 (2015) </a>

## Full List of publications

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
