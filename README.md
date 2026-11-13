# Fundación YPF - Data Science: Análisis de Tasas de Promoción Escolar (2012-2023)

**Alumnas:** Florencia Zoni, Virginia Contreras  
**Programa:** Ciencia de Datos - Fundación YPF  

---

## 📌 Descripción del Proyecto

Este repositorio contiene el trabajo final de Data Science, cuyo objetivo es analizar y modelar las **tasas de promoción efectiva** de los estudiantes en las distintas jurisdicciones de Argentina entre los años 2012 y 2023.

El estudio se divide en dos grandes etapas metodológicas:
1. **Supervisada (Regresión Lineal Múltiple):** Predicción de la tasa total de promoción del nivel secundario para el año siguiente ($t+1$) basándose en los indicadores del año actual ($t$).
2. **No Supervisada (Clustering):** Agrupamiento de las provincias argentinas según sus patrones históricos y perfiles de promoción en los distintos años escolarizados (1° a 6° de primaria y 8° a 12° de secundaria).

---

## 📂 Dataset

* **Nombre:** `Tasa_de_Promocion_Efectiva_2012-2023_unificada.xlsx`
* **Fuente:** Registros oficiales del sistema educativo argentino (2012–2023).
* **Unidades:** 24 jurisdicciones provinciales (se excluyen agregados como *Total País*, *Conurbano* y *Resto de Bs As* en la fase de clustering para evitar duplicidad).

---

## 🚀 Estructura del Trabajo

### Parte 1: Regresión Lineal Múltiple (Modelado Predictivo)
* **Objetivo:** Predecir `Secundaria_Total_Siguiente` ($t+1$).
* **División Temporal:** 
  * *Entrenamiento (Train):* Años $\le 2018$.
  * *Prueba (Test):* Años $> 2018$.
* **Métricas de Evaluación:**
  * **MAE (Error Absoluto Medio):** 4.76 p.p.
  * **RMSE:** 6.12 p.p.
  * **$R^2$:** 0.68

### Parte 2: Clustering (Aprendizaje No Supervisado)
* **Objetivo:** Identificar agrupamientos de provincias con trayectorias escolares similares.
* **Algoritmos Comparados:** K-Means (modelo base), Clustering Jerárquico (Ward) y DBSCAN.
* **Modelo Final:** K-Means sobre componentes principales (PCA, 4 componentes, $k=3$).
* **Clusters Identificados ($k=3$):**
  1. *Cluster 0 - Promoción alta y sostenida en secundaria inicial.*
  2. *Cluster 1 - Promoción media/baja con mayor caída en los últimos años.*
  3. *Cluster 2 - Desempeño crítico con altas tasas de no promoción.*

---

## 🛠️ Tecnologías Utilizadas

* **Lenguaje:** Python 3.x
* **Librerías principales:**
  * `pandas`, `numpy` (Manipulación de datos)
  * `scikit-learn` (Modelos de regresión, PCA, K-Means, DBSCAN, jerárquico y métricas)
  * `matplotlib`, `seaborn` (Visualización de datos)

---

## ⚙️ Instrucciones para Ejecutar

1. Clonar el repositorio:
   ```bash
   git clone [https://github.com/tu-usuario/Curso-Data-Science/Mi-proyecto.git

   
