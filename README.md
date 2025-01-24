# Prediccion_Tasa_de_Cancelacion_de_clientes

### Resumen del Proyecto: Predicción de Tasa de Cancelación de Clientes

En este proyecto se desarrolló un modelo predictivo para abordar un problema de clasificación binaria relacionado con la tasa de cancelación de clientes, utilizando **XGBoost** como modelo final. El objetivo principal fue construir un sistema confiable y robusto que permitiera identificar clientes en riesgo de cancelar sus suscripciones, facilitando estrategias proactivas de retención.

#### Principales Logros:
- **Modelado Final**: El modelo XGBoost ajustado logró un rendimiento consistente, con un **AUC-ROC de 0.8959 en validación** y **0.8818 en prueba**, superando el umbral crítico de 0.88 establecido como objetivo.
- **Capacidad de Generalización**: Las métricas de validación y prueba (Accuracy, Recall y F1-Score) demostraron que el modelo es robusto y generaliza bien, sin señales de sobreajuste.
- **Optimizaciones**: Se implementaron estrategias avanzadas como el ajuste dinámico del umbral de clasificación (entre 0.360 y 0.510) y la regularización (L1, L2 y scale_pos_weight), maximizando el rendimiento.

#### Flujo del Proyecto:
1. **Análisis Exploratorio de Datos (EDA)**:
   - Identificación de variables clave como tipo de contrato, características del servicio y cargos mensuales.
   - Manejo de valores faltantes y generación de nuevas columnas útiles (e.g., duración del contrato).
   - Reducción del ruido eliminando columnas redundantes y optimizando el dataset.

2. **Preparación de los Datos**:
   - Escalamiento de características a valores numéricos.
   - Manejo del desequilibrio de clases con técnicas como el ajuste de `scale_pos_weight`.

3. **Entrenamiento y Selección de Modelos**:
   - Comparación de diferentes algoritmos (XGBoost, Random Forest, etc.).
   - Selección de XGBoost como modelo final por su rendimiento superior en métricas clave.
   - Optimización exhaustiva de hiperparámetros mediante validación cruzada.

4. **Evaluación del Modelo**:
   - Métricas clave alcanzadas:
     | Métrica     | Entrenamiento | Validación | Prueba  |
     |-------------|---------------|------------|---------|
     | Accuracy    | 0.9049        | 0.8400     | 0.8061  |
     | Recall      | 0.7997        | 0.7679     | 0.7758  |
     | F1-Score    | 0.8169        | 0.7179     | 0.6802  |
     | AUC-ROC     | 0.9583        | 0.8959     | 0.8818  |

#### Conclusiones:
El proyecto cumplió con los objetivos planteados, logrando un modelo robusto y eficiente que identifica clientes en riesgo de cancelar su contrato con alta precisión. Las optimizaciones implementadas garantizan un rendimiento consistente, convirtiendo este modelo en una herramienta clave para estrategias de retención y satisfacción del cliente. 
