# README

## Project Overview

This project utilizes a dataset on housing prices in Boston to perform exploratory data analysis (EDA) and build a linear regression model to predict housing prices. The analysis aims to uncover the relationships between various features of houses and their corresponding prices.

## Descripción del Proyecto

Este proyecto utiliza un conjunto de datos sobre precios de viviendas en Boston para realizar un análisis exploratorio de datos (EDA) y construir un modelo de regresión lineal para predecir los precios de las viviendas. El análisis tiene como objetivo descubrir las relaciones entre varias características de las casas y sus respectivos precios.

## Dataset Description

The dataset contains information about various characteristics of houses in Boston, including:

- **PRICE**: Value of the house.
- **RM**: Average number of rooms per house.
- **DIS**: Weighted distance to five employment centers in Boston.
- **NOX**: Concentration of nitrogen oxides (measured in parts per 10 million).
- **LSTAT**: Percentage of the population with lower education levels.
- **RAD**: Accessibility to highways.
- **CHAS**: Location next to the Charles River.

The goal of the analysis is to understand the distribution of prices and the relationships between different characteristics of the houses.

## Descripción del Conjunto de Datos

El conjunto de datos contiene información sobre varias características de las viviendas en Boston, que incluyen:

- **PRICE**: Valor de la vivienda.
- **RM**: Promedio de habitaciones por vivienda.
- **DIS**: Distancia ponderada a cinco centros de empleo en Boston.
- **NOX**: Concentración de óxidos de nitrógeno (medida en partes por 10 millones).
- **LSTAT**: Porcentaje de la población con un nivel de educación menor.
- **RAD**: Accesibilidad a las autopistas.
- **CHAS**: Ubicación junto al río Charles.

El objetivo del análisis es entender la distribución de precios, así como la relación entre diferentes características de las viviendas.

## Methodology

### Exploratory Data Analysis (EDA)

1. **Data Visualization**: We used various plots (like histograms, scatter plots, and box plots) to visualize the distributions of the features and the target variable (house prices). This helps identify patterns and potential outliers.
  
2. **Correlation Analysis**: We calculated correlation coefficients to assess the strength and direction of relationships between features and the target variable.

### Análisis Exploratorio de Datos (EDA)

1. **Visualización de Datos**: Utilizamos varios gráficos (como histogramas, diagramas de dispersión y diagramas de caja) para visualizar las distribuciones de las características y de la variable objetivo (precios de las viviendas). Esto ayuda a identificar patrones y posibles valores atípicos.
  
2. **Análisis de Correlación**: Calculamos coeficientes de correlación para evaluar la fuerza y dirección de las relaciones entre características y la variable objetivo.

### Regression Analysis

To predict housing prices, we implemented two types of regression models: 

1. **Linear Regression on Original Prices**: 
   - This model was trained on the original price data. We examined the relationship between features (like the number of rooms, proximity to the river, etc.) and the price of houses. 
   - **R-squared**: We used R-squared as a metric to evaluate how well our model fits the data. An R-squared value close to 1 indicates a good fit.

2. **Logarithmic Transformation of Prices**:
   - To stabilize the variance and normalize the distribution of the target variable, we transformed the price data using the natural logarithm (`log(price)`). This approach often helps improve the performance of linear regression models, especially in the presence of heteroscedasticity (when the variance of errors differs across levels of an independent variable).
   - We then trained a linear regression model using the transformed target variable.
   - **Evaluation**: We compared the R-squared values of the original and logarithmic models to assess which one provided a better fit.

### Análisis de Regresión

Para predecir los precios de las viviendas, implementamos dos tipos de modelos de regresión:

1. **Regresión Lineal sobre Precios Originales**: 
   - Este modelo fue entrenado con los datos de precios originales. Examinamos la relación entre características (como el número de habitaciones, la proximidad al río, etc.) y el precio de las viviendas. 
   - **R-cuadrado**: Utilizamos R-cuadrado como métrica para evaluar qué tan bien se ajusta nuestro modelo a los datos. Un valor de R-cuadrado cercano a 1 indica un buen ajuste.

2. **Transformación Logarítmica de Precios**:
   - Para estabilizar la varianza y normalizar la distribución de la variable objetivo, transformamos los datos de precios utilizando el logaritmo natural (`log(precio)`). Este enfoque a menudo ayuda a mejorar el rendimiento de los modelos de regresión lineal, especialmente en presencia de heteroscedasticidad (cuando la varianza de los errores difiere según los niveles de una variable independiente).
   - Luego, entrenamos un modelo de regresión lineal utilizando la variable objetivo transformada.
   - **Evaluación**: Comparamos los valores de R-cuadrado de los modelos original y logarítmico para evaluar cuál proporcionó un mejor ajuste.

### Model Evaluation

- We evaluated both models using residual analysis to check for patterns that might indicate problems with the model fit.
- Residual plots were generated to visualize the distribution of errors. A random spread of residuals suggests a good model fit, while any systematic patterns might indicate issues.

### Evaluación del Modelo

- Evaluamos ambos modelos utilizando el análisis de residuos para verificar patrones que podrían indicar problemas con el ajuste del modelo.
- Se generaron gráficos de residuos para visualizar la distribución de errores. Una dispersión aleatoria de los residuos sugiere un buen ajuste del modelo, mientras que patrones sistemáticos pueden indicar problemas.

## Dependencies

Ensure you have the following libraries installed in your Python environment:

- `pandas`
- `numpy`
- `seaborn`
- `plotly`
- `matplotlib`
- `scikit-learn`

You can install them using pip:

```bash
pip install pandas numpy seaborn plotly matplotlib scikit-learn
