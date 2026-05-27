# Patrones_eva2
Turnomatico
# Sistema Tunomático Inteligente

- Introducción

El presente proyecto desarrolla el modelado UML completo de un sistema digital de administración de turnos, diseñado para optimizar la atención de usuarios en organizaciones públicas o privadas.

La solución propuesta contempla el flujo completo de atención, desde la solicitud inicial del turno hasta la visualización y cierre del proceso de atención. Para ello, se utilizaron herramientas UML orientadas al análisis funcional, estructural y físico del sistema.

Además, el diseño incorpora patrones de software ampliamente utilizados en ingeniería de software moderna, permitiendo mejorar la mantenibilidad, reutilización y escalabilidad de la arquitectura.


- Diagrama de Casos de Uso

  <img width="516" height="1039" alt="1" src="https://github.com/user-attachments/assets/86fd1aeb-99b3-4032-bfe3-601d292e76ee" />


El diagrama representa las interacciones entre los distintos actores y las funcionalidades disponibles dentro del sistema.

* Actores del sistema

* Usuario
Corresponde a la persona que solicita atención mediante el kiosko digital o plataforma de autoservicio.

* Operador
Funcionario encargado de gestionar el flujo de atención y llamar los turnos pendientes.

* Supervisor
Administrador responsable de configurar servicios, módulos y reportes operacionales.

* Servicios externos
Incluyen sistemas de mensajería y dispositivos visuales utilizados para complementar la experiencia de atención.


* Relaciones utilizadas

Las relaciones `<<include>>` fueron utilizadas en funcionalidades obligatorias dentro del flujo principal. Por ejemplo, solicitar un turno requiere necesariamente elegir un servicio y generar un comprobante.

Las relaciones `<<extend>>` representan comportamientos opcionales o situaciones complementarias que pueden ejecutarse dependiendo del contexto operativo.


- Diagrama de Clases

  <img width="1474" height="383" alt="2" src="https://github.com/user-attachments/assets/c4ab3116-004a-4b81-89d7-98b2ccf0e187" />


El modelo de clases define la estructura lógica del sistema, incorporando atributos, métodos, asociaciones y patrones de diseño.

Aplicación de patrones

* Singleton

La clase `GestorCentral` utiliza el patrón Singleton para garantizar que exista un único controlador responsable de administrar la cola principal de turnos.

Esto evita inconsistencias en ambientes concurrentes y permite centralizar la lógica del sistema.


* Prototype

La clase `Turno` implementa Prototype, permitiendo generar nuevas instancias a partir de estructuras previamente configuradas.

Esto facilita la creación eficiente de tickets de atención.


* Adapter

El patrón Adapter se implementa mediante `AdaptadorSMS`, permitiendo conectar el sistema con proveedores externos de mensajería sin alterar la lógica interna.

Gracias a esto, el sistema puede cambiar fácilmente de proveedor tecnológico.


* Bridge

El patrón Bridge separa la lógica de visualización de los dispositivos físicos utilizados.

De esta forma, el sistema puede mostrar información tanto en televisores LED como en monitores interactivos sin modificar el comportamiento principal.


- Diagrama de Implementación

  <img width="1600" height="463" alt="3" src="https://github.com/user-attachments/assets/e412d6f4-9f49-4adf-adc9-67d42d9335f6" />


El diagrama de implementación representa cómo se distribuyen físicamente los componentes dentro de la arquitectura tecnológica.

* Componentes principales

- Terminales de autoservicio.
- Servidor principal de aplicaciones.
- Base de datos SQL.
- Servicios externos de mensajería.
- Pantallas digitales de atención.


* Decisiones técnicas

El servidor principal concentra toda la lógica operacional del sistema, mientras que los servicios externos quedan desacoplados mediante adaptadores.

La visualización fue diseñada bajo una arquitectura flexible, permitiendo agregar nuevos dispositivos de salida sin alterar el sistema base.

La separación de responsabilidades facilita futuras ampliaciones y mejora la mantenibilidad general del software.


- Conclusiones

El modelado realizado permitió representar el sistema desde distintas perspectivas UML, logrando una visión integral tanto funcional como arquitectónica.

La incorporación de patrones de diseño permitió estructurar una solución más ordenada y preparada para escenarios reales de crecimiento.

Finalmente, el proyecto demuestra cómo UML y los principios de diseño orientado a objetos pueden utilizarse para construir arquitecturas robustas y escalables en sistemas de atención digital.
