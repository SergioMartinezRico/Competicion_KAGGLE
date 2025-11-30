# Competicion_KAGGLE

# 💻 Predicción de Precios de Portátiles: Estrategia Competitiva para Cositas-Markt 📈

## 📝 Descripción del Proyecto

Nuestro objetivo es desarrollar un **Modelo de Machine Learning (ML)** capaz de predecir el precio de mercado de diversos **portátiles** basándose en sus características técnicas. Este proyecto surge de la necesidad estratégica de **Cositas-Markt** de obtener información competitiva sobre los precios de la competencia para optimizar su propia estrategia de precios.

El modelo resultante nos permitirá asignar precios competitivos a nuestro catálogo, asegurando un equilibrio entre la rentabilidad y el atractivo para el cliente.

## 🎯 Objetivo

El principal objetivo del proyecto es:

- Construir un modelo robusto de **regresión** para predecir la columna `Price_euros`.

---

## 💾 Dataset

Hemos trabajado con un dataset que contiene información detallada sobre una amplia variedad de portátiles. Los campos utilizados son:

| Columna                | Tipo de Dato | Descripción                                         |
| :--------------------- | :----------- | :-------------------------------------------------- |
| **`Company`**          | `String`     | Fabricante del portátil (ej: Dell, HP).             |
| **`Product`**          | `String`     | Marca y modelo.                                     |
| **`TypeName`**         | `String`     | Tipo de portátil (ej: Notebook, Gaming, Ultrabook). |
| **`Inches`**           | `Numeric`    | Tamaño de la pantalla en pulgadas.                  |
| **`ScreenResolution`** | `String`     | Resolución de la pantalla.                          |
| **`Cpu`**              | `String`     | Unidad Central de Procesamiento (CPU).              |
| **`Ram`**              | `String`     | Memoria RAM.                                        |
| **`Memory`**           | `String`     | Capacidad de almacenamiento (HDD/SSD).              |
| **`Gpu`**              | `String`     | Unidad de Procesamiento Gráfico (GPU).              |
| **`OpSys`**            | `String`     | Sistema Operativo.                                  |
| **`Weight`**           | `String`     | Peso del portátil.                                  |
| **`Price_euros`**      | `Numeric`    | **Variable Objetivo:** Precio en Euros.             |

---

## 🛠️ Metodología y Modelos

El proyecto se dividió en las siguientes fases clave:

### 1. Limpieza y Preprocesamiento de Datos

Se realizaron tareas cruciales de **Ingeniería de Características (Feature Engineering)** y limpieza para preparar los datos para los modelos de ML, incluyendo:

- **Conversión de Tipos:** Ajuste de columnas como `Inches` y `Weight`.
- **Extracción de Características:** Creación de nuevas variables a partir de columnas compuestas (`ScreenResolution`, `Ram`, `Memory`, `Cpu`, `Gpu`). Por ejemplo, extrayendo la velocidad de la CPU o el tipo de almacenamiento (SSD/HDD).
- **Codificación:** Aplicación de técnicas de codificación para variables categóricas.

### 2. Modelado

Se entrenaron y evaluaron diversos modelos de regresión para encontrar el mejor desempeño en la predicción de precios:

- **Regresión Lineal Simple:** Como modelo _baseline_.
- **Regresión Polinómica:** Para capturar relaciones no lineales entre las características y el precio.
- **Regresión Ridge:** Regresión lineal con regularización $L_2$ para mitigar el **sobreajuste (overfitting)**.
- **Regresión Lasso:** Regresión lineal con regularización $L_1$ que ayuda a la **selección de características (Feature Selection)**.

### 3. Evaluación

Los modelos fueron evaluados utilizando métricas de regresión clave, como:

- **Error Cuadrático Medio (MSE)**
- **Raíz del Error Cuadrático Medio (RMSE)**
- **Coeficiente de Determinación ($R^2$)**

---

## 🚀 Resultados Clave

El modelo de **Regresión Ridge** ha demostrado ser el más efectivo.

Las características que tienen mayor impacto en el precio son:

1.  **Tipo de GPU**
2.  **Capacidad de RAM**
3.  **Resolución de la Pantalla** (principalmente si es 4K)

---

## 📦 Tecnologías

- **Lenguaje:** Python
- **Librerías Principales:**
  - `pandas` (Manipulación de Datos)
  - `numpy` (Cálculos Numéricos)
  - `scikit-learn` (Modelos de Machine Learning)
  - `matplotlib` / `seaborn` (Visualización)

---

## 🧑‍💻 Autor

_(Sergio Martinez Rico)_

- [GitHub](https://github.com/SergioMartinezRico)
- [Contacto](https://www.linkedin.com/in/sergio-martinez-rico-)
