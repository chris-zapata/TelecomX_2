# 🛡️ TELECOMX PARTE 2: Predicción de Cancelación de Clientes (Churn Analysis)
**Autor: Christopher Zapata**

Este proyecto utiliza técnicas de Machine Learning para identificar a los clientes con mayor probabilidad de abandonar una empresa de telecomunicaciones, permitiendo diseñar estrategias de retención basadas en datos.

## 📊 Resumen del Proyecto
El objetivo principal es clasificar si un cliente cancelará su servicio (Churn) analizando su comportamiento histórico, servicios contratados y datos demográficos.

## 🛠️ Tecnologías Utilizadas
* Python (Pandas, NumPy)
* Visualización: Matplotlib & Seaborn
* Scikit-Learn:
  * Logistic Regression
  * K-Nearest Neighbors (KNN)
  * Decision Trees
  * Random Forest

## 📈 Hallazgos Principales (EDA)
A través del Análisis Exploratorio de Datos, se identificaron factores críticos:

* Antigüedad (Tenure): Los clientes nuevos tienen una tasa de abandono significativamente mayor.
* Cargos Mensuales: Existe una correlación positiva entre facturas altas y la probabilidad de fuga.
* Servicio de Internet: Los usuarios de Fibra Óptica presentan un riesgo de cancelación más elevado que los de DSL.

## 🤖 Modelos Evaluados
Se entrenaron y compararon diversos algoritmos, aplicando normalización para modelos de distancia y balanceo de clases para mejorar la detección de la clase minoritaria:

| Modelo | Accuracy | Recall (Clase: Yes) | F1-Score (Clase: Yes) |
| :--- | :---: | :---: | :---: |
| **Regresión Logística (Balanced)** | 0.74 | **0.79** | 0.62 |
| **Random Forest (Balanced)** | **0.78** | 0.74 | **0.64** |
| **Árbol de Decisión** | 0.78 | 0.59 | 0.59 |
| **KNN (K-Nearest Neighbors)** | 0.76 | 0.48 | 0.52 |

Conclusión: Se seleccionó el Random Forest como el modelo más equilibrado por su capacidad para manejar relaciones no lineales y su precisión en la identificación de factores de riesgo.

## 💡 Estrategias de Retención Sugeridas
1. Fidelización Temprana: Campañas dirigidas a clientes con menos de 12 meses de antigüedad.
2. Revisión de Fibra Óptica: Analizar la calidad/precio del servicio técnico en este segmento.
3. Incentivos de Contrato: Promover la migración de contratos mensuales a anuales mediante beneficios exclusivos.

## 🚀 Cómo ejecutarlo
1. Clona este repositorio.
2. Asegúrate de tener instaladas las librerías: pip install pandas scikit-learn seaborn matplotlib.
3. Abre el archivo .ipynb en Jupyter Notebook o Google Colab y ejecuta todas las celdas.
