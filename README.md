# Mobility_economy_project
Markdown
# 🌍 Análisis Global de Movilidad Urbana y Desempeño Económico (TomTom & OECD)

## 📌 Descripción del Proyecto
Este proyecto realiza un análisis integral interconectando datos globales de tráfico vehicular en tiempo real con indicadores macroeconómicos y ambientales a nivel de ciudad. El objetivo principal es identificar cómo la congestión vial impacta o se correlaciona con la calidad de vida, el desempleo, el PIB per cápita y la contaminación por material particulado ($PM_{2.5}$) en las principales urbes del mundo.

A través de este desarrollo, se demuestran capacidades sólidas en la construcción de **pipelines de limpieza de datos (ETL)**, manipulación de grandes volúmenes de información y **Análisis Exploratorio de Datos (EDA)** utilizando el ecosistema científico de Python.

---

## 🛠️ Habilidades Técnicas Demostradas

### 1. Ingeniería de Datos y Limpieza (ETL)
* **Procesamiento de DataFrames Masivos:** Manipulación eficiente de conjuntos de datos con más de 1 millón de registros (`tomtom_traffic.csv`).
* **Normalización y Estandarización:** Unificación de nomenclaturas (*snake_case*) en variables de múltiples fuentes para garantizar consistencia en el código.
* **Parsing y Conversión de Tipos Complejos:** Limpieza de strings con formatos regionales (reemplazo de separadores de miles/decimales, eliminación de símbolos de porcentaje `%`) y conversión explícita a tipos numéricos (`float64`).
* **Manejo de Series de Tiempo:** Extracción y enriquecimiento de datos temporales nativos utilizando `pd.to_datetime()` con especificación de zonas horarias (`utc=True`) y filtrado cronológico avanzado.

### 2. Análisis Exploratorio de Datos (EDA) y Enriquecimiento
* **Feature Engineering (Ingeniería de Características):** Creación de nuevas métricas clave a partir de variables base (ej. cálculo de la población absoluta de las ciudades combinando factores de escala).
* **Integración de Fuentes Heterogéneas (Data Merging):** Fusión lógica de datos de tráfico basados en códigos de país e identificadores de ciudades con estadísticas socioeconómicas de la OCDE.

---

## 📊 Estructura del Pipeline en el Notebook

El análisis está estructurado siguiendo las mejores prácticas del flujo de trabajo de un Data Analyst:

1.  **Carga de Datos y Vista Rápida:** Inspección inicial de las estructuras (`.info()`, `.head()`) para mapear tipos de datos y valores ausentes.
2.  **Estandarización de Esquemas:** Renombramiento técnico de columnas para eliminar espacios y caracteres especiales de los dataframes de tráfico y economía.
3.  **Sanitización de Datos:** Limpieza profunda de formatos de texto a numéricos e inicialización de tipos `datetime64[ns, UTC]`.
4.  **Filtrado y Segmentación:** Extracción de componentes temporales (años) para realizar análisis comparativos homogéneos (fijando cohortes como el año 2024).

---

## 💻 Tecnologías Utilizadas

* **Lenguaje:** Python 3.x
* **Manipulación de Datos:** Pandas, NumPy
* **Visualización de Datos:** Seaborn, Matplotlib
