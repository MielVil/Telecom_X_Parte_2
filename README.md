# 📊 Predicción de Churn en Clientes de Telecomunicaciones  

## 📖 Descripción  
Este proyecto busca **predecir el churn (cancelación) de clientes** en una empresa de telecomunicaciones de LATAM. Mediante análisis exploratorio, tratamiento de variables y modelos de **Regresión Logística** y **Random Forest**, se identifican factores clave que influyen en la cancelación y se generan insights para estrategias de retención.  

---

## 🎯 Propósito del Análisis  
El objetivo principal es **identificar las variables más relevantes** que explican la cancelación de clientes y construir modelos predictivos que permitan **anticipar el churn**. Con esto se busca apoyar decisiones estratégicas de retención y fidelización.  

---

## 📂 Estructura del Proyecto  
├── TelecomX_LATAM_P2.ipynb # Cuaderno principal con el análisis

├── /data/ # Datos tratados en formato CSV

├── /visualizations/ # Gráficos y visualizaciones del EDA

└── /models/ # (Opcional) Modelos entrenados y resultados


---

## ⚙️ Preparación de los Datos  

### 1. Clasificación de Variables  
- **Categóricas**: género, tipo de contrato, método de pago, servicios adicionales (soporte técnico, protección de dispositivo, etc.).  
- **Numéricas**: antigüedad, cargos mensuales, cargos totales, meses de contrato.  

### 2. Normalización y Codificación  
- Escalado de variables numéricas con `StandardScaler`.  
- Codificación de variables categóricas con `OneHotEncoder (drop="first")`.  

### 3. División en Entrenamiento y Prueba  
- 70% entrenamiento, 30% prueba con `train_test_split`.  
- Uso de `random_state` para garantizar reproducibilidad.  

### 4. Justificación de Decisiones  
- **Regresión Logística**: para interpretar coeficientes y dirección de los efectos.  
- **Random Forest**: para capturar interacciones no lineales y evaluar importancia de variables.  
- **Balanceo de clases**: `class_weight="balanced"` para manejar desbalance entre churn y no churn.  

---

## 🔍 Exploración de Datos (EDA)  
Se realizaron análisis exploratorios que mostraron:  
- Contratos más largos reducen la probabilidad de cancelación.  
- Ciertos métodos de pago (ej. *electronic check*) incrementan el churn.  
- Clientes con cargos totales más altos son más propensos a cancelar.  
- Variables de servicios adicionales aportan valor predictivo.  

Ejemplos de gráficos incluidos en `/visualizations/`:  
- Histogramas de variables numéricas.  
- Barras comparativas de churn según variables categóricas.  
- Heatmap de correlación.  

---

## 🚀 Instrucciones de Ejecución  

### 1. Clonar el repositorio  

git clone https://github.com/usuario/telecom-churn.git
cd telecom-churn

## 2. Instalar dependencias

pip install -r requirements.txt

Bibliotecas principales:

pandas

numpy

matplotlib

seaborn

scikit-learn

## 3. Ejecutar el cuaderno

jupyter notebook TelecomX_LATAM_P2.ipynb

## 4. Cargar datos

Los datos tratados se encuentran en /data/datos_tratados.csv.


## ✅ Resultados Esperados

Identificar las variables más influyentes en la cancelación.

Comparar desempeño entre Regresión Logística y Random Forest.

Generar insights accionables para estrategias de retención.




