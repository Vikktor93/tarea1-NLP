## Procesamiento de Lenguaje Natural – Tarea 1 (Cabildos Provinciales 2016)

**Asignatura:** Procesamiento de Lenguaje Natural
**Fecha de entrega:** 20 de julio de 2025

### Descripción del Proyecto
Este repositorio contiene el análisis de texto de los cabildos provinciales realizados el año 2016. Esta tarea se enfoca en la extracción y visualización de patrones léxicos para un concepto específico. El objetivo es:

1. Seleccionar un concepto con suficiente masa textual.  
2. Limpiar y normalizar el texto.  
3. Procesar con Stanza (tokenización, POS, lematización) y NLTK.  
4. Extraer sustantivos, adjetivos y bigramas sustantivo–adjetivo.  
5. Generar WordClouds y gráficas de frecuencias.  
6. Construir y visualizar la red léxica de bigramas.  
7. Interpretar resultados con ejemplos ilustrativos.

### Estructura del Repositorio
```
tarea1-NLP/
│
├── data/
│ ├── raw/
│ │ └── resultadocabildoprovincial.xlsx # Data original
│ └── processed/ # CSVs de subset limpio
│
├── notebooks/
│ └── tarea1_victor_saldivia.ipynb # Notebook principal paso a paso
│
├── output/
│ ├── figures/ # WordClouds, gráficas, red de bigramas
│ └── tables/ # CSV/TXT de conteos y stopwords
│
└── README.md # Documentación del proyecto
```

### Instalación y Configuración

1. **Clonar el repositorio**  
   ```bash
   git clone https://github.com/Vikktor93/tarea1-NLP
   cd tarea1-NLP
   ```

2. Crear entorno virtual en Anaconda (recomendado)
    ```bash
    conda create -n nlp python=3.12.11 -y
    conda activate nlp
    ```

3. Instalar dependencias
    ```bash
    pip install --upgrade pip
    pip install pandas numpy matplotlib networkx tqdm nltk stanza wordcloud
    ```

4. Descargar recursos de NLTK y Stanza
    ```
    import nltk
    nltk.download('stopwords')

    import stanza
    stanza.download('es')
    ```

### Uso

1. Clonar el repositorio en VS Code

2. Siguir las secciones en orden:
    1. Instrucciones y enunciado
    2. Carga y exploración inicial de datos
    3. Configuración de librerías y workaround OpenMP
    4. Carga y Exploración Inicial
    5. Selección del concepto a analizar
    6. Pre-Procesamiento de Texto
        6.1. Tokenización, POS-tagging y lematización (Stanza)
        6.2 Análisis de frecuencias crudas
        6.3. Stopwords
    7. Extracción de sustantivos, adjetivos y bigramas
    8. Conteo Globales
    9. Visualizaciones
        9.1. WordCloud de sustantivos
        9.2. WordCloud de palabras de bigramas
        9.3. Histograma de adjetivos
        9.4. Red de bigramas
    10. Interpretación y ejemplos

3. Los gráficos y tablas generados se guardan en output/figures y output/tables.

### Resultados

- **WordClouds:** Nube de sustantivos y nube de bigramas.
- **Gráfica de adjetivos:** Histograma de los 20 adjetivos más frecuentes.
- **Red de Bigramas:** Grafo de bigramas sustantivo–adjetivo con métricas de grado.
- **Ejemplos:** Frases representativas que contienen los términos más frecuentes.

### Interpretación y Conclusiones

Revisar la sección 10: Interpretación y Ejemplos del notebook para observar insights semánticos y fragmentos ilustrativos.