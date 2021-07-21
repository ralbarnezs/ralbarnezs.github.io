---
layout: post
title: Sistemas distribuidos
subtitle: Projectos de aplicacion distribuidas de la asignatura INF-343
gh-repo: daattali/beautiful-jekyll
tags: [golang, socket,  gRPC, RabbitMQ]
comments: true
---

### Primer proyecto

El objetivo de este proyecto fue aplicar de forma practica los contenidos en la primera parte del curso de sistemas distribuidos. Para esto se llevo a cabo una aplicación que buscaba emular un sistema distribuido de paquetería. Este sistema podría verse como un Chile Express donde hay diferentes secciones. Entre las principales se encuentran:

- Cliente: Este intenta acceder a información de entrega del paquete. Esta información debe actualizarse en tiempo real y es lo que hace la solución implementada, cada vez que cambia el estado de un paquete.
- Contabilidad: logística hace los reportes (envió de mensajes) a esta sección a través de RabbitMQ para que esta sección de la empresa realice la escritura al libro contable y reporte las ganancias del día.
- Reparto: Tiene por objetivo distribuir de forma óptima los camiones con paquetes a entregar. La forma optima está determinada por kilómetros a recorrer y los intentos de entrega. Por ejemplo, un paquete con entrega normal (no prioritario) no se intenta entregar una segunda vez, pues seria mas caro que lo que pago el cliente (esto bien podría relajarse).

Estas secciones necesitan tanto acceder a secciones criticas para tomar una orden, modificar su estado como también el paso de mensajes entre ellas. Para estos requerimientos se utiliza gRPC con protocol buffers, así como RabbitMQ. Cabe recalcar que el objetivo de este proyecto era crear un sistema distribuido y simularlo, por lo tanto, no tiene front-end y su ejecución es mediante consola de comandos.

Para más detalles técnicos y acceso al código fuente de lo desarrollado, puede acceder directamente al repositorio.


{: .box-note}
**Repositorio:** [primer proyecto](https://github.com/ralbarnezs/lab1).
