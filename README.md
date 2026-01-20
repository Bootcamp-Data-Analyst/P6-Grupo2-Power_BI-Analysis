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
| Ruben Camacho    | [![GitHub](https://img.shields.io/badge/GitHub-000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/RubenCG1997) | [![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ruben-camacho-gomez) |
| Pablo Rodríguez  | [![GitHub](https://img.shields.io/badge/GitHub-000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/PabloRodMu) | [![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/pablo-rodríguez-muñoz-357890185) |
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
 ┣ 📁 all-cities-csv/
 │   ┣ 📁 all-csv
 │   │   ┣ clean-Madrid.pbix
 │   │   ┣ clean-Tokyo.pbix
 │   │   ┣ clean-london.pbix
 │   │   ┣ clean-milan.pbix
 │   │   ┣ clean-ny.pbix
 │   │   ┗ clean-sydney.pbix
 │   ┗ all-cities.csv
 ┣ 📁 cities/
 │   ┣ New_York.pbix
 │   ┣ clean-Madrid.pbix.pbix
 │   ┣ london.pbix
 │   ┣ milan.pbix
 │   ┣ sydney.pbix
 │   ┗ tokyo.pbix
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


## 🔄 Transformaciones de Columnas (ETL)

Durante el proceso de limpieza y estandarización de los datos se aplicaron las siguientes transformaciones:

| Columna | Descripción | Transformación |
|--------|------------|----------------|
| `id` | Identificador de la propiedad (Número entero) | Eliminación de nulos y conversión a numérico |
| `name` | Nombre de la propiedad (Texto) | Sin transformación |
| `host_id` | Identificador del propietario (Número entero) | Eliminación de nulos y conversión a numérico |
| `host_name` | Nombre del propietario (Texto) | Sin transformación |
| `neighborhood_group` | Agrupación de barrios | Usada solo cuando existe |
| `neighborhood` | Barrio donde se encuentra la propiedad | Usada solo cuando existe |
| `latitude` | Latitud geográfica | Conversión a decimal y ajuste regional |
| `longitude` | Longitud geográfica | Conversión a decimal y ajuste regional |
| `room_type` | Tipo de alojamiento | Sin transformación |
| `price` | Precio en moneda local | Limpieza de símbolos y normalización regional |
| `usd` | Precio en dólares (USD) | Conversión de `price` a USD |
| `minimum_nights` | Mínimo de noches | Eliminada |
| `last_review` | Fecha de última reseña | Eliminada |
| `reviews_per_month` | Reseñas por mes | Eliminada |
| `number_of_reviews` | Cantidad de reseñas por propiedad | Conversión a numérico |
| `host_list_count` | Cantidad de propiedades por anfitrión | Conversión a entero |
| `availability_365` | Días disponibles por propiedad al año | Faltante en el caso de Tokio |
| `city` | Ciudad del alojamiento | Columna añadida manualmente |

---

## 🧮 Columnas Calculadas

### 👤 Tipo de Host

Clasificación según número de propiedades del anfitrión:

DAX
Tipo Host =
IF(
    [host_list_count] >= 2,
    "Profesional",
    "Particular"
)

📆 Tipo de Disponibilidad

Tipo Disponibilidad =
IF(
    [availability_365] <= 100, "Disponibilidad baja",
    IF(
        [availability_365] > 180, "Disponibilidad alta",
        "Disponibilidad media"
    )
)



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

#### 4️⃣ Demanda y Ocupación
- Disponibilidad media  
- Media de *reviews*  
- Precio medio por tipo de habitación  
- Gráfico circular de disponibilidad de alojamientos  

#### 5️⃣ Tipo de Host
- Distribución: Profesional vs Particular  
- Precio mediano por tipo de host  


Cada país utiliza una **paleta de colores propia**, manteniendo el mismo layout.

---

## 🗺️ Mapas y Visualización Geográfica

Permite:

- Mapas de calor por zonas  
- Comparación visual de precios y concentración  

Además, se ha utilizado un **mapa de forma (shape map)** en el que, para cada ciudad, se descargó su respectivo archivo **JSON/GeoJSON** y se aplicó un **color de relleno condicional** para distinguir tres rangos de precio:  
Para el resto de visualizaciones geográficas se utilizaron **mapas estándar basados en latitud y longitud**, representando la ubicación exacta de los alojamientos y su densidad.

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
- Sydney
- Milan
- New York

---

## 📈 Métricas y Medidas DAX

Medidas creadas:

- Total alojamientos  
- Precio medio  
- Precio mediano  
- Total barrios  
- Promedios por tipo de alojamiento y host  

Segmentación por:

- Barrio  
- Tipo de host  
- Tipo de habitación  

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


