# Simulación del Flujo de Ventas de Tiendas Argentinas y visualizacion en Druid

## Introducción
El presente documento proporciona una descripción detallada del proyecto que simula el flujo de ventas de varias tiendas argentinas. El objetivo principal del proyecto es generar datos aleatorios de ventas en tiempo real, incluyendo información sobre el tipo de pago, el producto comprado, el estado de la transacción y la plataforma desde donde se realizó la compra. Estos datos se envían a Confluence mediante Kafka y se pueden consultar en streaming utilizando Apache Druid, que se encuentra alojado en una instancia de Google Cloud.

## Objetivos
El objetivo principal de este proyecto es simular el flujo de ventas de tiendas argentinas para generar datos aleatorios que permitan realizar análisis en tiempo real. Los objetivos específicos incluyen:

Generar datos aleatorios de ventas con información relevante como tipo de pago, producto comprado, estado de la transacción y plataforma de compra.

Enviar los datos generados a Confluence utilizando Kafka para su almacenamiento.

Utilizar Apache Druid para realizar consultas en streaming sobre los datos almacenados en Confluence.

## Arquitectura del Proyecto
El proyecto se basa en la siguiente arquitectura:
### 3.1. Generación de Datos de Ventas:

Se utilizará una función de Python para generar datos aleatorios de ventas.
La función generará información sobre el tipo de pago, producto comprado, estado de la transacción y plataforma de compra.
Los datos se generarán cada 1 o 2 segundos para simular un flujo continuo de ventas en tiempo real.

### 3.2. Envío de Datos a Confluence:

Se utilizará Kafka para enviar los datos generados a Confluence.
Kafka garantiza una entrega confiable y eficiente de los datos en tiempo real.

### 3.3. Almacenamiento y Procesamiento en Confluence:

Confluence actuará como el almacenamiento principal de los datos de ventas generados.
Los datos se almacenarán en formato de eventos y se organizarán en los temas de Confluence.
Confluence proporciona una interfaz amigable para la consulta y visualización de los datos almacenados.

### 3.4. Consultas en Streaming con Apache Druid:

Apache Druid se utilizará para realizar consultas en streaming sobre los datos almacenados en Confluence.
Druid es una base de datos en tiempo real optimizada para consultas analíticas.
Se configurarán los esquemas y las consultas adecuadas en Druid para permitir el análisis de los datos de ventas en tiempo real.

### 3.5. Alojamiento en Google Cloud:

Apache Druid se alojará en una instancia de Google Cloud.
Google Cloud proporciona un entorno confiable y escalable para alojar la infraestructura de Druid.
Se configurarán los recursos necesarios en Google Cloud para garantizar un rendimiento óptimo de Apache Druid.

## Conclusiones
El proyecto de simulación del flujo de ventas de tiendas argentinas utilizando Python, Kafka, Confluence y Apache Druid tiene como objetivo generar datos de ventas aleatorios en tiempo real y permitir su análisis en streaming. Con esta solución, las tiendas pueden obtener información valiosa sobre sus ventas y tomar decisiones bas