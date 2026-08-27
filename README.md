# Felipe Duarte

Estudiante de Analista de Sistemas en la Universidad Siglo 21 (Córdoba, Argentina). Desarrollo web freelance con Next.js, Payload CMS y MongoDB.

## Stack

![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Payload CMS](https://img.shields.io/badge/Payload_CMS-000000?style=flat)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)

En la carrera: ![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white)

## Proyectos

- **Catálogo web para una revendedora de indumentaria** — Next.js, Payload CMS, MongoDB y TypeScript. Arquitectura en dos capas, integración continua en GitHub Actions y 23 decisiones de arquitectura documentadas. El código es privado; la documentación es pública en [NOMBRE-DEL-REPO](#).
- Trabajos académicos en Java: [concesionaria-autos](https://github.com/FeliDuarte/concesionaria-autos) y PeluqueriaCanina.

# Caso de estudio: catálogo web para una revendedora de indumentaria

Documentación de arquitectura de un proyecto freelance real: la especificación
y las 23 decisiones de arquitectura (ADRs) que definieron el sistema.

El código fuente es privado por acuerdo con el cliente. Lo que se publica acá
es el diseño: qué se decidió, por qué, y qué alternativas se descartaron.
Todas las referencias al cliente están anonimizadas.

## El problema

Una revendedora de indumentaria que vendía por Instagram necesitaba un catálogo
web propio: mostrar productos con sus variantes, mantener el stock al día y
recibir pedidos sin depender de mensajes directos.

## Stack

Next.js · Payload CMS · MongoDB · TypeScript · GitHub Actions

## Contenido

- [Especificación del proyecto](docs/especificacion.md) — alcance, requerimientos y modelo de dominio.
- [Índice de ADRs](adr/README.md) — las 23 decisiones, con su estado.

## Algunas decisiones

- **Modelo de dominio propio, no isomorfo al CMS.** El dominio declara sus
  propios tipos en lugar de importar los que genera Payload, para que un cambio
  de CMS no obligue a reescribir la lógica de negocio.
- **Arquitectura en dos capas.** Separación explícita entre dominio e
  infraestructura.
- **Una sola fuente de verdad para la disponibilidad.** El estado de la variante
  determina si un producto puede venderse; nada más lo decide.
- **Reserva optimista con actualizaciones condicionales atómicas.** Evita vender
  dos veces la misma unidad sin bloquear la base.

## Estado

Proyecto en desarrollo. La documentación refleja la versión 1.2 de la
especificación.

---

Felipe Duarte — [LinkedIn](https://www.linkedin.com/in/feli-duarte/) · [GitHub](https://github.com/FeliDuarte)
