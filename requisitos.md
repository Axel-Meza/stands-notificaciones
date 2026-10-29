# Especificación de Requisitos: Sistema de Notificaciones

## 1. Requisitos Funcionales (RF)

| ID | Característica / Nombre | Descripción | Prioridad |
| :--- | :--- | :--- | :---: |
| **RF-01** | **Evaluación de Reserva** | El sistema debe comparar la fecha de ejecución actual con la fecha de expiración de la reserva de cada stand para determinar los días restantes de vigencia. | Alta |
| **RF-02** | **Evaluación de Pronto Pago** | El sistema debe calcular el tiempo restante hacia la fecha límite del descuento de pronto pago y evaluar si el beneficio sigue activo para la editorial. | Alta |
| **RF-03** | **Evaluación de Límite de Liquidación** | El sistema debe contrastar la fecha actual contra la fecha máxima permitida para cubrir el costo total del stand. | Alta |
| **RF-04** | **Umbral de Alerta Anticipada** | El motor lógico debe disparar una notificación de advertencia únicamente si la diferencia entre la fecha actual y la fecha objetivo se encuentra dentro de un margen predefinido (ej. 3 días de anticipación). | Alta |
| **RF-05** | **Salida por Consola** | El programa debe imprimir los avisos resultantes directamente en la interfaz de línea de comandos, detallando el tipo de alerta, el nombre de la editorial, el ID del stand afectado y el tiempo restante exacto. | Alta |
| **RF-06** | **Inyección de Datos de Prueba** | El sistema debe permitir la creación en memoria (instanciación en código) de un conjunto mínimo de objetos interrelacionados con parámetros controlados para demostrar el motor lógico. | Media |

<br>

## 2. Requisitos No Funcionales (RNF)

| ID | Atributo de Calidad | Descripción | Prioridad |
| :--- | :--- | :--- | :---: |
| **RNF-01** | **Entorno y Tecnologías** | El módulo debe estar diseñado para compilarse y ejecutarse exclusivamente mediante consola (terminal), empleando POO y evitando dependencias de interfaces gráficas. | Alta |
| **RNF-02** | **Diseño y Mantenibilidad** | La arquitectura del código base debe mantener un bajo acoplamiento, separando estrictamente la definición de las estructuras de datos (modelo) de la clase encargada de la lógica. | Alta |
| **RNF-03** | **Rendimiento** | Al prescindir de conexiones a bases de datos, el análisis de fechas y la impresión de las notificaciones de los datos de prueba deben ejecutarse de manera instantánea en consola. | Media |