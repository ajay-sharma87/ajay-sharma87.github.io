---
layout: default
---

<section id="about">
<h2>About</h2>
<div class="bio-grid">
<div class="bio-text">
{{ site.data.profile.bio | markdownify }}
<div class="contact-block">
🏛 &nbsp;{{ site.institution }}, Rau–Pithampur Road, Indore 453 556<br>
{% if site.email != "" %}✉️ &nbsp;<a href="mailto:{{ site.email }}">{{ site.email }}</a><br>{% endif %}
🔗 &nbsp;{% if site.ideas_repec != "" %}<a href="{{ site.ideas_repec }}" target="_blank">IDEAS/RePec</a> &nbsp;·&nbsp;{% endif %}{% if site.google_scholar != "" %}<a href="{{ site.google_scholar }}" target="_blank">Google Scholar</a> &nbsp;·&nbsp;{% endif %}{% if site.researchgate != "" %}<a href="{{ site.researchgate }}" target="_blank">ResearchGate</a>{% endif %}
</div>
</div>
<div class="bio-photo">
  <div class="photo-placeholder">
    <svg width="48" height="48" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><circle cx="12" cy="8" r="4"/><path d="M4 20c0-4 3.6-7 8-7s8 3 8 7"/></svg>
    <span>Photo</span>
  </div>
</div>
</div>
</section>

<section id="research">
<h2>Research Interests</h2>
<div class="tags">
{% for interest in site.data.profile.research_interests %}<span class="tag">{{ interest }}</span>{% endfor %}
</div>
</section>

<section id="publications">
<h2>Publications</h2>
<p class="section-label">Peer-Reviewed Journal Articles</p>
<ol class="pub-list">
{% for pub in site.data.publications.journal_articles %}
<li>
  <span class="pub-title">{{ pub.title }}</span>
  <div class="pub-meta">{% if pub.authors %}{{ pub.authors }} &nbsp;·&nbsp;{% endif %}<span class="journal">{{ pub.journal }}</span>{% if pub.details %}, {{ pub.details }}{% endif %}{% if pub.year == "forthcoming" %} (forthcoming){% endif %}</div>
  {% if pub.link or pub.wp %}<div class="pub-links">{% if pub.link %}<a class="pub-link" href="{{ pub.link }}" target="_blank">link</a>{% endif %}{% if pub.wp %}<a class="pub-link" href="{{ pub.wp }}" target="_blank">wp</a>{% endif %}</div>{% endif %}
</li>
{% endfor %}
</ol>

<p class="section-label">Commentaries</p>
<ol class="pub-list">
{% for pub in site.data.publications.commentaries %}
<li>
  <span class="pub-title">{{ pub.title }}</span>
  <div class="pub-meta">{% if pub.authors %}{{ pub.authors }} &nbsp;·&nbsp;{% endif %}<span class="journal">{{ pub.journal }}</span>{% if pub.details %}, {{ pub.details }}{% endif %}</div>
  {% if pub.link %}<div class="pub-links"><a class="pub-link" href="{{ pub.link }}" target="_blank">link</a></div>{% endif %}
</li>
{% endfor %}
</ol>

<p class="section-label">Book Chapters &amp; Reports</p>
<ol class="pub-list">
{% for pub in site.data.publications.book_chapters %}
<li>
  <span class="pub-title">{{ pub.title }}</span>
  <div class="pub-meta">{% if pub.authors %}{{ pub.authors }} &nbsp;·&nbsp;{% endif %}<em>{{ pub.venue }}</em>, {{ pub.year }}</div>
  {% if pub.link %}<div class="pub-links"><a class="pub-link" href="{{ pub.link }}" target="_blank">link</a></div>{% endif %}
</li>
{% endfor %}
</ol>

<p class="section-label">Working Papers</p>
<ol class="pub-list">
{% for pub in site.data.publications.working_papers %}
<li>
  <span class="pub-title">{{ pub.title }}</span>
  <div class="pub-meta">{% if pub.authors %}{{ pub.authors }}{% endif %}</div>
  {% if pub.link %}<div class="pub-links"><a class="pub-link" href="{{ pub.link }}" target="_blank">link</a></div>{% endif %}
</li>
{% endfor %}
</ol>

<div class="profile-links">
{% if site.ideas_repec != "" %}<a class="profile-link" href="{{ site.ideas_repec }}" target="_blank">IDEAS/RePec Profile</a>{% endif %}
{% if site.google_scholar != "" %}<a class="profile-link" href="{{ site.google_scholar }}" target="_blank">Google Scholar Profile</a>{% endif %}
{% if site.researchgate != "" %}<a class="profile-link" href="{{ site.researchgate }}" target="_blank">ResearchGate Profile</a>{% endif %}
</div>
</section>

<section id="teaching">
<h2>Teaching</h2>
<p>I teach across MBA, Executive Education, and PhD programmes at {{ site.institution }}.</p>
<div class="teaching-grid">
{% for course in site.data.teaching.courses %}
<div class="course-card">
  <div class="level">{{ course.level }}</div>
  <h3>{{ course.title }}</h3>
  <p>{{ course.description }}</p>
</div>
{% endfor %}
</div>
</section>

<section id="cv">
<h2>CV</h2>
<div class="cv-section">
<h3>Positions</h3>
{% for pos in site.data.cv.positions %}
<div class="cv-row"><span class="year">{{ pos.years }}</span><div class="detail"><strong>{{ pos.title }}</strong>{{ pos.institution }}</div></div>
{% endfor %}
</div>
<div class="cv-section">
<h3>Education</h3>
{% for edu in site.data.cv.education %}
<div class="cv-row"><span class="year">{{ edu.year }}</span><div class="detail"><strong>{{ edu.degree }}</strong>{{ edu.institution }}</div></div>
{% endfor %}
</div>
<div class="cv-section">
<h3>Grants</h3>
{% for grant in site.data.cv.grants %}
<div class="cv-row"><span class="year">{{ grant.years }}</span><div class="detail"><strong>{{ grant.title }}</strong>{{ grant.description }}</div></div>
{% endfor %}
</div>
{% if site.cv_pdf != "" %}<a href="{{ site.cv_pdf }}" class="cv-download"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"/><polyline points="7 10 12 15 17 10"/><line x1="12" y1="15" x2="12" y2="3"/></svg> Download Full CV (PDF)</a>{% endif %}
</section>

<section id="contact">
<h2>Contact</h2>
<div class="contact-grid">
<div>
<p><strong>Mailing Address</strong></p>
<p class="mono-text">{{ site.title }}<br>Economics Area<br>{{ site.institution }}<br>Rau–Pithampur Road<br>Indore 453 556, Madhya Pradesh, India</p>
</div>
<div>
<p><strong>Online Profiles</strong></p>
<div class="profile-links vertical">
{% if site.ideas_repec != "" %}<a class="profile-link" href="{{ site.ideas_repec }}" target="_blank">IDEAS/RePec</a>{% endif %}
{% if site.google_scholar != "" %}<a class="profile-link" href="{{ site.google_scholar }}" target="_blank">Google Scholar</a>{% endif %}
{% if site.researchgate != "" %}<a class="profile-link" href="{{ site.researchgate }}" target="_blank">ResearchGate</a>{% endif %}
</div>
</div>
</div>
</section>
