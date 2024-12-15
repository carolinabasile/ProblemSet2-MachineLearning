# ProblemSet2-MachineLearning

Este repositorio contiene los materiales, scripts y resultados del Problem Set 2 de Machine Learning en la Maestría en Economía de la UNLP. El proyecto abarca limpieza de datos, análisis exploratorio, modelado predictivo y presentación de resultados. A continuación, se detalla la estructura del repositorio y el flujo de trabajo.

## Estructura del repositorio

```plaintext
Problem_Set_1/
├── document/
│   └── report.pdf         # PDF con la metodología, análisis y resultados
├── scripts/
│   └── Union.ipynb          # Script con el código para unir bases de datos
│   └── PS2.ipynb                    # Script con el código para análisis y modelado
├── stores/
│   └── Input                        # Bases de datos sin procesar
│       └── test_hogares.rar                # Conjunto de datos crudos correspondiente al test set de hogares
│       └── train_hogares.rar               # Conjunto de datos crudos correspondientes al training set de hogares
│       └── test_personas.rar               # Conjunto de datos crudos correspondientes al test set de personas
│       └── train_personas.rar              # Conjunto de datos crudos correspondientes al training ser de personas
│   └── test_df.csv                # Conjunto de datos crudos del test set de hogares y personas
│   └── train_df.csv               # Conjunto de datos crudos del training set de hogares y personas
├── views/
│   └── *.png              # Gráficos con estadísticas descriptivas, resultados de modelos y errores de predicción
├── README.md
└── requirements.txt
```

## 1. document
Contiene un archivo PDF (report.pdf) que documenta todo el proceso, incluyendo los objetivos, la metodología y los resultados clave.
Consulta este archivo para obtener un resumen completo del proyecto sin necesidad de ejecutar el código.

## 2. scripts
Union.ipynb: Un notebook de Jupyter que incluye:
- Importación de bases de datos.
- Unión de las bases de personas con las de hogares según id.

PS2.ipynb: Un notebook de Jupyter que incluye:
- Importación de bases de datos.
- Limpieza y creación de variables: Creación de variables de interés y tratado de missing values para evitar conflictos en el modelado.
- Análisis exploratorio de datos con estadísticas descriptivas y distribuciones de variables.
- Construcción y evaluación de modelos predictivos para predecir el la situación de pobreza de los hogares en Colombia. 
- Comparación de los accuracy, ROC-AUC y F1 scores asociados a cada modelo.
- Predicción del test set.

## 3. stores
Contiene los conjuntos de datos (train_df.rar y test_df.rar), generados tras las uniones de las bases.
## 3a. views
Contiene las bases en bases por personas y hogares que luego se unen.

## 4. views
Almacena visualizaciones generadas durante el análisis, que incluyen:
- Histogramas de las variables clave.
- Matriz de correlación para analizar la relación entre las variables independientes y la dependiente.
- ROC-AUC para diferentes modelos.

## Cómo usar este repositorio
### Instalar Dependencias

Este proyecto utiliza Python y varias bibliotecas. Instala las dependencias necesarias con:

```plaintext
pip install -r requirements.txt
```

### Ejecutar el script

- Abre el archivo Union.ipynb en Jupyter Notebook, Jupyter Lab o Google Colab.
- Ejecuta las celdas en orden para reproducir los resultados:
    - Importación de las bases.
    - Unión de las bases de personas con las de hogares.
      
- Abre el archivo PS2.ipynb en Jupyter Notebook, Jupyter Lab o Google Colab.
- Ejecuta las celdas en orden para reproducir los resultados:
    - Análisis descriptivo de las variables numéricas.
    - Creación de variables de interés.
    - Análisis de correlación.
    - Modelado y predicciones: Regresión lineal y logística, árboles de decisión, random forest y boosting.
    - Evaluación de las predicciones.

### Explorar los resultados

- Revisa las visualizaciones en la carpeta views/ para obtener información clave.
- Consulta el archivo report.pdf en la carpeta document/ para un resumen detallado.

### Características principales
- Obtención de variables: Obtención de variables a nivel hogar en basada en información a nivel individuo usando Python.
- Descripción y análisis de datos: Filtrado, preprocesamiento y análisis exploratorio de datos.
- Modelado Predictivo: Incluye regresión lineal y logística, árboles de decisión, random forest y una predicción por boosting.
- Visualización: Gráficos informativos para apoyar la interpretación de los datos.

### Requisitos
- Python 3.8 o superior
- Bibliotecas principales:
pandas, rarfile, matplotlib, numpy, seaborn, statsmodels, scikit-learn
