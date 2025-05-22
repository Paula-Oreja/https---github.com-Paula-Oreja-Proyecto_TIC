# Proyecto TIC: Evaluación Comparativa de Rendimiento entre Máquina Virtual y Docker

## Introducción

Este proyecto compara el rendimiento y uso de recursos de una aplicación Java ejecutada en dos entornos distintos: una Máquina Virtual Ubuntu y un contenedor Docker. La aplicación es un juego de simulación de partido de fútbol desarrollado en Java.

---

## Estructura del Proyecto

- `/docker` : Contiene el código fuente Java (`Fifa.java`) y el `Dockerfile` para construir la imagen.  
- `/docs` : Documentación adicional con resultados, análisis y guías de instalación.  
- `README.md` : Descripción general y guía de uso.

---

## Escenario Máquina Virtual (Ubuntu)

Se configuró una máquina virtual con Ubuntu instalada mediante VirtualBox, donde se instaló Java y Git para ejecutar el juego. En [`docs/vm-instrucciones.md`](./docs/vm-instrucciones.md) se detalla el proceso de configuración y uso.

---

## Escenario Docker

La aplicación Java se ejecuta dentro de un contenedor Docker basado en la imagen oficial `openjdk:21-slim`. El `Dockerfile` y el código `Fifa.java` están ubicados en la carpeta `/docker`. Instrucciones para construir y ejecutar el contenedor:

```bash
cd docker
docker build -t fifa-java:1.0 .
docker run --rm fifa-java:1.0

