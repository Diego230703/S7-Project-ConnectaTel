# ConnectaTel Latam – Análisis de Comportamiento y Segmentación de Clientes

Este repositorio contiene el proyecto de análisis exploratorio, procesamiento de datos y evaluación del comportamiento de los clientes de **ConnectaTel**, una empresa de telecomunicaciones en Latinoamérica.

---

## 🎯 Objetivo del proyecto

El objetivo principal de este proyecto es analizar el comportamiento de consumo de los usuarios de ConnectaTel para identificar patrones de uso, diagnosticar y corregir problemas de calidad de los datos (valores nulos, *sentinels* y anomalías temporales) y generar *insights* estratégicos que permitan optimizar los planes tarifarios y mejorar las estrategias de retención de clientes (*churn*).

---

## 📊 Datasets utilizados

El análisis se fundamenta en tres fuentes de datos integradas (`/datasets/`):

1. **`plans.csv`**: Información sobre las tarifas y beneficios de los planes ofrecidos (plan *Básico* y plan *Premium*), incluyendo límites de minutos, mensajes y datos, así como los costos por exceso de consumo.
2. **`users_latam.csv`**: Registro demográfico y contractual de los clientes (ID de usuario, nombre, edad, ciudad de residencia, fecha de alta, fecha de baja y tipo de plan contratado).
3. **`usage.csv`**: Histórico detallado de consumo por usuario, con métricas agregadas de llamadas realizadas, duración total de las llamadas (en minutos) y cantidad de mensajes de texto enviados.

---

## 🛠️ Etapas del análisis realizadas

1. **Diagnóstico y Limpieza de Datos:**
   - Identificación y tratamiento de valores faltantes y valores centinela (*sentinels* como `-999` en edades o `?` en ubicaciones).
   - Corrección de anomalías en fechas (registros fuera de rango o con años futuros).
   - Estandarización de tipos de datos (`datetime`, enteros y flotantes).
2. **Ingeniería de Características y Agregación:**
   - Agregación del consumo histórico por cliente (total de llamadas, minutos consumidos y mensajes enviados).
   - Creación de variables segmentadas para análisis comparativo entre tipos de plan.
3. **Análisis Exploratorio de Datos (EDA):**
   - Evaluación de distribuciones demográficas (edad, principales ciudades de Latinoamérica).
   - Comparación del comportamiento de uso entre usuarios de planes *Básico* vs. *Premium*.
4. **Conclusiones y Recomendaciones de Negocio:**
   - Identificación de segmentos clave con alto riesgo de abandono.
   - Propuestas estratégicas para el ajuste de paquetes comerciales y retención de usuarios.

---

## 🚀 Cómo ejecutar el notebook

Puedes explorar y ejecutar el análisis interactivo de dos formas:

### Opción 1: Abrir en Google Colab (Recomendado)
Haz clic en el siguiente botón para abrir el cuaderno directamente en Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1lYWRFeCuIvHuAuR-BcTQovgr92YSrIxm?usp=sharing)


### Opción 2: Desde el visor de GitHub
1. Haz clic en el archivo `S7 Version-Estudiante-Project-ConnectaTel.ipynb` en este repositorio para ver la versión pre-renderizada directamente en tu navegador.
2. Utiliza el botón **Open in Colab** que aparece en la parte superior del visor de GitHub.

---

## 📖 Guía de reproducción local

Sigue estos pasos para ejecutar el notebook en tu entorno local (Jupyter Notebook / VS Code):

1. **Clonar el repositorio:**
   ```bash
   https://github.com/Diego230703/S7-Project-ConnectaTel.git
