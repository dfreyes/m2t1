# m2t1
Modulo 2 Tarea 1: Taller: Contestando preguntas sobre los datos

### Objetivos del Proyecto
*   **Adquisición de datos:** Realizar la adquisición de una API de datos meteorológicos y visualizar los datos mediante la API de **Open-Meteo**.
*   **Exploración de datos:** Plantear preguntas sobre los datos y y contestarlas de forma visual.

---

### Fundamentos de ciencia de datos
Modulo 2 Tarea 1
|   |   |
| :--- | :--- |
| **Autor:** | Ing. Diego F. Reyes Y. |
| **Fecha:** | Septiembre 2026 |
| **Fuente de Datos:** | [Open-Meteo.com](https://open-meteo.com) *(API de acceso público)* |
---

Logistica de un vuelo seguro para drone DJI Mini 3
---
**Problema a resolver:**  
Se requiere identificar la o las mejores ventanas operativa para ejecutar el vuelo de un vuelo de drone a una altura de 80 m y a maxima velocidad horizontal de 16 m/s de manera segura, minimizando el riesgo que esta asociado a las condiciones de factores meteorológicos.

**Preguntas orientadoras a responder**

1. ¿Cuáles fueron las condiciones del tiempo en la zona de vuelo durante los últimos tres días?
2. Conforme al pronóstico del tiempo respecto a las variables meteorológicas para los próximos tres días, ¿Cuáles  son las condiciones del tiempo en la zona de vuelo?
3. ¿Cuál es la mejor rango horario para ejecutar el vuelo seguro del drone?

---

##Umbrales de seguridad del drone DJI Mini 3
---

| Variable Meteorológica | Umbral Operativo Máximo | Impacto en el Vuelo |
| :--- | :--- | :--- |
| **Velocidad de Viento** | 10.7 m/s | Límite de resistencia física del motor (Nivel 5). |
| **Precipitación** | 0.0 mm (Sin lluvia/nieve) | Riesgo de cortocircuito y pérdida de aerodinámica. |
| **Temperatura** | -10°C a 40°C | Degradación de batería o sobrecalentamiento. |
| **Visibilidad** | Despejado | Seguridad de transmisión y reducción de riesgo de choque con otros objetos. |

---

# Desarrollo del Análisis

---

El flujo trabajo sigue la siguiente ruta:

1. **Adquisición de Datos:** Conexión automatizada a la API y descarga del histórico y pronóstico  de variables meteorológicas.
2. **Revisión de la data:** Inspección del esquema, tipos de datos y verificación de valores nulos o anomalías.
3. **Análisis Exploratorio de Datos:** Procesamiento estadístico y visualización de variables críticas.
4. **Resolución de Preguntas:** Evaluación de umbrales operativos para la toma de decisiones.
---

**1. Adquisición de Datos:**

Se procede a solicitar la información meteorológica conforme la coordenada, las variables y la cantidad de días

---
**2. Cleaning Data**

Verificando las características del set de datos
Ver cuántas filas duplicadas existen en total
Filtra solo las columnas numéricas y cuenta cuántas celdas son menores a 0

---
**3. Exploratory Data Analysis**

Analizando y explorando los datos en función a las preguntas orientadoras
Ubicación de lugar de vuelo
*   Se analiza si se puede despegar y volar dada la altitud de la ubicación?
*   ¿Cual es el rango temporal del conjunto de datos meteorológicos?
*   Importación de librerías para gráficas.

*   Filtro de horario 08:00 a 16:30 tres días antes
*   Descripción de las características del tiempo en la zona de vuelo con el drone hace tres días.
*   Matriz de Correlación - Variables  meteorológicas
*   Una gráfica que analiza la Precipitación vs Probabilidad de Precipitación
*   Una gráfica que analiza la Gradiente Vertical: Umbral de Vientos Bajos 

*   Filtro de horario 08:00 a 16:30 tres días después
*   Descripción de las características del tiempo en la zona de vuelo con el drone  tres días después.
*   Una gráfica que analiza la Precipitación vs Probabilidad de Precipitación y ventana optima de vuelo
*   Una gráfica que analiza la Gradiente Vertical: Umbral de Vientos Bajos y ventana optima de vuelo

*   Filtro para definir cuál es la mejor hora del día para realizar un vuelo seguro con el drone.
*   Tablero que muestra  la mejor rango de hora del día para realizar un vuelo seguro con el drone.

---

