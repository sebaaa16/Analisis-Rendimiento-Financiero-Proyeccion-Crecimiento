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
Implementé una arquitectura de **Modelo en Estrella (Star Schema)** para garantizar escalabilidad y rendimiento:
* **Tablas de Dimensiones:** `Dim_Industria` y `Dim_Tipo_Negocio`.
* **Tabla de Hechos:** `Tabla_Principal` con métricas de ingresos, gastos y beneficios.
* **Relaciones:** Conexiones de uno a muchos (1:*) para un filtrado preciso entre dimensiones y hechos.

### 3️⃣ Análisis con DAX y Visualización
* **Cálculo de Eficiencia:** Creé la medida DAX `% de Margen de Beneficio` para identificar qué sectores son más rentables operativamente.
* **KPIs Dinámicos:** Tarjetas con **Formato Condicional** (Verde/Rojo) basadas en el cumplimiento de márgenes de beneficio.
* **Análisis de Tendencia:** Comparativa visual entre el beneficio neto actual y la proyección futura.

---

## 📂 Estructura del Repositorio
* **`/Data/Raw`**: Dataset original con los datos brutos del planner.
* **`/Data/Processed`**: Dataset auditado y normalizado en Excel (fuente de datos final).
* **`/Reports`**: Archivo `.pbix` con el dashboard interactivo de Power BI.

---

## 💡 Hallazgos Clave (Insights)
* **Liderazgo Sectorial:** La industria de **Construction** domina el volumen de ingresos totales y presenta la proyección de crecimiento más prometedora.
* **Rentabilidad vs. Volumen:** Se identificaron sectores que, aunque facturan menos, poseen un margen de beneficio superior, lo que representa una mayor eficiencia en el uso de recursos.

---

## ⚙️ Nota Técnica
Para visualizar correctamente el reporte, es necesario actualizar la ruta del origen de datos en Power BI (`Transformar Datos > Configuración de origen de datos`) apuntando al archivo Excel ubicado en la carpeta `/Data/Processed`.

---
**Autor:** Sebastian  
**Rol:** Junior Data Analyst
