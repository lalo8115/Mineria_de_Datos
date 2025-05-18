# Práctica #7 - Agrupamiento de Datos con K-Means

**Materia:** Minería de Datos  
**Alumno:** Eulalio González Valencia  
**Matrícula:** 1994940  
**Profesor:** José Anastacio Hernández Saldaña  

---

## Objetivo

Aplicar la técnica de **K-Means Clustering** para agrupar automáticamente títulos de contenido en el catálogo de Netflix, usando como variables principales el **año de lanzamiento** y la **duración** (en minutos o temporadas aproximadas).

---

##  Dataset

Se utilizó el dataset `netflix_titles.csv`, que contiene información sobre títulos disponibles en la plataforma, incluyendo:

- Tipo (`Movie` o `TV Show`)
- Año de lanzamiento (`release_year`)
- Duración (`duration`)

---

##  Preparación de los Datos

- Se separaron películas y series.
- Se extrajo la duración numérica:
  - Para películas: minutos.
  - Para series: se estimó que 1 temporada ≈ 300 minutos.
- Se combinaron ambas categorías y se filtraron valores nulos.
- Se seleccionaron las variables `release_year` y `duration_value` para el análisis.

---

##  Modelo: K-Means Clustering

- Se aplicó escalado de datos con `StandardScaler`.
- Se utilizó el **método del codo** para determinar el número óptimo de clusters (`k`).
- Se entrenó el modelo con `k = 3`.
- Se visualizó la distribución de clusters en un gráfico de dispersión.

---

##  Resultados

- El modelo K-Means agrupó los títulos de Netflix en **3 clusters** distintos, basados en duración y año.
- Se identificaron posibles patrones como:
  - Contenidos recientes y cortos.
  - Producciones más antiguas y extensas.
  - Series con múltiples temporadas.

---

##  Visualización

Se incluyó un gráfico para representar los clusters resultantes, con color por grupo y ejes para año de lanzamiento y duración.

---

##  Conclusión

Esta práctica permitió aplicar K-Means en un contexto real de entretenimiento, mostrando cómo agrupar datos similares sin etiquetas previas. Esta técnica puede ser útil para segmentar contenido o sugerir agrupamientos en sistemas de recomendación.

---
