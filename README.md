# 🧑🏻‍💻 Habilidades y Herramientas Demandadas para un Analista de Datos

Este proyecto tiene como objetivo medir las demandas laborales de análisis de datos en Colombia. [LinkedIn](https://linkedin.com/) fue la fuente de datos preferida debido a su amplia gama de información disponible:

* Título del empleo
* Empresa
* Modalidad de trabajo
* Tipo de empleo
* Ubicación
* Descripción del empleo

## Pregunta a Responder

Este proyecto responde a la pregunta: 
**¿Qué habilidades y herramientas son las más demandadas para el puesto de Analista de Datos en Colombia?**

## Descripción

Utilizando técnicas de Web Scraping, Traducción, Embedding y Clustering sobre lenguaje natural se identificaron grupos diferenciados con base a descripciones de ofertas de empleo que permitieron conocer qué habilidades técnicas y no técnicas se solicitan más para los puestos de analistas de datos, dando lugar a un análisis crítico sobre las oportunidades laborales y las posibilidades que existen para formarse en el contexto colombiano.

Para una explicación detallada del funcionamiento de este proyecto, entre [aquí](https://nbviewer.org/github/vcardonas/linkedin-project/blob/main/Cuadernos/1%20Propuesta_Proyecto.ipynb)

### Requerimientos de Software

El proyecto se desarrolló con las siguientes versiones:

- Python Versión 3.10.8
- Selenium Versión 4.1.2 ó reciente
- Transformers Versión 4.25.1 ó reciente
- Scikit Learn Versión 1.2.0 ó reciente

## Metodología

Este proyecto utilizó una combinación de Web Scraping, Análisis Exploratorio de Datos (Exploratory Data Analysis - EDA) y Machine Learning (ML) para responder a las preguntas anteriores.

### Web Scraping

Se proporciona un script llamado [WebScraping_LinkedIn.ipynb](./Cuadernos/2%20WebScraping_LinkedIn.ipynb) usando `selenium` para manejar el web scraping de LinkedIn. Para ejecutar este Script, caben hacer las siguientes recomendaciones:

* Cree un sólo ambiente para trabajar el web scraping. Debido a que todos los paquetes que se instalaran en los demás pasos podrían hacer colapsar su ambiente de trabajo.
* Es necesaria la creación de perfil falso ya que, pese a que es [legal](https://www.forbes.com/sites/zacharysmith/2022/04/18/scraping-data-from-linkedin-profiles-is-legal-appeals-court-rules/?sh=45913a722a9c), este sitio web suele banear a bots de web scraping.
* Se utiliza el navegador Brave en Mac. Por lo tanto, en `binaryPath` se debe designar la ruta de acceso a su navegador.

Este script se romperá si cambia la estructura del sitio web.

### Traducción

La traducción de los datos se realizó y publicó por separado en un cuaderno Jupyter en este repositorio, llamado [Traducción_Datos.ipynb](./Cuadernos/3%20Traducci%C3%B3n_Datos.ipynb).

Debido a que los descripciones correspondían a diferentes idiomas, se utilizó el modelo de [Helsinki-NLP](https://huggingface.co/sentence-transformers/all-mpnet-base-v2) para traducir los datos.

### Exploratory Data Analysis (EDA)

En la EDA, se explorarón los elementos visuales de los datos.

### Machine Learning

Hay dos formas de Aprendizaje Automático que se aplicaron para este proyecto:

* Embedding para procesamiento del lenguaje natural.
* Reducción de dimensiones (UMAP).
* Clustering de trabajos (K-Means).

## Propietaria

El proyecto es realizado por Valentina Cardona (vcardonas@unal.edu.co)
