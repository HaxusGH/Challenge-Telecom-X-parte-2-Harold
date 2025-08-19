# 📑 Informe Final del Proyecto "Predicción de Churn – Telecom X parte 2"

## 1. Contexto y Objetivo

Telecom X se encuentra con un nivel considerable de cancelación de clientes (churn), lo que impacta de manera directa en sus ingresos y en la estabilidad de su crecimiento.  
El propósito de este trabajo es **reconocer los factores que generan el churn** y desarrollar **modelos predictivos sólidos** que permitan anticipar la probabilidad de abandono en los clientes. Con esta información, la compañía podrá diseñar **acciones de retención más eficaces y enfocadas**.

---

## 2. Resumen de Hallazgos Principales

- **Estructura del dataset:** 7,267 observaciones y 21 variables con datos de clientes: demografía, servicios contratados, facturación y estado de churn.  
- **Distribución de la variable objetivo:** 71% de clientes permanecen, 25.7% se dieron de baja y un 3% de registros con valores nulos fueron descartados para el análisis.  
- **Variables más determinantes para el churn:**
  - **Contrato:** 55% de los clientes tienen plan *Month-to-month*, el grupo con mayor tasa de cancelación.  
  - **Antigüedad (tenure):** Los clientes con menos de 12 meses de servicio tienen hasta 3 veces más probabilidad de abandono.  
  - **Servicios adicionales:** La falta de *OnlineSecurity, TechSupport* o *DeviceProtection* se asocia a mayor riesgo.  
  - **Método de pago:** *Electronic check* es el método con mayor tasa de churn (~34%).  
  - **Tipo de internet:** Los usuarios de *Fiber optic* presentan un churn superior frente a *DSL*.  
  - **Patrón de cargos:** Facturación mensual elevada junto con un acumulado bajo corresponde a clientes nuevos de alto riesgo.  
- **Variables con poca influencia:** Género y múltiples líneas telefónicas no muestran relación significativa con la deserción.

---

## 3. Modelos Desarrollados y Comparación

| Modelo                | AUC   | Recall | Precision | F1   | Observaciones |
|-----------------------|-------|--------|-----------|------|---------------|
| **Random Forest**     | 0.84  | 0.76   | 0.56      | 0.64 | Buen desempeño con balance entre precisión y facilidad de interpretación. |

- El modelo fue validado con *cross-validation* y se aplicaron ajustes de pesos para tratar el desbalance de clases.

---

## 4. Recomendaciones de Negocio

1. **Incentivar la migración de contratos "Month-to-month" a planes anuales** ofreciendo descuentos o beneficios adicionales.  
2. **Promocionar servicios adicionales** (seguridad, soporte técnico, protección de dispositivos) con paquetes atractivos dirigidos a clientes recientes.  
3. **Enfocar campañas en usuarios con "Electronic check"** para promover el uso de pagos automáticos mediante tarjeta o débito.  
4. **Implementar programas de fidelización temprana**, con beneficios especiales a los 6 y 12 meses de antigüedad.  
5. **Desarrollar un sistema de alertas preventivas** para identificar clientes en riesgo (tenure bajo, contrato M2M, Electronic check).  

---

## 5. Segmentos de Clientes en Riesgo

Del análisis emergen distintos perfiles con mayor propensión al churn, los cuales deberían ser el centro de las estrategias de retención:

### a) Contrato "Month-to-month", menos de 12 meses de servicio y pago con "Electronic check"
Clientes nuevos y con poca lealtad, además de un método de pago poco práctico.  
**Acción sugerida:** Incentivar contratos anuales y pagos automáticos.  

### b) Usuarios de internet "Fiber optic" sin servicios adicionales
Tienen una percepción limitada del valor del servicio o posibles problemas técnicos.  
**Acción sugerida:** Ofrecer paquetes con seguridad y soporte, junto con encuestas de satisfacción.  

### c) Clientes con cargos mensuales altos y acumulados bajos
Perfil típico de clientes recientes en planes premium con alto riesgo de desconexión temprana.  
**Acción sugerida:** Acompañamiento y seguimiento durante los primeros 3-6 meses.  

### d) Clientes sin dependientes ni pareja, especialmente adultos mayores
Tienden a un menor uso del servicio, lo que aumenta la posibilidad de abandono.  
**Acción sugerida:** Ofrecer beneficios exclusivos y comunicación personalizada.  

### e) Clientes sin servicio de internet
Aunque muestran baja tasa de churn, representan una oportunidad para aumentar ingresos mediante upselling.  

> **Conclusión de la sección:**  
> Identificar y segmentar estos grupos permite orientar los recursos hacia campañas de mayor impacto y efectividad.

---

## 6. Conclusión

El churn en Telecom X puede predecirse con una precisión considerable (AUC de 0.84 con *Random Forest*). Las variables relacionadas con **tipo de contrato, servicios extra y forma de pago** son las más influyentes y permiten accionar estrategias directas de retención.  
Si se aplican las recomendaciones, se estima que el churn anual podría reducirse entre **8 y 12 puntos porcentuales**, generando mejoras significativas en el ingreso y en la estabilidad de la empresa.  


---
