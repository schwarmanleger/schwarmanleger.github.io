---
layout: default
title: Aktuelle Crowdfunding-Projekte
permalink: /projekte/
check_this_out: http://www.instantshift.com/2015/10/16/free-html5-css3-pricing-tables/
---

<h2>Projekte</h2>
  <div class="entry">
	Hier finden Sie eine Übersicht aktueller Crowdfunding-Projekte:<br><br>

	{% for projekt in site.data.projekte %}
	{% if projekt.name != "" %}
	<div class="ampstart-card ampstart-card-hover">
		<div class="m0 px2 py1 mb2 i-amphtml-form">
			<fieldset class="border-none p0 m0">
			<div class="relative m10 p10 px2 pb2 ta-r fw-b">
				<span class="mdl-chip"><span class="mdl-chip__text c-projprops" >{{ projekt.zins }}</span></span>
				<span class="mdl-chip"><span class="mdl-chip__text c-projprops">{{ projekt.dauer }}</span></span>
				<span class="mdl-chip {{ projekt.status_css }}"><span class="mdl-chip__text c-projprops status_text_highlight" >{{ projekt.status }}</span></span>
			</div>
			<div class="px2 pt0 pb2 fs-14">
				<div><h3 class="fs-18 m0 c-projtitle"><a target="_blank" href="{{ projekt.url }}">{{ projekt.name }}</a></h3></div>
				<div class="c-projdesc">{{ projekt.zusammenfassung }}</div>
				<div class="c-projprops">{{ projekt.konditionen }}</div>
			</div>
			<div class="p0 fs-14 ta-r"><a target="_blank" href="{{ projekt.url }}" >Zur Projektseite »</a></div>
			</fieldset>
		</div>
	</div>
	{% endif %}
	{% endfor %}
	
	<div class="kleintext">Zuletzt aktualisiert: {{ site.time | date: '%d.%m.%Y' }}</div>
	<div class="kleintext">
		<p>
			Haftungsausschluss: Die Inhalte dieser Seite dienen ausschließlich der Information und stellen nicht eine Anlageberatung oder sonstige Empfehlung im Sinne des Wertpapierhandelsgesetzes dar. Die auf dieser Seite bereit gestellten Informationen sollen nicht als Aufforderung verstanden werden, ein Geschäft oder eine Transaktion einzugehen. Alle Angaben ohne Gewähr - Irrtümer vorbehalten. Einige der externen Links sind sogenannte Affiliate-Links. Unseren vollständigen Disclaimer finden sie <a href="/disclaimer/">hier</a>.
		</p>
	</div>
</div>
