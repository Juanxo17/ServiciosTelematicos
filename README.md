# Servicios Telemáticos

Repositorio académico para la materia **Servicios Telemáticos** que contiene configuraciones, prácticas y parciales desarrollados durante el semestre.

---

## Estructura del Repositorio

Este repositorio está organizado en ramas por corte:

- **main** → Rama principal con información general.
- **primerParcial** → Configuración y resultados del primer parcial.

---

## Primer Parcial (primerParcial)
Optimización y exposición de un servidor web.

### Parte 1: Configuración DNS Maestro-Esclavo
- Configuración de **BIND9** con resolución directa e inversa.  
- Dominio configurado: `empresa.local`.  
- Verificación de resolución con `dig` y `host`.  
- Pruebas de funcionamiento con Maestro activo y pruebas al Esclavo cuando el Maestro está detenido.

### Parte 2: Compresión en Apache
- **Apache2** con `mod_deflate` habilitado.  
- Compresión de archivos estáticos: `.html`, `.css`, `.js`.  
- Exclusión de imágenes y videos de la compresión.  
- Configuración de DNS para `www.parcial.juanplata.com`.  
- Verificación mediante:
  - **curl** (`Content-Encoding: gzip`).  
  - **Navegador (Opera)** con herramientas de red.  
  - **Wireshark**, confirmando cabeceras `Content-Encoding: gzip` y tráfico comprimido.  
- Comparación entre tráfico comprimido y no comprimido (ahorro de ancho de banda).

### Parte 3: Exposición del servidor web con Ngrok
- Instalación y configuración de **Ngrok**.  
- Creación de túnel en el puerto 80 (`ngrok http 80`).  
- Generación de URL pública accesible desde Internet.  
- Página personalizada `pagina_ngrok.html` en el virtualhost `parcial.juanplata.com`.  
- Acceso remoto validado desde dispositivo externo (móvil con datos).  

---

## Autor
- **Juan Plata**  
Estudiante de Ingeniería Informática  
Universidad Autónoma de Occidente  

