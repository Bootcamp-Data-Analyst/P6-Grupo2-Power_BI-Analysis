# 📊 Análisis del Negocio de Airbnb por Ciudades con Power BI

## 🧭 Descripción del Proyecto

Este proyecto tiene como objetivo analizar el negocio de Airbnb en diferentes ciudades utilizando **Power BI**, con el fin de identificar patrones de:

- 💰 Precios  
- 📍 Popularidad de barrios  
- 🏠 Tipos de alojamiento  
- 👤 Perfil de los anfitriones  
- 📆 Disponibilidad de los alojamientos  

El resultado final es un conjunto de **dashboards individuales por ciudad** y un **dashboard comparativo global entre ciudades**.

---

## 👩‍💻 Contribuyentes

  | Nombre           | GitHub | LinkedIn |
|------------------|--------|----------|
| Jaime Amuedo     | [![GitHub](https://img.shields.io/badge/GitHub-000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/JaimeAmuedoJAH) | [![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jaime-amuedo-hidalgo-a432bb354/) |
| Ruben Camacho    | [![GitHub](https://img.shields.io/badge/GitHub-000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/RubenCG1997) | [![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](www.linkedin.com/in/ruben-camacho-gomez) |
| Pablo Rodríguez  | [![GitHub](https://img.shields.io/badge/GitHub-000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/PabloRodMu) | [![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](www.linkedin.com/in/pablo-rodríguez-muñoz-357890185) |
| Andrés Pérez     | [![GitHub](https://img.shields.io/badge/GitHub-000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/andresdatalyst) | [![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/andresproviraprogramador/) |

## 👥 Equipo de Trabajo

- **Rubén** — Data Analyst  
- **Pablo** — Data Analyst  
- **Jaime** — Scrum Master  
- **Andrés** — Product Owner  

---

## 🧩 Metodología de Trabajo

Se trabajó siguiendo una metodología ágil simulando un entorno real:

- Organización de tareas mediante **GitHub Projects**
- Uso de **ramas por funcionalidad y por ciudad**
- Reuniones tipo **daily stand-up**
- Revisión continua del progreso y ajustes del plan

---

## 🎯 Objetivos del Análisis

Responder a las siguientes preguntas de negocio:

- ¿Qué ciudades tienen mayor oferta de alojamientos?
- ¿Qué barrios concentran más propiedades en cada ciudad?
- ¿Qué tipo de alojamiento es más común?
- ¿Predominan los anfitriones particulares o profesionales?
- ¿Cómo se relacionan el precio, la disponibilidad y la demanda?
- ¿Qué diferencias existen entre ciudades?

---

## 🗂️ Fuentes de Datos

Datos en formato **CSV**, uno por cada ciudad, con información pública de Airbnb:

- Propiedades  
- Anfitriones  
- Ubicación  
- Precio  
- Reseñas  
- Disponibilidad  

Cada archivo presentaba **ligeras diferencias en estructura y formato**.

---

## 🤖 Tecnologías y Librerías

![Power Bi](https://img.shields.io/badge/power_bi-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Microsoft Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)

## 📁 Estructura del Repositorio

```
📦 P6-GRUPO2-POWER_BI-ANALYSIS/
 ┣ 📁 cities/
 │   ┣ New_York.pbix
 │   ┣ clean-Madrid.pbix.pbix
 │   ┣ london.pbix
 │   ┣ milan.pbix
 │   ┣ sydney.pbix
 │   ┣ tokyo.pbix
 │   ┗ all-states-history.csv
 ┣ 📁 clean_csv/
 │   ┣ clean-Madrid.csv
 │   ┣ clean-Tokyo.csv
 │   ┣ clean-london.csv
 │   ┣ clean-sydney.csv
 │   ┣ clean-Milan.csv
 │   ┗ clean_NY.csv
 ┣ 📁 plantilla_dashboard/
 │   ┗ platilla_dashboard.pbix 
 ┣ 📄 .gitignore
 ┗ 📄 README.md
```

## 🔄 Proceso ETL (Extract, Transform, Load)

### 🔹 Extract
- Importación directa de archivos CSV en Power BI.

### 🔹 Transform
Limpieza y estandarización de columnas:

| Columna                | Transformación                                   |
|------------------------|--------------------------------------------------|
| `id`                   | Eliminación de nulos y conversión a numérico     |
| `host_id`              | Eliminación de nulos y conversión a numérico     |
| `latitude / longitude` | Conversión a decimal y ajuste regional           |
| `price`                | Conversión de moneda a USD                       |
| `minimum_nights`       | Eliminada                                        |
| `last_review`          | Eliminada                                        |
| `reviews_per_month`    | Eliminada                                        |
| `neighborhood_group`   | Usada solo cuando existe                         |
| `city`                 | Columna añadida manualmente                      |

Configuración regional ajustada para correcta lectura de decimales y mapas.

---

## 🧹 Estrategia de Limpieza

Dado que los datasets estaban separados por ciudad:

- Cada analista realizó el ETL de su ciudad
- Se siguieron reglas comunes acordadas por el equipo
- CSV limpios almacenados en: `csv_clean/`
- Archivos Power BI por ciudad en: `cities/`

---

## 📤 Exportación de CSV Limpio

Desde Power BI:

1. Crear visual de tabla con todas las columnas  
2. Menú de opciones → **Exportar datos**  
3. Seleccionar **datos subyacentes**  
4. Descargar CSV  

Esto permitió consolidar los datasets posteriormente.

---

## 🧱 Modelado y Columnas Calculadas

Se añadieron columnas calculadas para análisis de negocio:

- **Tipo de Host** (Profesional vs Particular)

---

## 📊 Diseño de Dashboards por Ciudad

Plantilla común ubicada en la rama:

`feature/plantilla`

### Páginas por ciudad

#### 1️⃣ Overview
- Total de alojamientos  
- Total de barrios  
- Precio medio  
- Distribución por tipo de habitación  
- Top 10 barrios con más alojamientos  

#### 2️⃣ Barrios y Precios
- Total de alojamientos por barrio  
- Precio medio por barrio  
- Precio por tipo de alojamiento  
- Mapa de localización  

#### 3️⃣ Tipo de Alojamiento
- Distribución por *room type*  
- Relación con precios y disponibilidad  

#### 4️⃣ Tipo de Host
- Distribución: Profesional vs Particular  
- Precio mediano por tipo de host  

Cada país utiliza una **paleta de colores propia**, manteniendo el mismo layout.

---

## 🗺️ Mapas y Visualización Geográfica

Columna adicional para mapas de calor:

- `ubicacion_mapa`

Permite:

- Mapas de calor por zonas  
- Comparación visual de precios y concentración  

Herramientas utilizadas:

- **Azure Maps**
- **Visual Maps**

Con especial atención a la configuración regional de coordenadas.

---

## 🌍 Dashboard Comparativo de Ciudades

Para la comparación entre ciudades:

- Unión de todos los CSV limpios
- Conversión de todas las monedas a USD
- Columna creada: `price_usd`

### Indicadores comparados

- Precio medio por ciudad  
- Distribución de tipos de alojamiento  
- Popularidad de barrios  
- Perfil de host  

Ciudades incluidas:

- Londres  
- Madrid  
- Tokio  

---

## 📈 Métricas y Medidas DAX

Medidas creadas:

- Total alojamientos  
- Precio medio  
- Precio mediano  
- Total barrios  
- Promedios por tipo de alojamiento y host  

Segmentación por:

- Ciudad  
- Barrio  
- Tipo de host  
- Tipo de habitación  

---

## 🧠 Análisis Adicional

Caso Tokio:

- Estudio de correlación entre:
  - Precio  
  - Número de reseñas  

Objetivo: evaluar relación entre **demanda y precio**.

---

## 🚀 Entregables

- Dashboards individuales por ciudad  
- Dashboard comparativo global  
- CSV limpios estandarizados  
- Documentación del proyecto  

---

## 📌 Conclusiones

El proyecto demuestra que:

- La estandarización es clave en análisis multifuente  
- El diseño común facilita comparativas  
- El storytelling es esencial para comunicar insights  

Resultado: herramienta útil para la toma de decisiones en el sector turístico y de alquiler vacacional.

---

# 🎤 Storytelling / Data Driven para Presentación

## ❓ Contexto y Objetivo — Problema

Entender cómo funciona el mercado de Airbnb en distintas ciudades y qué diferencias existen en:

- Precios  
- Barrios  
- Tipos de alojamiento  
- Perfil de anfitriones  

---

## 🎯 Importancia

- Ayuda a inversores  
- Ayuda a anfitriones  
- Ayuda a plataformas  

---

## 🧠 Decisiones Iniciales

### 🔹 Análisis por ciudades
**Decisión:** analizar cada ciudad por separado  
**Motivo:** limpieza individual antes de comparar  

### 🔹 Conversión de moneda
**Decisión:** convertir precios a USD  
**Motivo:** comparaciones válidas entre ciudades  

### 🔹 Plantilla común
**Decisión:** mismo diseño para todas las ciudades  
**Motivo:**
- Comparación visual  
- Menos sesgos  
- Escalabilidad  

---

## 🧹 Limpieza y Modelado

### Problemas
- Valores nulos  
- Formatos decimales distintos  
- Columnas irrelevantes  

### Soluciones
- Reglas de limpieza comunes  
- Validación de tipos  
- Columnas calculadas  

---

## 📊 Preguntas de Negocio por Página

| Página   | Pregunta                         |
|--------|----------------------------------|
| Overview | ¿Cómo es el mercado general?     |
| Barrios  | ¿Dónde se concentra la oferta?   |
| Vivienda | ¿Qué tipo domina?                |
| Host     | ¿Quién controla el mercado?      |

---

## 💡 Insights Clave (Ejemplos)

- Barrios con más alojamientos  
- Ciudades con mayor precio medio  
- Mayor peso de hosts profesionales  
- Relación entre reseñas y precio  

---

## 🌍 Comparativa Global

### Aportaciones

- Ranking de ciudades  
- Mercados más competitivos  
- Diferencias estructurales  

---

## 🧩 Conclusiones de Negocio

### Aprendizajes

- Cada ciudad tiene dinámicas distintas  
- La profesionalización varía  
- El tipo de alojamiento impacta en el precio  

### Decisiones Posibles

- Ajuste dinámico de precios  
- Inversión por zonas  
- Detección de saturación  

---

## 🔮 Futuras Mejoras

- Series temporales  
- Datos de ocupación real  
- Análisis de rentabilidad  
- Datos turísticos externos  
