# Product Matching

---

### Creador:
- Wilbert Vong

---

#### **Este trabajo consiste en la aplicación del modelo pre entrenado BERT para crear una función de 'Product Matching' para comparar precios de productos idénticos, pero escritos de manera diferente.**

#### **'Product Matching' es un tipo de solución de IA que consiste en identificar y emparejar productos que son esencialmente iguales o muy similares, aunque estén descritos de maneras diferentes en distintas bases de datos o sitios web. Este proceso es de alta importancia rubros como el comercio electrónico, donde varios proveedores pueden ofrecer el mismo producto con descripciones, nombres y formatos de datos diferentes.**

---

## **Funcionamiento**:

#### *Obtención de Embeddings*:
Se obtienen los embeddings de las descripciones usando BERT. Estos embeddings son vectores en un espacio de alta dimensión que representan las descripciones.

#### *Cálculo de similitud*:
Aplicando la fórmula de similitud del coseno: 

$$
cos(θ) = \frac{e_1 \cdot e_2}{\|e_1\| \|e_2\|}
$$

Donde: 

* $e_1$​ y $e_2$ son los embeddings *(vectores)* de las descripciones 1 y 2.

* $cos(θ)$ es el valor de la similitud.

El resultado de la similitud está entre el rango de -1 al 1. Cuanto más cercano sea al 1, quiere decir que ambos vectores tienen mayor similitud, y entre más lejos sea del 1, tienen menos similitud.

#### *Fine-Tuning (opcional)*:
En algunos casos, se puede hacer un ajuste fino (fine-tuning) de BERT si se tiene un conjunto de datos etiquetado específico para el problema de Product Matching. Esto ajusta los pesos del modelo BERT preentrenado para optimizar su rendimiento en una tarea concreta. Sin embargo, este ajuste es opcional y solo necesario si los resultados de inferencia directa no son lo suficientemente buenos.

---

## **Usos prácticos**:

*Comparación de precios*: Identificar el mismo producto en diferentes fuentes para comparar precios.

*Consolidación de Inventarios*: Identificar productos duplicados en bases de datos.

*Recomendaciones Personalizadas*: Sugerir productos relacionados o alternativos basados en similitud con el artículo que el usuario está visualizando.

---

*El modelo pre entrenado aplicado en este trabajo fue [BERT](https://huggingface.co/docs/transformers/model_doc/bert).*

---

## Notebooks

[Notebook - Product Matching](https://colab.research.google.com/drive/1_oVOuObN0cPFvjoLfRn76Js9P91DuXhW?usp=sharing)
