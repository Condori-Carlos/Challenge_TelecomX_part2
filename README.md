# 📊 Predicción de Churn - TelecomX LATAM (Parte 2)

## 1. 📌 Propósito del Análisis
El objetivo principal de este proyecto es **predecir la cancelación de clientes (Churn)** en una empresa de telecomunicaciones ficticia llamada **TelecomX LATAM**.  
A través del uso de técnicas de Machine Learning y un proceso de preparación de datos robusto, buscamos identificar las **variables más relevantes** que influyen en la decisión de un cliente de abandonar el servicio, con el fin de implementar estrategias efectivas de **retención**.

---

## 2. 📂 Estructura del Proyecto
El proyecto está organizado de la siguiente forma:

- `TelecomX_part2_LATAM.ipynb` → Cuaderno principal donde se realiza la limpieza de datos, preparación de variables, modelización y evaluación de resultados.  
- `Data/datos_tratados.csv` → Conjunto de datos ya procesados y listos para el modelado.  
- `Visualizaciones/` → Carpeta opcional donde se pueden guardar gráficos y resultados de las evaluaciones de modelos.  
- `README.md` → Documento actual con la descripción general del proyecto.

---

## 3. 🔧 Proceso de Preparación de los Datos

### a) Clasificación de Variables
- **Categóricas**: Género, método de pago, tipo de contrato, servicios adicionales (internet, soporte técnico, streaming, etc.).  
- **Numéricas**: Tenure (meses de permanencia), cargos mensuales (`MonthlyCharges`), cargos totales (`TotalCharges`), etc.  

### b) Normalización y Codificación
- Se aplicó **Label Encoding** para variables categóricas.  
- Se eliminaron variables redundantes como `Charges.daily` tras verificar correlación con `tenure` y `Charges.Monthly`.  

### c) División del Dataset
- Los datos se dividieron en **entrenamiento (train)** y **prueba (test)** usando `train_test_split` con una proporción estándar (ej. 70%-30%).  

### d) Justificación de Decisiones
- Se utilizó **SMOTE (Synthetic Minority Over-sampling Technique)** para balancear la variable objetivo `Churn`, debido a la desproporción de clases.  
- Se probaron distintos algoritmos de clasificación (Random Forest, Árboles de Decisión, KNN), evaluando métricas como **precision, recall, f1-score y matriz de confusión**.  
- Se priorizó la **interpretabilidad de resultados** junto con el rendimiento del modelo.

---

## 4. ▶️ Instrucciones de Ejecución

### a) Requisitos Previos
Instala las siguientes bibliotecas de Python:

```bash
pip install pandas scikit-learn imbalanced-learn matplotlib seaborn jupyter
```
### b) Ejecución del Proyecto
1. Clonar este repositorio en tu máquina local:

```bash
git clone https://github.com/tu_usuario/telecomx-churn-prediction.git
cd telecomx-churn-prediction
```
2. Abrir el cuaderno con Jupyter:
```bash
jupyter notebook TelecomX_part2_LATAM.ipynb
```
3. Cargar los datos tratados desde la carpeta /Data:
```bash
datos = pd.read_csv("Data/datos_tratados.csv")
   ```
4. Ejecutar las celdas en orden para reproducir el flujo de preparación, modelado y evaluación de resultados
## ✍️ Proyecto realizado como continuación del análisis exploratorio de TelecomX LATAM, enfocado en la predicción de churn mediante Machine Learning.

Condori Carlos
