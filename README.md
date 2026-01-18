# 📊 Proyecto BI en Excel – Análisis de Ventas 2024

## Descripción general
Este proyecto presenta un **análisis de Business Intelligence (BI)** aplicado utilizando Microsoft Excel como herramienta analítica, implementando modelado de datos, medidas DAX y visualización dinámica.  
El objetivo es transformar datos transaccionales de ventas en **información estructurada, analizable y accionable**, siguiendo principios reales de BI (no solo tablas dinámicas aisladas).

El dataset utilizado proviene de Kaggle:  
**“Datasets para Proyecto BI – Análisis de Ventas”**

--- 

## Objetivos del proyecto
- Construir un modelo de datos óptimo en Excel
- Aplicar análisis descriptivo con fundamentos de análisis diagnóstico
- Implementar medidas DAX reales, no cálculos manuales
- Diseñar un dashboard interactivo y completamente dinámico
- Simular un flujo de trabajo similar a herramientas como Power BI

---


## 📁 Estructura del repositorio

**Informe ejecutivo:** Presenta las conclusiones del análisis, estas fueron elaboradas a partir de un modelo BI optimizado y están orientadas a la toma de decisiones.

🔗 [Ver informe ejecutivo completo](docs/Informe_Ejecutivo_BI.pdf)

**Dashboard ventas:** Muestra el comportamiento de las ventas a través del tiempo y las KPIs principales

**Dashboard categorías:** Muestra el comportamiento de las ventas según las categorías y los productos

**Modelado:** Muestra el modelo de datos, este sigue un esquema estrella

---

## Estructura del dataset
El proyecto trabaja con 6 tablas, organizadas bajo un enfoque **modelo estrella**:

- **Hecho_venta** (tabla de hechos)
- **dim_producto**
- **dim_categoría**
- **dim_cliente**
- **dim_metodo_pago**
- **Calendario** (creada manualmente)

---

## Paso 1 – Modelado de datos (BI real en Excel)
Se utilizó el Modelo de Datos de Excel **(Power Pivot)** para:

- Crear el modelo estrella
- Definir relaciones 1 a muchos entre tablas
- Evitar duplicación de datos
- Garantizar integridad referencial
- Permitir análisis multi-dimensional

**Relaciones clave**:
- Hecho_venta[ID_Producto] → dim_Producto[ID_Producto]
- Dim_Producto[ID_Categoría] → dim_Categoría[ID_Categoría]
- Hecho_venta[Fecha] → Calendario[Fecha]

Este enfoque elimina cálculos redundantes y replica un entorno BI profesional.

---

## Paso 2 – Creación de la Tabla Calendario (DAX)
Se creó una tabla calendario dinámica basada en el rango real de fechas del dataset, permitiendo:

- Análisis temporal correcto
- Segmentadores por mes y año
- Escalabilidad futura

Ejemplo de campos creados:
- Año
- Mes
- Nombre del mes
- Número de mes (para ordenación correcta)

---

## Paso 3 – Medidas DAX
Todas las métricas se construyeron como medidas, no como columnas calculadas.

Medidas principales:
- `Ventas_totales`
- `Unidades_vendidas`
- `Ventas_acumuladas (YTD)`
- `KPIs contra objetivo de ventas`

Esto garantiza:
- Correcta evaluación de contexto
- Compatibilidad con tablas dinámicas del modelo
- Escalabilidad analítica

---

## Paso 4 – Tablas dinámicas desde el Modelo de Datos
Las visualizaciones se construyeron usando:
> **Insertar → Tabla dinámica → Usar el Modelo de Datos**

Esto permitió:
- Usar medidas DAX en valores
- Filtrar por dimensiones relacionadas
- Crear análisis cruzados reales

Análisis desarrollados:
- Ventas por mes
- Top 5 productos más vendidos
- Ventas por categoría
- Estado de las ventas (completa, pendiente, cancelada)
- Métodos de pago

---

## Paso 5 – Segmentadores y control de contexto
Se implementaron segmentadores conectados al modelo:
- Mes
- Categoría
- Estado de venta

Además:
- Corrección del orden cronológico de meses
- Sincronización entre visuales
- Eliminación de filtros visuales innecesarios

---

## Paso 6 – KPIs
Se construyeron KPIs personalizados para:
- Ventas totales vs objetivo
- Variación porcentual
- Estado visual (superación o no del objetivo)

Los KPIs se diseñaron usando:
- Medidas DAX
- Formato condicional
- Indicadores visuales claros

---

## Paso 7 – Dashboard
El dashboard final:
- Es 100% dinámico
- Responde a segmentadores
- No contiene cálculos manuales
- Presenta información clara para toma de decisiones

Se ocultaron hojas técnicas (tablas dinámicas, modelo) para entregar una vista ejecutiva limpia.

---

## 🧠 Tipo de análisis realizado
- ✅ **Análisis descriptivo**
- ⚠️ **Elementos de análisis diagnóstico**
  - Concentración de ventas
  - Identificación de productos y categorías dominantes
  - Evaluación de estados de venta y métodos de pago

Este proyecto sienta las bases para análisis predictivos y prescriptivos.

---

## 🛠️ Herramientas utilizadas
- Microsoft Excel
  - Power Pivot
  - Modelo de Datos
  - DAX
  - Tablas dinámicas
  - Segmentadores
- Dataset de Kaggle

---

## Conclusión
Este proyecto demuestra que Excel puede ser utilizado como una herramienta de BI real, siempre que se aplique:

- Modelado correcto
- Separación hechos / dimensiones
- Uso de medidas DAX
- Análisis basado en contexto

No es un reporte estático, sino un **modelo analítico reutilizable y escalable**, alineado con buenas prácticas de Business Intelligence.

---


## 👤 Créditos
Proyecto desarrollado por **Fernando David Carela Pichardo**


