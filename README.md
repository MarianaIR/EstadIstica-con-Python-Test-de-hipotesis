# ✅ ESTADÍSTICA CON PYTHON: TEST DE HIPÓTESIS

[![Python](https://img.shields.io/badge/Python-3670A0?style=flat&logo=python&logoColor=ffdd54)](https://www.python.org/)  
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)](https://pandas.pydata.org/)  
[![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)](https://numpy.org/)  
[![SciPy](https://img.shields.io/badge/SciPy-8DAA90?style=flat&logo=scipy&logoColor=white)](https://scipy.org/)

Este proyecto es la **Parte 3** del curso de **Estadística con Python**. Se enfoca en la **Estadística Inferencial** avanzada, específicamente en el **Test de Hipótesis**, la técnica que permite a los Data Scientists tomar decisiones basadas en datos al aceptar o rechazar afirmaciones sobre una población.

---

## 🧠 Contenido del Proyecto

### 1️⃣ Fundamentos del Test de Hipótesis
- **Definición:** Un **Test de Hipótesis** es un procedimiento estadístico que se utiliza para decidir si una determinada afirmación (hipótesis) sobre un parámetro poblacional es razonable o no.
- **Tipos de Hipótesis:**
    * **Hipótesis Nula (H₀):** Representa la afirmación que se asume cierta a menos que la evidencia empírica sugiera lo contrario.
    * **Hipótesis Alternativa (H₁):** Es la negación de H₀; lo que se busca probar.
- **Errores:** Se definen los errores que pueden ocurrir: **Error Tipo I (rechazar H₀ siendo cierta)** y **Error Tipo II (no rechazar H₀ siendo falsa)**.
- **Nivel de Significación ($\alpha$):** Es la **probabilidad máxima de cometer un Error Tipo I** (ej. se utiliza $\alpha = 0.05$ o 5%).

### 2️⃣ Pruebas de Comparación y Metodología
- **Caso de Uso:** Se analiza si el **rendimiento escolar promedio** es diferente entre dos grupos: alumnos que practican ejercicios físicos y aquellos que no.
- **Métrica de Decisión (P-valor):** La decisión se toma comparando el P-valor (la probabilidad de obtener el resultado observado, asumiendo que H₀ es cierta) con el nivel de significación ($\alpha$):
    * **Si P-valor $\le \alpha$:** Se **Rechaza H₀**.
    * **Si P-valor $> \alpha$:** Se **No rechaza H₀** (no hay suficiente evidencia).

### 3️⃣ Implementación de Tests Específicos
El proyecto implementa tests para diferentes escenarios:

| Test Utilizado | Propósito | Librería | Resultado Típico |
|:---:|:---:|:---:|:---:|
| **Test t (Student)** | Se utiliza para comparar la media de una muestra con la media poblacional, o la diferencia entre las medias de dos grupos, asumiendo una distribución normal. | `scipy.stats.ttest_ind` | Se determina si hay una diferencia estadísticamente significativa en el rendimiento promedio. |
| **Test de Mann-Whitney U** | Es una **prueba no paramétrica** (utilizada cuando los datos no siguen una distribución normal) para comparar la diferencia entre dos muestras independientes. | `scipy.stats.mannwhitneyu` | Se decide si el rendimiento de un grupo es superior al otro, sin depender de la normalidad. |

- **Conclusión del Ejemplo:** En el ejemplo del rendimiento escolar, la prueba de Mann-Whitney U resultó en **"No rechace H₀"** (P-valor $> 0.10$), concluyendo que **no hay suficiente evidencia** para afirmar que el rendimiento escolar de los alumnos que practican ejercicio es superior.

---

## 🛠️ Librerías Utilizadas

| Librería       | Uso principal                               |
|----------------|---------------------------------------------|
| **SciPy.stats**| Implementación de los tests estadísticos paramétricos y no paramétricos (`ttest_ind`, `mannwhitneyu`)|
| **Pandas**     | Manejo y estructuración de los datos de las muestras|

---

## 🎯 Objetivo del Proyecto
Dominar la metodología del **Test de Hipótesis** como herramienta de **toma de decisiones**. El proyecto proporciona la capacidad de formular, implementar y concluir pruebas estadísticas, permitiendo a los analistas utilizar el **P-valor** para hacer afirmaciones rigurosas sobre la población.

---

## 📈 Resultados Clave
- Se demuestra el flujo completo para **aceptar o rechazar la Hipótesis Nula (H₀)** en función del P-valor.
- Se utiliza el **Test t** para escenarios paramétricos y el **Test de Mann-Whitney U** para escenarios no paramétricos.
- El proyecto concluye con un **ejemplo práctico** donde la evidencia no es suficiente para confirmar la hipótesis de que el ejercicio mejora el rendimiento escolar, ilustrando la aplicación del método científico en el análisis de datos.

