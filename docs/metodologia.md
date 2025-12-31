# Metodología del Análisis

## Enfoque general

El análisis se desarrolló con un enfoque de **Data Analytics aplicado a gestión ambiental**, priorizando la comprensión de los tiempos, estados administrativos y patrones generales de los sitios incluidos en la National Priorities List (NPL).

El objetivo no fue evaluar la eficiencia técnica de las remediaciones, sino **analizar el comportamiento histórico y actual del programa Superfund** desde una perspectiva de planificación y seguimiento.

---

## Organización de los datos

Se trabajó con una estructura clara de hojas dentro de Google Sheets:

- **01_Datos_Crudos**  
  Contiene el dataset original sin modificaciones, preservando la integridad de la fuente.

- **02_Datos_Trabajo**  
  Copia de trabajo utilizada para limpieza y transformación de datos.

- **03_Variables_Derivadas**  
  Cálculo de duraciones, clasificaciones y variables auxiliares.

- **04_Analisis**  
  Tablas dinámicas y resúmenes analíticos.

- **05_Dashboard**  
  KPIs y visualizaciones finales.

Esta separación permite **reproducibilidad, trazabilidad y control de cambios**.

---

## Limpieza y normalización de datos

Las principales tareas de limpieza incluyeron:

- Conversión de campos de fecha a formato fecha estándar.
- Normalización del estado de remediación:
  - *Remediado*
  - *Activo* (incluye sitios sin fecha de salida de la NPL).
- Revisión de valores nulos y consistencia entre fechas de ingreso y salida.

No se eliminaron registros del dataset original.

---

## Creación de variables derivadas

Se construyeron las siguientes variables clave:

- **Duración del proceso (días)**  
  Diferencia entre fecha de ingreso y fecha de salida de la NPL.

- **Duración del proceso (años)**  
  Conversión de días a años para facilitar la interpretación.

- **Fecha de fin de cálculo**  
  Para sitios activos, se utilizó la fecha actual del análisis como referencia.

- **Clasificación por duración**
  - Corta: < 2 años  
  - Media: 2–5 años  
  - Larga: 5–10 años  
  - Muy larga: > 10 años

- **Sitios activos de larga duración**  
  Identificación de sitios activos con más de 10 años en el programa.

---

## Indicadores y análisis exploratorio

Se construyeron KPIs orientados a responder preguntas de gestión:

- ¿Cuántos sitios siguen activos?
- ¿Qué proporción fue remediada?
- ¿Cuántos casos presentan duraciones extremadamente largas?
- ¿Existen diferencias relevantes entre regiones EPA o estados?

El análisis se apoyó en tablas dinámicas y visualizaciones sintéticas.

---

## Supuestos del análisis

- El tiempo de permanencia en la NPL se utiliza como **proxy de la duración del proceso de remediación**.
- Para sitios activos, la duración calculada representa una duración mínima.
- Se asume consistencia administrativa en los criterios de inclusión y exclusión de la NPL a lo largo del tiempo.

---

## Limitaciones

- El dataset no incluye información técnica sobre métodos de remediación.
- No se dispone de datos de costos, presupuesto ni cronogramas detallados.
- No se incorporan variables socioeconómicas o de impacto sanitario.
- El análisis se limita a la información administrativa disponible públicamente.

---

## Alcance del proyecto

Este proyecto tiene fines **analíticos y demostrativos**, orientado a portfolio profesional en Data Analytics, y no pretende reemplazar evaluaciones técnicas o regulatorias oficiales.

