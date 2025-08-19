# 📈 Transformación y Tratamiento de Datos – Predicción de Churn en Telecom X

Este proyecto tiene como finalidad **analizar, limpiar y transformar datos de clientes de Telecom X**, para posteriormente realizar un **análisis descriptivo** y construir un modelo predictivo de churn (cancelación de clientes).  
El enfoque está en **identificar factores clave que generan deserción** y proponer acciones de retención basadas en los hallazgos.

---

## 📌 Contenido

- [🎯 Objetivo del Proyecto](#-objetivo-del-proyecto)  
- [📑 Resumen del Dataset](#-resumen-del-dataset)  
- [📊 Hallazgos Principales](#-hallazgos-principales)  
- [🤖 Modelos y Resultados](#-modelos-y-resultados)  
- [🧪 Instalación y Ejecución](#-instalacion-y-ejecucion)  
- [▶️ Cómo ejecutar el proyecto](#%EF%B8%8F-cómo-ejecutar-el-proyecto)  

---

## 🎯 Objetivo del Proyecto

- Tratar y normalizar datos de clientes provenientes de un API.  
- Identificar **factores que incrementan el churn**.  
- Construir un **modelo predictivo** para anticipar la deserción.  
- Proponer **estrategias de negocio** para mejorar la retención de clientes.  

---

## 📑 Resumen del Dataset

- **Total de registros:** 7,267  
- **Total de variables:** 21  
- **Características incluidas:** datos demográficos, servicios contratados, historial de pagos, antigüedad y estado de churn.  
- **Desbalance de clases:**  
  - 71% clientes permanecen  
  - 25.7% clientes cancelan  
  - 3% registros con valores faltantes (eliminados en análisis).  

---

## 📊 Hallazgos Principales

- **Contrato Month-to-month:** 55% de los clientes, con la mayor tasa de churn.  
- **Antigüedad baja (<12 meses):** hasta 3 veces más riesgo de fuga.  
- **Servicios adicionales:** la ausencia de *OnlineSecurity, TechSupport* o *DeviceProtection* aumenta la probabilidad de cancelación.  
- **Método de pago:** *Electronic check* concentra el churn más alto (~34%).  
- **Tipo de internet:** los clientes con *Fiber optic* presentan mayor churn que con *DSL*.  
- **Patrón de facturación:** cargos mensuales altos y acumulados bajos son comunes en clientes nuevos en riesgo.  
- **Variables poco influyentes:** género y múltiples líneas telefónicas.  


---

## 💼 Recomendaciones de Negocio

1. **Migrar contratos "Month-to-month" a planes anuales** mediante descuentos e incentivos.  
2. **Promover servicios adicionales** con bundles de seguridad, soporte y protección de dispositivos.  
3. **Campañas específicas para clientes con "Electronic check"**, promoviendo pagos automáticos.  
4. **Programas de fidelización temprana**, con beneficios a los 6 y 12 meses.  
5. **Implementar alertas proactivas** cuando un cliente cumpla condiciones de riesgo (tenure bajo, contrato M2M, Electronic check).  

---

## 🧪 Instalación y Ejecución

Este proyecto fue desarrollado en **Google Colab**, por lo que no requiere instalación local.  

### 📌 **Opción 1: Abrir en Google Colab (recomendada)**

1. Abre el siguiente enlace:  
   👉 [Ejecutar en Google Colab](h[ttps://colab.research.google.com/](https://colab.research.google.com/drive/1oMtwWXSoFYPbZ7z0o9Btyx4pGHDuqoK3#scrollTo=3woWH3QDU2Lo))  
2. Inicia sesión con tu cuenta Google.  
3. Ejecuta las celdas de manera secuencial para reproducir el análisis completo.  

### 📌 **Opción 2: Reproducir localmente (opcional)**

1. Clona este repositorio:  
   ```bash
   git clone https://github.com/tu_usuario/tu_repositorio.git
