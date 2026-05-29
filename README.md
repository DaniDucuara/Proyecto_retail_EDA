# Análisis Exploratorio de Datos - Ecommerce Retail
Este proyecto desarolla un análisis exploratorio de datos sobre el comportamiento de usuarios en un e-commerce multicategoría. El objetivo principal es identificar patrones de navegación, carrito y compra, así mismo como horarios en donde hay mayor conversión para brindar oportunidades de mejora.
El análisis se realizó en Python utilizando un notebook en Visual Studio Code.


## Fuente de datos

El conjunto de datos utilizado corresponde al repositorio de Kaggle: eCommerce behavior data from multi category store.
El dataset usado corresponde al archivo de octubre del 2019.

## Objetivo del análisis

Analizar el comportamiento de los usuarios dentro del e-commerce para identificar:

Distribución general de eventos: view, cart y purchase.
Categorías con mayor tasa de conversión.
Horarios y días con mayor actividad de compra.
Distribución de precios y presencia de valores atípicos.

## Estructura del proyecto
```text
Proyecto_retail_EDA/
│
├── data/              # Carpeta local para almacenar los datos
├── images/            # Gráficos generados durante el análisis
├── notebooks/         # Notebook principal del EDA
├── requirements.txt   # Librerías necesarias para ejecutar el proyecto
├── README.md          # Documentación del proyecto
└── .gitignore         # Archivos y carpetas excluidos del repositorio
```
## Variables del dataset
Variable	Descripción

| Variable | Descripción |
|---|---|
| `event_time` | Fecha y hora del evento |
| `event_type` | Tipo de evento: visualización, carrito o compra |
| `product_id` | Identificador del producto |
| `category_id` | Identificador de la categoría |
| `category_code` | Taxonomía de la categoría del producto |
| `brand` | Marca del producto |
| `price` | Precio del producto en USD |
| `user_id` | Identificador del usuario |
| `user_session` | Identificador de la sesión del usuario |

## Principales análisis realizados

- Revisión de estructura, tipos de datos y valores nulos.
- Tratamiento de valores faltantes en `category_code`, `brand` y `user_session`.
- Eliminación de registros duplicados.
- Distribución general de eventos: `view`, `cart` y `purchase`.
- Tasa de conversión por categoría.
- Compras por hora del día.
- Distribución de precios y detección de outliers.
- Mapa de calor de compras por día y hora.

## Principales hallazgos
- La mayor parte de las interacciones corresponde a eventos de visualización, mientras que los eventos de carrito y compra representan una proporción menor.
- La tasa de conversión general es baja, lo que evidencia oportunidades de mejora en el embudo de ventas.
- Categorías como electronics.smartphone y kids.fmcg.diapers presentan una mayor tasa de conversión relativa.
- Las compras se concentran en determinadas horas y días, lo que permite identificar franjas estratégicas para campañas y promociones.
- La distribución de precios presenta asimetría positiva y valores atípicos asociados a productos de mayor valor.

## Oportunidades de mejora
- Optimizar el paso de visualización a carrito mediante mejores fichas de producto, imágenes, descripciones, reseñas y llamados a la acción.
- Reducir fricciones en el proceso de compra, especialmente en checkout, medios de pago, costos de envío y tiempos de carga.
- Priorizar categorías con alta conversión relativa para campañas, inventario y recomendaciones.
- Programar campañas comerciales en las franjas horarias de mayor actividad de compra.
- Segmentar productos por rangos de precio para evitar conclusiones distorsionadas por outliers.
- Mejorar la calidad del catálogo completando información de marca y categoría.

## Instalación y ejecución
Clonar el repositorio:

git clone <URL_DEL_REPOSITORIO>

Ingresar a la carpeta del proyecto:

cd Proyecto_retail_EDA

Crear un entorno virtual:

python -m venv .venv

Activar el entorno virtual en Windows:

.\.venv\Scripts\Activate.ps1

Instalar las dependencias:

pip install -r requirements.txt

Abrir el notebook ubicado en la carpeta notebooks/ y ejecutar las celdas en orden.

## Nota sobre los datos

La carpeta data/ no se incluye en el repositorio debido al tamaño del dataset original. Para reproducir el análisis, se debe descargar el archivo desde Kaggle y ubicarlo localmente en la carpeta data/.
