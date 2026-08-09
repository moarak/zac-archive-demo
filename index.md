---
layout: default
title: Catalog
nav_order: 1
has_children: true
---

# Archivo digital de las obras de Zoila Aurora Cáceres (1872-1958)

Este repositorio reúne versiones digitales
de la obra de **Zoila Aurora Cáceres** 
(Lima, 1872 – Madrid, 1958), escritora, 
periodista y activista feminista peruana. 
Figura central del modernismo hispanoamericano 
y de los primeros movimientos por los derechos 
de la mujer en el Perú, Cáceres desarrolló una 
obra dispersa en revistas, periódicos y 
ediciones hoy poco accesibles, que este archivo 
reúne y ofrece a la comunidad investigadora y 
al público general.

---

## Colección

{% for item in site.pages %}
  {% if item.parent == "Catalog" %}
  <div style="border: 1px solid #D7CCC8; padding: 16px; margin-bottom: 20px; background-color: #ffffff;">
    <a href="{{ item.url | relative_url }}">
      <img src="{{ item.cover | relative_url }}" alt="{{ item.title }} Cover" style="max-width: 100px; float: left; margin-right: 16px; border: 1px solid #e0e0e0;">
    </a>
    <h3 style="margin-top: 0;"><a href="{{ item.url | relative_url }}">{{ item.title }}</a></h3>
    <p style="margin-bottom: 8px;"><strong>{{ item.author }}</strong> ({{ item.year }})</p>
    <p style="font-size: 0.9em; margin-bottom: 12px;">{{ item.description }}</p>
    <p style="margin-bottom: 0;">
      <a href="{{ item.download_url | relative_url }}">[ Descargar .TXT ]</a>
    </p>
    <div style="clear: both;"></div>
  </div>
  {% endif %}
{% endfor %}