## 🚗 Predicción de Precios de Coches de Segunda Mano

![R](https://img.shields.io/badge/R-%23276DC3.svg?style=for-the-badge&logo=r&logoColor=white)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Supervisado-orange?style=for-the-badge)

### 📌 Descripción del Proyecto
Este proyecto tiene como objetivo desarrollar una **herramienta de apoyo a la toma de decisiones para concesionarios**. A través del análisis de datos y la aplicación de algoritmos de Machine Learning, estimamos el precio de mercado de vehículos de segunda mano en India. 

El modelo permite a los negocios automovilísticos ajustar sus precios de compra y venta basándose en características objetivas del vehículo.

### 🗂️ El Dataset
Utilizamos el conjunto de datos `car_price.csv`, que contiene alrededor de 7.400 registros de vehículos usados y 18 columnas. Algunas de las variables clave analizadas incluyen:
* `yr_mfr`: Año de fabricación.
* `kms_run`: Kilómetros recorridos.
* `body_type` y `fuel_type`: Tipo de carrocería y combustible.
* `sale_price`: Nuestra variable objetivo (Target).

### 🧠 Modelos y Metodología
El proyecto se desarrolló en **R** siguiendo estas fases:
1. **Depuración y EDA (Análisis Exploratorio de Datos):** Limpieza de valores nulos, recodificación de variables categóricas y análisis de correlaciones.
2. **Entrenamiento de Modelos:** Se probaron y compararon varios algoritmos de aprendizaje supervisado:
   * Regresión Lineal (StepBIC)
   * Árboles de Decisión (Podados)
   * Random Forest
   * Gradient Boosting


### 📊 Resultados Principales
Tras evaluar las métricas de rendimiento en los conjuntos de entrenamiento (Train) y prueba (Test), los modelos de ensamblaje (Ensembles) demostraron una clara superioridad:

* **Regresión StepBIC:**
  - $R^2$ Train = 0.7034 
  - $R^2$ Test = **0.7044** (Sin sobreajuste, pero bajo poder predictivo).
* **Modelo penalizado (ENET):** Seleccionamos un modelo LASSO.
  - $R^2$ Train = 0.6850
  - $R^2$ Test = **0.6796**
* **Árbol Podado:**
  - $R^2$ Train = 0.6571.
  - $R^2$ Test = **0.6282.**
* **Random Forest:**
  - $R^2$ Train = 0.9066 
  - $R^2$ Test = **0.8475** 
* **🏆Gradient Boosting:** (Mejor equilibrio. Logra capturar la complejidad de los datos con un sobreajuste mínimo de solo 0.05 puntos respecto a train).
  - $R^2$ Train = 0.9150
  - $R^2$ Test = **0.8621**


**Conclusión de negocio:** A medida que aumenta el año de fabricación (vehículos más nuevos), el valor medio predicho aumenta de forma consistente en todos los tipos de carrocería. El modelo *Gradient Boosting* es el candidato ideal para ser desplegado en el concesionario, puesto que, además de ser el que obtiene mejores resultados en cuanto a capacidad predictiva, la complejidad que escode este tipo de modelo de Matching Learning nos permite ajustarnos mejor a esta clase de toma de decisiones.

### 🚀 Cómo ejecutar este proyecto
1. Clona este repositorio: `git clone https://github.com/laulop27/prediccion-precios-coches.git`
2. Abre el script principal **TRABAJOgrupal.qmd** en **RStudio**.
3. Asegúrate de tener instaladas las librerías necesarias (ej. `randomForest`, `gbm`, `rpart`, `ggplot2`).
4. Ejecuta el código paso a paso para reproducir la limpieza de datos y el entrenamiento de los modelos.

---
*Trabajo realizado por: Marcos Martínez, Laura López, Marina Parra, Verónica Yebra y Rodrigo Castillo.*
