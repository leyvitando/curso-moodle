# Créditos

## Autoría

* {{ book.author }}

### Colaboradores:

{% for collaborator in book.collaborators %}
* {{collaborator.name}} en {{collaborator.edited}}
{% endfor %}

___

{% include "git+https://github.com/catedu/faq-aularagon.git/imagenes_creditos.md" %}

**Materiales cofinanciados por Fondo Social Europeo**

![](img/FSE_grande_fondo_blanco.jpg)