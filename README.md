# 📊 Telecom X — Parte 2: Predicción de Cancelación de Clientes

Este proyecto forma parte del desafío Telecom X y tiene como objetivo principal **predecir el churn (cancelación) de clientes** en una empresa de telecomunicaciones, utilizando variables relevantes del comportamiento y características del cliente. A través de técnicas de aprendizaje automático y análisis exploratorio, se identifican los factores que más influyen en la decisión de cancelar el servicio.

---

## 🧠 Propósito del Análisis

- Anticipar qué clientes tienen mayor probabilidad de cancelar su contrato.
- Identificar patrones y variables clave que explican el churn.
- Proponer estrategias de retención basadas en los resultados obtenidos.

---

## 📁 Estructura del Proyecto

TelecomX_Parte2/ │
├── TelecomX_Parte2_Modelado.ipynb # Cuaderno principal con todo el flujo del análisis
data
├── datos_tratados.csv # Dataset limpio y transformado 
README.md # Descripción del proyecto 

---

## 🧼 Preparación de los Datos

### 🔹 Clasificación de Variables

- **Categóricas:** Contract, PaymentMethod, InternetService, OnlineSecurity, TechSupport, PaperlessBilling, etc.
- **Numéricas:** tenure, Charges.Total, Cuentas_Diarias

### 🔹 Transformaciones Aplicadas

- **Codificación:** Variables categóricas fueron transformadas mediante One-Hot Encoding y binarización.
- **Normalización:** Se aplicó `StandardScaler` para modelos sensibles a escala (como Regresión Logística).
- **Separación de datos:** Se dividió el dataset en conjunto de entrenamiento (80%) y prueba (20%) usando `train_test_split`.

---

## ⚙️ Modelización y Justificaciones

Se entrenaron varios modelos de clasificación:

- **Regresión Logística:** Por su interpretabilidad y eficiencia en problemas lineales.
- **Random Forest:** Por su capacidad de capturar relaciones no lineales y manejar variables categóricas sin necesidad de normalización.

Ambos modelos obtuvieron un rendimiento perfecto en el conjunto de prueba. Se eligió **Random Forest** para el análisis de importancia de variables por su robustez y capacidad explicativa.

---

## 📊 Análisis Exploratorio (EDA)

Durante el EDA se generaron gráficos como:

- Histogramas de distribución de cargos y antigüedad
- Gráficos de barras para tipos de contrato y métodos de pago
- Matriz de correlación entre variables numéricas
- Comparación de cancelación según servicios contratados

**Insights clave:**

- Los clientes con contrato mensual y bajo tenure tienen mayor probabilidad de cancelar.
- El método de pago electrónico está asociado con mayor churn.
- La falta de soporte técnico y seguridad digital también influye negativamente.

---

## 🚀 Cómo Ejecutar el Cuaderno

### 🔧 Requisitos

Instala las siguientes bibliotecas antes de ejecutar el notebook:

```bash
pip install pandas scikit-learn matplotlib seaborn
📂 Carga de Datos
Asegúrate de tener el archivo datos_tratados.csv en el mismo directorio que el cuaderno. El notebook cargará los datos automáticamente desde ese archivo.

👤 Autor
Oscar Coello — Este proyecto refleja un enfoque reproducible, documentado y orientado a la toma de decisiones basada en datos.
