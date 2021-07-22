---
layout: post
title: Sians
subtitle: Sistema de interconexión de aplicaciones vía SMS-Internet
gh-repo: daattali/beautiful-jekyll
tags: [Node, Flask, MongoDB, React, Javascript, Python, TextNow]
comments: false
---

### Descripción del problema

En Chile, casi uno de cada tres colegios no tiene conexión a internet. Son, en total, 2.680 recintos, el 47% rurales, donde las clases online o híbridas, por motivo de pandemia, se han vuelto una misión imposible. Es por esto que los mismos estudiantes y profesores han tenido que realizar un mayor esfuerzo por mantenerse comunicados, teniendo que realizar acciones como subir cerros o techumbres con el fin de lograr una conexión a internet, poniendo en riesgo su propia integridad.

### Solución propuesta

Como solución a esta problemática surge Sians. La idea es proveer una aplicación móvil para el estudiante y web para el profesor. Los pasos que sigue el proceso son los siguientes:

- El profesor redacta documentos en la aplicación web.
- Estos son codificados a través de un lenguaje de marcado de texto propio.
- El output del paso anterior es comprimido con el fin de minimizar el tamaño del texto a enviar.
- Por temas de seguridad, se realiza un cifrado al texto mencionado anteriormente.
- Se envía uno (o más) SMS con el output que fue cifrado.
- La aplicación móvil descifra, descomprime y decodifica el output recibido y así el estudiante obtiene el documento que originalmente redactó el profesor y pudiendo exportarlo a pdf si así lo quiere.  

En conclusión, el estudiante podrá recibir material educativo de parte de su profesor sin necesidad de contar con una conexión a internet; los únicos requisitos una vez instalada la aplicación móvil son disponer de un celular con cobertura a una red de telefonía móvil.

Esta idea fue postulada a la asignatura de gestión de proyectos la cual es parte de Feria de Software que busca desarrollar un producto funcional a través de un año académico. Esto con el fin de potenciar la idea (con el feedback obtenido mediante los profesores) y acceder a fondos. 

Actualmente junto a otros tres integrantes a los cuales convencí de ser parte del proyecto, nos encontramos en la fase de demostración del PMV. En el repositorio dispuesto a continuación se encuentra totalmente funcional todo lo desarrollado para la parte web (de la cual me encargue), que es lo que requirió resolver más tareas con el fin de realizar el PMV. Por motivo de que mis compañeros hicieron lo referente a la aplicación móvil no subo el código de esta por ahora, quedando la tarea de desarrollarla por mí mismo en Ionic y subirla dentro de los próximos dos meses.


Como comentario final, debido a que este PMV fue desarrollado parcialmente durante tres semanas, no se dio lugar a estructurar de buena forma el código ni separar por microservicios, dos tareas prioritarias apenas termine el actual semestre académico. 

{: .box-note}
**Repositorio:** [Sians](https://github.com/ralbarnezs/sians).




