---
layout: page
title: Introducción a la programación científica
nositetitle: true
---

El objetivo de este curso es exponer las bases para el desarrollo de aplicaciones en entorno UNIX con fines científicos, con enfasis en los aspectos prácticos de su programación e implementación.

El curso no asume conocimientos previos de programación, por lo que en la primer parte se da una intruducción al uso de linea de comando (*shell*), la sintaxis de los lenguajes más utilizados en esta disciplina (`C` y `Fortran`), asi también como herramientas para compilar, desarrollar, debuggear y perfilar programas.

El foco del curso está en exponer la sintaxis de programas escritos en C, Fortran y Python.

Acá podés encontrár algunas de [aplicaciones](/ejemplos/) que trataremos en el curso.

# Programa del curso

<ul>
{% assign clases = site['clases'] | sort: 'date' %}
{% for clase in clases %}
    {% if clase.phony != true %}
      {% if clase.ready %}
        <li>
        <strong>{{ clase.date | date: 'C%-m.%-d' }}</strong>:
            <a href="{{site.baseurl}}{{ clase.url }}">{{ clase.title }}</a>
        </li>
        {% else %}
        {% comment %}
        	 <li>  {{ clase.title }} {% if clase.noclass %}[no class]{% endif %}</li> 
        {%endcomment%}
      {% endif %}
    {% endif %}
{% endfor %}
</ul>

Los video tutoriales estarán disponible [en Youtube](https://www.youtube.com/@ramiroespadaguerrero/playlists).

---

<div class="small center">
<p><a href="https://github.com/ramespada/sintaxis">Repositorio</a>.</p>
<p>Licencia CC</p>
</div>
