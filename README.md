# 📊 Análisis de Rendimiento Financiero y Proyección de Crecimiento

## 📝 Descripción del Proyecto
Este proyecto presenta un dashboard interactivo desarrollado en **Power BI**, basado en el dataset *Business Growth Planner*. El objetivo principal fue transformar datos financieros brutos en un tablero de control estratégico que permite visualizar la rentabilidad actual y las proyecciones de crecimiento a 6 meses de diversos sectores industriales.

---

## 🛠️ Metodología y Herramientas

### 1️⃣ Limpieza y Auditoría de Datos (Excel)
Antes del modelado, realicé un proceso de **ETL** para asegurar la calidad de la información:
* **Validación Lógica:** Comprobé mediante fórmulas que la relación `Ingresos - Gastos = Beneficio` fuera consistente en los más de 5,000 registros.
* **Normalización:** Limpié y estandaricé las categorías de `Industry` y `Business Type`, eliminando duplicados y valores nulos para evitar errores en el filtrado.

### 2️⃣ Modelado de Datos (Power BI)
Implementé una arquitectura de **Modelo en Estrella** para garantizar escalabilidad y rendimiento:
* **Tablas de Dimensiones:** `Dim_Industria1` y `Dim_Tipo_Negocio2`.
* **Tabla de Hechos:** `Tabla_Principal` con métricas de ingresos, gastos y beneficios.
* **Relaciones:** Conexiones de uno a muchos (1:*) para un filtrado preciso entre dimensiones y hechos.

### 3️⃣ Análisis con DAX y Visualización
* **Cálculo de Eficiencia:** Creé la medida DAX `% de Margen de Beneficio` para identificar qué sectores son más rentables operativamente.
* **Consistencia Visual:** Apliqué formatos de moneda unificados ($) y etiquetas de unidades en millones para facilitar la lectura rápida de grandes volúmenes de capital.
* **Análisis de Tendencia:** Diseñé un gráfico comparativo de barras para contrastar el **Beneficio Actual** frente a la **Proyección de Crecimiento (6 meses)**, permitiendo identificar sectores con mayor potencial de escalabilidad

---


## 💡 Hallazgos Clave (Insights)
* **Liderazgo Sectorial:** La industria de **Construction** domina el volumen de ingresos totales y presenta la proyección de crecimiento más prometedora.
* **Rentabilidad vs. Volumen:** Se identificaron sectores que, aunque facturan menos, poseen un margen de beneficio superior, lo que representa una mayor eficiencia en el uso de recursos.

---
**Desarrollado por Sebastian Mayorga - Junior Data Analyst**
