# Prácticas de NLP

## Descripción del proyecto
Este repositorio contiene dos prácticas de **Procesamiento de Lenguaje Natural (NLP)** realizadas en Python:

1. **Análisis de texto literario:** Procesamiento del corpus *The Adventures of Sherlock Holmes* utilizando **spaCy** para dividir el texto en oraciones, detectar patrones y extraer contexto completo.  
2. **Análisis de sentimientos:** Clasificación de reseñas de películas utilizando **VADER**, con preprocesamiento de texto, generación de predicciones y evaluación del desempeño del modelo.

---

## Contenido

- **Corpus:**  
  - `sherlock_holmes.txt` – Texto de *The Adventures of Sherlock Holmes* (dominio público, Project Gutenberg).  
  - `filmreviews_sentiment.tsv` – Reseñas de películas con etiquetas de sentimiento (`pos`/`neg`).

- **Librerías utilizadas:**  
  ```python
  import warnings                     # Para manejar y suprimir mensajes de advertencia
  import spacy                        # Librería de Procesamiento de Lenguaje Natural (NLP)
  import re                           # Librería para trabajar con expresiones regulares, permite buscar, extraer y manipular patrones de texto de manera eficiente.
  from spacy.matcher import Matcher   # Herramienta de SpaCy para definir y buscar patrones en el texto
  import pkg_resources                # Permite acceder a recursos dentro de paquetes Python, verificar versiones de librerías y manejar dependencias de manera programática
  import pandas as pd                 # Manipulación y análisis de datos en estructuras tipo DataFrame
  import numpy as np                  # Operaciones numéricas y manejo de arreglos
  import nltk                         # Librería para procesamiento de lenguaje natural
  from nltk.sentiment.vader import SentimentIntensityAnalyzer  # Analizador de sentimiento VADER
  from sklearn.metrics import accuracy_score, confusion_matrix, classification_report     # Métricas de evaluación para modelos de clasificación
