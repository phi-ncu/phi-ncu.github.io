---
title: People
permalink: /people/
---

### Team

<img class='img-responsive center-block' src="/images/others/PHI_lab.png" width="100%" height="100%" />


#{% assign people_sorted = site.people | sort: 'joined' %}
#{% assign role_array = "pi|postdoc|gradstudent|researchstaff|visiting|team|alumni" | split: "|" %}

#{% for role in role_array %}

#{% assign people_in_role = people_sorted | where: 'position', role %}

<!-- Skip section if there's nobody -->
{% if people_in_role.size == 0 %}
  {% continue %}
{% endif %}

<div class="pos_header">
{% if role == 'postdoc' %}
<h3>Postdoctoral Fellows</h3>
 {% elsif role == 'pi' %}
<h3>Principal Investigator</h3>
 {% elsif role == 'gradstudent' %}
<h3>Graduate Students</h3>
 {% elsif role == 'researchstaff' %}
<h3>Research Staff</h3>
 {% elsif role == 'visiting' %}
<h3>Visiting Scholars</h3>
 {% elsif role == 'team' %}
<h3>Team</h3>
 {% elsif role == 'alumni' %}
<h3>Alumni</h3>
{% endif %}
</div>

{% if role != 'alumni' %}
<div class="content list people">
  {% for profile in people_sorted %}
    {% if profile.position contains role %}
      <div class="list-item-people">
        <p class="list-post-title">
          {% if profile.avatar %}
            <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="{{site.baseurl}}/images/people/{{profile.avatar}}"></a>
          {% else %}
            <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="http://evansheline.com/wp-content/uploads/2011/02/facebook-Storm-Trooper.jpg"></a>
          {% endif %}
          <a class="name" href="{{ site.baseurl }}{{ profile.url }}">{{ profile.name }}</a>
        </p>
      </div>    
    {% endif %}
  {% endfor %}
</div>
<hr>

{% else %}

<br>

{% endif %}
{% endfor %}

### Scientific collaboration

- [Danielle Bassett (University of Pennsylvania, USA)](https://live-sas-physics.pantheon.sas.upenn.edu/people/standing-faculty/danielle-bassett)
- [Nicolas Schuck (Max Planck Institute for Human Development, Berlin, Germany)](https://www.mpib-berlin.mpg.de/staff/nicolas-schuck)
- [Olivier Hulme (Danish Research Centre for Magnetic Resonance in Copenhagen, Denmark)](https://www.drcmr.dk/ollieh)]
- [Charley Wu (Human and Machine Cognition Lab, Eberhard Karl University, Tübingen, Germany)](https://charleywu.github.io/)
- [Giovanni Petri (The Institute for Scientific Interchange Foundation, Turin, Italy)](https://lordgrilo.github.io/)
- [Simone Kühn (Max Planck Institute for Human Development, Germany)](https://www.mpib-berlin.mpg.de/staff/simone-kuehn)
- [Russell Poldrack (Stanford University, USA)](https://poldracklab.stanford.edu/)
- [Oscar Esteban (University of Lausanne, USA)](https://wp.unil.ch/connectomics/team/oscar-esteban/)
- [Xiaosong He (University of Pennsylvania, USA)](https://www.linkedin.com/in/xiaosong-he-380b25aa/)
- [David Lydon-Staley (University of Pennsylvania, USA)](https://www.asc.upenn.edu/people/faculty/david-lydon-staley-phd)

### Collaboration with organizations

- [Neurodio](https://neurodio.com/)
- [Neurotechnology Scientific Students Club](https://neurotech.umk.pl/pages/main_page/)
- [Inny Rytm](https://innyrytm.pl/)


 
