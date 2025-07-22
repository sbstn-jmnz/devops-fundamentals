+++
title = "Testing ágil"
date = 2025-07-08
description = "Pruebas automatizadas"
template = "docs/page.html"
weight = 100
sort_by = "weight"

[extra]
toc = true
top = false
+++

## 1. Testing en un entorno ágil

## ¿Qué es Agile Testing?

Agile Testing es un enfoque de pruebas de software que se alinea con los principios del desarrollo ágil. A diferencia de los enfoques tradicionales, donde las pruebas se ejecutan al final del ciclo de desarrollo, en Agile Testing las pruebas se integran desde el inicio y se realizan de forma continua a lo largo del desarrollo del producto.

Este tipo de pruebas fomenta la colaboración entre testers, desarrolladores y usuarios, y se centra en entregar valor de negocio de forma iterativa. El feedback rápido y la detección temprana de errores son pilares fundamentales, lo que permite ajustar los entregables en tiempo real y mantener la calidad sin frenar la velocidad de entrega.

Agile Testing no es una técnica específica, sino un enfoque cultural y metodológico que aboga por la integración de la calidad como una responsabilidad compartida dentro del equipo ágil.

[Testing pyramid](https://martinfowler.com/articles/practical-test-pyramid.html)

## Principios y prácticas de Agile Testing

Entre los principios más importantes del Agile Testing se encuentran la colaboración continua, el enfoque en la entrega temprana de valor, la retroalimentación constante y la automatización de las pruebas. Los testers trabajan junto con los desarrolladores desde el inicio, ayudando a definir criterios de aceptación y a construir casos de prueba en paralelo con el código.

Prácticas comunes incluyen Test Driven Development (TDD), Acceptance Test Driven Development (ATDD) y Behaviour Driven Development (BDD), que permiten construir software basado en pruebas desde el diseño. Estas técnicas aseguran que el código cumpla con los requisitos funcionales antes incluso de ser escrito.

Otro principio esencial es la mejora continua. Los equipos revisan y ajustan regularmente sus procesos de prueba para responder mejor al cambio, reducir el retrabajo y aumentar la eficiencia del ciclo de desarrollo.

## El rol del tester en marcos ágiles

En un equipo ágil, el rol del tester va mucho más allá de simplemente “probar”. Se convierte en un facilitador de calidad, integrándose al equipo de desarrollo para anticipar defectos, clarificar requisitos y aportar una visión crítica sobre la usabilidad y confiabilidad del sistema.

El tester participa en ceremonias ágiles como refinamientos, planificaciones y retrospectivas. Aporta una mirada basada en la experiencia del usuario y la validación temprana, sugiriendo estrategias de prueba automatizadas y exploratorias desde el día uno.

Además, es habitual que el tester en entornos ágiles posea conocimientos técnicos que le permitan colaborar en la escritura de scripts automatizados, configuración de pipelines de testing y monitoreo de calidad continua.

## Pruebas en el pipeline de integración continua

La integración continua (CI) implica integrar y validar los cambios de código de forma frecuente, idealmente varias veces al día. Las pruebas son una parte crítica de este proceso, ya que aseguran que el nuevo código no introduzca errores ni rompa funcionalidades existentes.

Dentro del pipeline de CI, las pruebas se ejecutan automáticamente cada vez que se sube nuevo código al repositorio. Estas pruebas incluyen unitarias, de integración, de sistema, de regresión, entre otras. Si alguna de estas pruebas falla, se interrumpe el pipeline, permitiendo actuar de inmediato sobre el error.

La automatización de pruebas en el pipeline no solo mejora la velocidad del desarrollo, sino que también incrementa la confianza del equipo en la calidad del software entregado. Esto habilita prácticas como entrega continua (CD) y despliegue continuo (CD), donde los cambios llegan más rápido y seguros al entorno productivo.

## Tipos de prueba:

### Unitarias

Las pruebas unitarias validan el comportamiento de unidades pequeñas e independientes de código, como funciones o métodos. Son las más cercanas al desarrollador y permiten detectar errores en etapas tempranas del ciclo de vida del software.

Su principal ventaja es la rapidez de ejecución y su alta cobertura. Al estar automatizadas, se convierten en la primera línea de defensa contra errores y regresiones. Herramientas como JUnit (Java), pytest (Python) o Mocha (JavaScript) son ampliamente utilizadas para este propósito.

Las pruebas unitarias deben ser simples, independientes y predecibles. Idealmente, deberían ejecutarse con cada commit y formar parte obligatoria del pipeline de CI.

### Integración

Estas pruebas aseguran que múltiples módulos o componentes de una aplicación funcionen correctamente en conjunto. Se encargan de validar flujos entre clases, capas de arquitectura (como frontend-backend) o interacciones con servicios externos.

A menudo, las pruebas de integración detectan errores que no son visibles a nivel unitario, como incompatibilidades entre versiones de APIs, mal manejo de datos o errores de configuración. Suelen requerir entornos de prueba más complejos y mayor tiempo de ejecución.

Su automatización debe planificarse considerando sus dependencias, y pueden implementarse con herramientas como Postman, REST Assured, TestContainers, entre otras.

### Sistema (funcionales, rendimiento)

Las pruebas de sistema validan el software como un todo, probando funcionalidades de extremo a extremo desde la perspectiva del usuario. Estas incluyen tanto pruebas funcionales como pruebas no funcionales, como rendimiento, seguridad o accesibilidad.

Las pruebas funcionales verifican que el sistema haga lo que se espera según los requerimientos definidos. Pueden realizarse con herramientas como Selenium o Cypress.

Las pruebas de rendimiento, por su parte, buscan identificar cuellos de botella, consumo excesivo de recursos o inestabilidad bajo carga. JMeter es una herramienta común para estas pruebas. Su ejecución frecuente es crucial para garantizar una experiencia de usuario satisfactoria.

### Aceptación y humo

Las pruebas de aceptación son definidas por el cliente o el Product Owner y validan que el software cumple con los criterios de negocio. Suelen implementarse como pruebas automáticas al final de cada sprint y son clave para validar entregas incrementales.

Por otro lado, las pruebas de humo son una colección mínima de pruebas que aseguran que el sistema es estable después de una nueva compilación o despliegue. Se enfocan en las funcionalidades más críticas y permiten una validación rápida antes de ejecutar pruebas más exhaustivas.

Ambos tipos son esenciales para entornos de CI/CD, donde se requiere validación rápida y confiable para cada entrega.

## Objetivo y beneficios de la automatización

El objetivo principal de automatizar pruebas es mejorar la eficiencia, confiabilidad y repetibilidad del proceso de validación del software. Esto permite a los equipos entregar valor continuamente, sin comprometer la calidad.

La automatización reduce el esfuerzo manual, minimiza los errores humanos y permite ejecutar grandes cantidades de pruebas en menor tiempo. Además, facilita el feedback temprano, lo que es vital para resolver errores antes de que escalen en complejidad y costo.

Otro beneficio es la capacidad de escalar: a medida que el sistema crece, las pruebas automatizadas permiten mantener la calidad sin requerir proporcionalmente más testers. También proporcionan documentación viva del comportamiento esperado del sistema, ayudando a nuevos integrantes del equipo a entender la lógica del producto.

## Herramientas comunes para la automatización de pruebas

Existen múltiples herramientas especializadas para distintos tipos de pruebas. Para pruebas unitarias, destacan JUnit (Java), NUnit (.NET), pytest (Python), entre otras. Estas herramientas permiten integrar las pruebas directamente en el entorno de desarrollo y en pipelines de CI.

Para pruebas funcionales en interfaces web, Selenium y Cypress son ampliamente utilizadas. Selenium permite automatizar navegadores reales, mientras que Cypress es más reciente y se enfoca en pruebas rápidas y consistentes en el frontend.

Para pruebas de APIs o servicios web, SoapUI y Postman permiten crear suites automatizadas. JMeter es común para pruebas de carga y estrés. Finalmente, herramientas como Jenkins, GitHub Actions o GitLab CI permiten orquestar la ejecución automática de todas estas pruebas en un flujo de integración continua.

La elección de herramientas dependerá del stack tecnológico, nivel de automatización deseado y recursos disponibles del equipo.
