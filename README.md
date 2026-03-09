# Challenge-Alura_Telecomx2
Desafio Alura Telecomx Parte 2

# 🤖 Machine Learning: Predicción de Cancelación (Churn) - Telecom X

![Python](https://img.shields.io/badge/python-3.x-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/library-sklearn-orange.svg)
![Pandas](https://img.shields.io/badge/library-pandas-green.svg)
![Imbalanced-Learn](https://img.shields.io/badge/library-imblearn-red.svg)

## 📌 Escenario del Proyecto (Parte 2)
Tras la fase de análisis exploratorio (EDA), el objetivo de esta segunda etapa fue construir un pipeline de **Machine Learning** capaz de predecir qué clientes tienen mayor probabilidad de abandonar Telecom X. 

El enfoque principal fue pasar del análisis descriptivo a la **inteligencia predictiva**, permitiendo a los equipos de retención y marketing anticiparse a la fuga de clientes con estrategias basadas en datos.

## 🛠️ Pipeline y Tecnologías Utilizadas
* **Preprocesamiento:** * `One-Hot Encoding` para transformar variables categóricas.
  * `StandardScaler` para la normalización de variables numéricas.
  * `SMOTE` para el balanceo de clases (mitigando el desbalance del 73% vs 26%).
* **Modelado Predictivo:**
  * Regresión Logística.
  * Random Forest (Bosque Aleatorio).
* **Evaluación:** Matrices de Confusión, Exactitud (Accuracy), Precisión y Recall.

## 🏆 Evaluación de Modelos
El modelo ganador fue el **Random Forest**. 
* Logró identificar correctamente a **1347 clientes en riesgo** (Verdaderos Positivos) en el set de prueba, superando a la regresión logística. 
* Aunque presentó cierta tendencia al sobreajuste (*overfitting*) en los datos de entrenamiento debido a su profundidad, su capacidad predictiva y su alto *Recall* resultaron ser los más útiles para minimizar las pérdidas del negocio.

## 📊 Factores Críticos de Cancelación (Insights)
El análisis de la importancia de variables del Random Forest y los coeficientes de la Regresión Logística revelaron tres ejes fundamentales:
1. **El Factor Tiempo (`Meses_Contrato`):** Es la variable de mayor impacto. El riesgo de fuga se concentra drásticamente en los primeros meses.
2. **El Factor Económico (`Gasto_Total` y `Gasto_Mensual`):** El peso de la factura es el segundo motor de cancelación.
3. **El Escudo del Contrato:** Los contratos a uno o dos años (`Tipo_Contrato`) actúan como una fuerte barrera de retención frente a los contratos de renovación mensual.

## 💡 Recomendaciones Estratégicas
1. **Onboarding Blindado:** Invertir en la experiencia del usuario durante los primeros 6 meses. Implementar beneficios exclusivos que se desbloqueen al cumplir el primer año.
2. **Migración de Contratos:** Lanzar campañas para convertir a los clientes "Mes a Mes" en clientes anuales, absorbiendo costos iniciales o regalando meses de servicio.
3. **Auditoría de Valor VIP:** Los clientes con mayor gasto mensual son propensos a buscar alternativas más económicas. Se debe asegurar atención prioritaria y servicios de valor agregado (`Soporte_Tecnico`, `Seguridad_Online`) para fidelizar este segmento.

---
**Desarrollado por (https://github.com/lucioquildrian)** *| Apasionado por la optimización de procesos, el análisis de datos y la estrategia de negocios.*
